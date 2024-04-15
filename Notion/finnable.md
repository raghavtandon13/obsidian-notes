```JavaScript
//---------------------------------------------------------------------------------------------//
// FINNABLE API--------FINNABLE API--------FINNABLE API--------FINNABLE API--------FINNABLE API//
//---------------------------------------------------------------------------------------------//

const finnableApiKey = "YOUR_FINNABLE_API_KEY";
const finnableApiUrl = "https://finnable-api-url.com";

router.post("/finnable", async (req, res) => {
  try {
    // Step 1: Get the Access Token
    const timestamp = new Date().toISOString();
    const accessTokenData = JSON.stringify({ });

    const accessTokenSignature = crypto
      .createHmac("sha256", finnableApiKey)
      .update(`POST/accessToken${timestamp}${accessTokenData}`)
      .digest("hex");

    const accessTokenHeaders = {
      "finnable-api-key": finnableApiKey,
      "Content-Type": "application/json",
      "finnable-access-timestamp": timestamp,
      "finnable-api-signature": accessTokenSignature,
    };

    const accessTokenResponse = await axios.post(
      `${finnableApiUrl}/accessToken`,
      accessTokenData,
      { headers: accessTokenHeaders }
    );

    const finnableAccessToken = accessTokenResponse.data.accessToken;

    // Step 2: Use the Access Token for Sanction
    const sanctionData = req.body;

    const sanctionHeaders = {
      "finnable-access-token": finnableAccessToken,
      "Content-Type": "application/json",
    };

    const sanctionResponse = await axios.post(
      `${finnableApiUrl}/sanction`,
      sanctionData,
      { headers: sanctionHeaders }
    );

    const sanctionDecision = sanctionResponse.data;

    res.json({ accessToken: finnableAccessToken, sanctionDecision });
  } catch (error) {
    console.error("Error:", error);
    res.status(500).json({
      error: "An error occurred while processing the Finnable request.",
    });
  }
});

//---------------------------------------------------------------------------------------------//
//---MONEY WIDE----------MONEY WIDE----------MONEY WIDE----------MONEY WIDE----------MONEY WIDE//
//---------------------------------------------------------------------------------------------//
const tokenApiUrl = "https://deployapigateway.moneywide.com/token";
const tokenApiCredentials = {
  client_id: "MWide",
  client_key: "hsdfgh*&^&dgdhg87",
  source: "MWide",
};

const losApiUrl =
  "https://deployapigateway.moneywide.com/api/connectorapi-updated-flow";

let authToken = "";

app.post("/moneywide", async (req, res) => {
  try {
    const tokenResponse = await axios.post(tokenApiUrl, tokenApiCredentials);

    if (tokenResponse.data.status === "1") {
      authToken = tokenResponse.data.token;

      const losApiResponse = await axios.post(
        losApiUrl,
        req.body, // Using body data for LOS Push API request
        {
          headers: {
            "API-CLIENT": "MWide",
            "API-KEY": authToken,
          },
        }
      );

      res.json(losApiResponse.data);
    } else {
      res.status(500).json({ error: "Token generation failed" });
    }
  } catch (error) {
    console.error("Error:", error.message);
    res.status(500).json({ error: "An error occurred" });
  }
});

//--------------------------------------------------------------------------------//
// LendingKart API------LendingKart API------LendingKart API------LendingKart API //
// leadExists===false
//--------------------------------------------------------------------------------//
const LK_Key = "your_api_key_here";

// Define the base URL for Lendingkart API
const lendingkartBaseUrl = "https://api.lendingkart.com/v2/partner/leads";

router.post("/lendingkart", async (req, res) => {
  // Extract mobile and email from the request body
  const { mobile, email, ...otherData } = req.body;

  // Step 1: Check if the user exists
  try {
    const existsResponse = await axios.post(
      `${lendingkartBaseUrl}/lead-exists-status`,
      { mobile, email },
      {
        headers: { "X-Api-Key": LK_Key },
      }
    );

    if (existsResponse.data === false) {
      // Step 2: User doesn't exist, proceed to create a new application
      try {
        const createResponse = await axios.post(
          `${lendingkartBaseUrl}/create-application`,
          { mobile, email, ...otherData },
          {
            headers: { "X-Api-Key": LK_Key },
          }
        );

        // Assuming Lendingkart responds with some confirmation data
        res.json({
          message: "Application created successfully",
          data: createResponse.data,
        });
      } catch (error) {
        console.error("Error creating application:", error);
        res.status(500).json({ error: "Failed to create application" });
      }
    } else {
      // User already exists
      res.status(400).json({ error: "User already exists" });
    }
  } catch (error) {
    console.error("Error checking user existence:", error);
    res.status(500).json({ error: "Failed to check user existence" });
  }
});

router.get("/lendingkart-status/:applicationId", async (req, res) => {
  const { applicationId } = req.params;

  try {
    const response = await axios.get(
      `${lendingkartBaseUrl}/applicationStatus/${applicationId}`,
      {
        headers: { "X-Api-Key": apiKey },
      }
    );

    res.json(response.data);
  } catch (error) {
    console.error("Error checking application status:", error);
    res.status(500).json({ error: "Failed to check application status" });
  }
});

//--------------------------------------------------------------------------------//
// UPWARDS--------UPWARDS API-------UPWARDS API------UPWARDS API------UPWARDS API //
//--------------------------------------------------------------------------------//

// Define the route for affiliate user authentication
router.post("/upwards", async (req, res) => {
  try {
    const { pan, social_email_id, ...otherData } = req.body;

    const affiliatedUserId = "your_user_id";
    const affiliatedUserSecret = "your_user_secret";

    const response = await axios.post(
      "https://uat1.upwards.in/af/v1/authenticate/",
      {
        affiliated_user_id: affiliatedUserId,
        affiliated_user_secret: affiliatedUserSecret,
      }
    );

    if (response.data && response.data.affiliated_user_session_token) {
      const affiliated_user_session_token =
        response.data.affiliated_user_session_token;

      // Store the token for use in subsequent requests
      const headers = {
        "Affiliated-User-Id": affiliatedUserId,
        "Affiliated-User-Session-Token": affiliated_user_session_token,
      };

      // Modify this part to include the pan and social_email_id
      const loanEligibilityRequest = {
        pan: pan,
        social_email_id: social_email_id,
      };

      const eligibilityResponse = await axios.post(
        "https://uat1.upwards.in/af/v1/customer/loan/eligibility/",
        loanEligibilityRequest,
        {
          headers,
        }
      );

      if (
        eligibilityResponse.data &&
        eligibilityResponse.data.is_eligible === true
      ) {
        // Proceed to post data to the next endpoint
        const loanDataRequest = req.body; // Assuming you want to send the entire request body

        const loanDataResponse = await axios.post(
          "https://uat1.upwards.in/af/v2/customer/loan/data",
          loanDataRequest,
          {
            headers,
          }
        );

        // Handle the response from the data posting if needed
        res.status(200).json({ message: "Data posted successfully" });
      } else {
        res.status(403).json({ message: "You are not eligible for a loan" });
      }
    } else {
      res.status(400).json({ error: "Invalid response from the API" });
    }
  } catch (error) {
    console.error("Error:", error);
    res.status(500).json({ error: "An error occurred" });
  }
});
```