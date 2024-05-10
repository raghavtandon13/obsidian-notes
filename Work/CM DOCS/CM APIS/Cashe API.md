# Stage 1 - Dedupe Check
```json
    {
        partner_name: "CredMantra_Partner1", // DO NOT CHNAGE
        mobile_no: "8094634634", 
        email_id: "ragahv@credmantra.com",
    };
```

```
https://credmantra.com/api/v1/partner-api/cashe/checkDuplicateLead
```
 If  ```Payload  === "NO" ``` then move to stage 2 else show "**Customer Already Registered with Cashe**"
 
 ----
# Stage 2 - Dedupe Check
```json
    {
            partner_name: "CredMantra_Partner1",
            pan: "BUSPT0022l",
            mobileNo: "8094634634",
            name: "firstname lastname"
            addressLine1: "addressLine1",
            locality: "locality",
            pinCode: "101010",
            gender: "M"/"F"
            salary: "50000"
            state: "DELHI"
            city: "Delhi"
            dob: "1998-10-10 00:00:00",
            employmentType: 1,
            salaryReceivedType: 3,
            emailId: "email,
            companyName: lead.empName || "OTHERS",
            loanAmount: 200000,
        };
```

```
https://credmantra.com/api/v1/partner-api/cashe/checkDuplicateLead
```
 If  ```Payload  === "NO" ``` then move to stage 2 else show "**Customer Already Registered with Cashe**"