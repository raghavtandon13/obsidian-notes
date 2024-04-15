curl 
-X POST https://credmantra.com/api/v1/partner-api/fibe 
-H 'Content-Type: application/json' 
-d '{
    "mobilenumber": 8722405343,
    "profile": {
      "firstname": "Hikshath",
      "lastname": "Badyar",
      "dob": "1990-05-28",
      "profession": "Salaried",
      "address1": "",
      "address2": "",
      "landmark": "",
      "city": "",
      "pincode": 560097,
      "maritalstatus": ""
    },
    "finance": {
      "pan": "BYFPK6693D"
    },
    "employeedetails": {
      "employername": "",
      "officeaddress": "",
      "officeCity": "",
      "officepincode": 560097,
      "salary": 208330
    },
    "consent": true,
    "consentDatetime": ""
  }'
  
  
  
{
"mobilenumber":"8722405343",
"status":"Accepted",
"statuscode":200,
"customerid":"1445616798",
"reason":"customer lead updated",
"sanctionLimit":150000,
"responseDate":"2024-02-28 13:35:01",
"esRefId":"28485124yjxagj",
"inPrincipleLimit":0,
"inPrincipleTenure":0,
"redirectionUrl":"https://portal.fibe.in/es-landing?sso=g8qhYGQwdnG3HFo20240228133501","customerType":"A1","highestTenure":12
}