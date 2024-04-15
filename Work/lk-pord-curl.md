---
id: lk-pord-curl
aliases:
  - lk pord curl
tags: []
---

# lk pord curl
```js
curl --location 'https://credmantra.com/api/v1/partner-api/lendingkart/p/create-application' \    --header 'Content-Type: application/json' \
--header 'Accept: application/json' \
--header 'X-Api-Key: 4c71ff7f-9dff-4ebf-bd5a-0e475ddf68b1' \
--data-raw '{
    "firstName": "Jeevith",
    "lastName": "R",
    "email": "himanshutest@testmail.com",
    "mobile": "7239970840",
    "personalDob": "1990-05-21",
    "personalPAN": "GHTPA3164O",
    "gender": "MALE",
    "personalAddress": {
      "pincode": "560100",
      "city": "Bengaluru",
      "state": "Karnataka"
    },
    "loanAmount": 1000000,
    "productType": "Personal Loan",
    "uniqueId": "CP-0111",
    "cibilConsentForLK": true,
    "otherFields": {
      "consentTimestamp": "2023-12-13T06:57:32.000+00:00",
      "employmentType": "FULL_TIME",
      "monthlySalary": 100000,
      "monthlyProfit": null,
      "tenure": 18,
      "itrFiled": true,
      "itrRange": "THREE_TO_FIVE_LACS",
      "maritalStatus": "SINGLE",
      "companyName": "OTHERS",
      "companyEmailId": "hmsingh@testmail.com"
    }
  }'
{"leadId":null,"applicationId":null,"message":"DATA_INSUFFICIENT","errorMessageList":["Invalid PAN"],"uniqueId":"CP-0111","loanDeliveryMethod":null,"lender":null,"redirectionLink":null}%
```
# our own lead
```js
 curl --location 'https://api.lendingkart.com/v2/partner/leads/create-application' \
--header 'Content-Type: application/json' \
--header 'Accept: application/json' \
--header 'X-Api-Key: 4c71ff7f-9dff-4ebf-bd5a-0e475ddf68b1' \
--data-raw '{
    "firstName": "Yogesh",
    "lastName": "Raut",
    "email": "yraut9387@gmail.com",
    "mobile": "9028031667",
    "personalDob": "1998-09-04",
    "personalPAN": "AJAPR3971J",
    "gender": "MALE",
    "personalAddress": {
      "pincode": "414001",
      "city": "Ahmednagar",
      "state": "Maharashtra"
    },
    "loanAmount": 1000000,
    "productType": "Personal Loan",
    "uniqueId": "CP-0118",
    "cibilConsentForLK": true,
    "otherFields": {
      "consentTimestamp": "2023-12-13T06:57:32.000+00:00",
      "employmentType": "FULL_TIME",
      "monthlySalary": 31000,
      "monthlyProfit": null,
      "tenure": 18,
      "itrFiled": false,
      "itrRange": null,
      "maritalStatus": "SINGLE",
      "companyName": "OTHERS",
      "companyEmailId": "yraut9387@gmail.com"
    }
  }'
{"leadId":"CI-002006063","applicationId":"AI-001625656","message":"ELIGIBLE","errorMessageList":[],"uniqueId":"CP-0118","loanDeliveryMethod":null,"lender":null,"redirectionLink":"https://zype.sng.link/Bjygt/443e?_dl=com.zype.mobile&_smtype=3"}%

```

```http
POST /admin/lead/v2/partner/leads/create-application HTTP/1.1
Host: lkext.lendingkart.com
Content-Type: application/json
X-Api-Key: 2e067259-5f4a-4ed1-880f-ece8e7b1b9dd

{
    "firstName": "DEBABRATA",
    "lastName": " RAUL",
    "email": "bhghav@candad.co.in",
    "mobile": "8094634621",
    "businessAge": 50,
    "businessRevenue": 1200000,
    "registeredAs": "Proprietorship",
    "personalDob": "1990-05-21",
    "personalPAN": "BUSPT0442K",
    "gender": "MALE",
    "cibilConsentForLK": true,
    "personalAddress": {
        "pincode": "560100",
        "address": "wferferfe"
    },
    "businessRunBy": "Self",
    "loanAmount": 700000,
    "businessAddress": {
        "address": "A-215, SRK silicana",
        "pincode": "560100"
    },
    "productCategory": "Film Producer",
    "natureOfBusiness": [
        "Importer"
    ],
    "uniqueId": "xyz123xyz"
}


GET /posts
Host: jsonplaceholder.typicode.com
```

