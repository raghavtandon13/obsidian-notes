# Eligibility

```sh
curl --request POST \
  --url https://prod.zype.co.in/attribution-service/api/v1/underwriting/customerEligibility \
  --header 'Content-Type: application/json' \
  --data '
{
  "mobileNumber": "7970076008",
  "panNumber": "BTCPB0794G",
  "partnerId": "66603df5a5168dbb6e95ec25"
}'
```

```json
{ "message": "ACCEPT" }
```

# PreApprovalOffer

```sh
curl --request POST \
  --url https://prod.zype.co.in/attribution-service/api/v1/underwriting/preApprovalOffer \
  --header 'Content-Type: application/json' \
  --data '
{
    "mobileNumber": "7970076008",
    "email": "shivendu1996@gmail.com",
    "panNumber": "BTCPB0794G",
    "name": "shivendu yadav",
    "dob": "2001-08-23",
    "employmentType": "salaried",
    "income": 100000,
    "partnerId": "66603df5a5168dbb6e95ec25",
    "orgName": "Viacom",
    "bureauType": 3
}
'
```

```json
{ "status": "ACCEPT", "offer": 150000 }
```
