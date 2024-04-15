curl -L -X GET 'http://localhost:3000/api/v1/partner-api/moneytap/create' -H 'Content-Type: application/json' --data-raw '{
    "emailId": "abc@example.org",
    "phone": "8094634635",
    "name": "Raman Singh",
    "panNumber": "BUSPK0563L",
    "dateOfBirth": "1984-08-20",
    "gender": "MALE",
    "jobType": "SALARIED",
    "homeAddress": {
        "addressLine1": "address line 1",
        "addressLine2": "address line 2",
        "city": "Bangalore",
        "state": "Karnataka",
        "pincode": "560066"
    },
    "residenceType": "OWNED_BY_SELF_SPOUSE",
    "fatherName": "Fathers Name",
    "motherName": "Mothers Name",
    "officeAddress": {
        "addressLine1": "office address line 1",
        "addressLine2": "office address line 2",
        "city": "Bangalore",
        "state": "Karnataka",
        "pincode": "560103"
    },
    "designation": "Product Manager",
    "companyName": "Microsoft",
    "companyType": "PUBLIC_LIMITED",
    "officeEmail": "xyx@office.org",
    "incomeInfo": {
        "declared": 35000,
        "mode": "NETBANKING"
    }
}'
{"customerId":"d0d99339-ba6f-4da3-ad93-

**RESPONSE**

b78ec2968fc5","softApprovalStatus":"processing","finalApprovalStatus":"processing","status":"PENDING","amount":0}