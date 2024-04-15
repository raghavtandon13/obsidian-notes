# Overview
1. **Register User** - It will send an OTP to the input mobile number.

2. **Login User** - It will generate a JWT token for that user to be further used in other APIs.

3. **Upload & Validate PAN** - It is used to upload user PAN (front image) & validate, based on the validate response - Name, PAN Number & DOB will be pre-filled for that user.  

4. **Update Profile** - It is used to update user profile details like Marital Status, Gender, Address etc.

5. **Required Loan Details | BL** - It is used to fetch the relevant loan related questions to be used for application. Category is BL & subcategory is SME.

6. **Apply Loan | BL** - It is used to apply for Business Loan. It will include all the fields fetched from "Required Loan Details | BL" API in request body.

  

Below are the details to use Vitto APIs in **staging** environment (these are the two headers which needs to be passed to all API requests) - 

>**X-Partner-API-Key**: 7ba1d96dfc74f0eed67d351e0f7830d2dae8eb732f47e4e8e4a138143008765b  
**X-Partner-Id**: ceba5f64579232655bd11627ae3f0023
# 1. Register User
```bash
curl -L -X POST 'https://apis-staging.vitto.money/users/api/v1/ext/register' -H 'X-Partner-Id: ceba5f64579232655bd11627ae3f0023' -H 'X-Partner-API-Key: 7ba1d96dfc74f0eed67d351e0f7830d2dae8eb732f47e4e8e4a138143008765b' -H 'Content-Type: application/json' -d '{
  "phoneNumber": "+91-8094634634"
}'
```

```json
{
    "status": "SUCCESS",
    "message": "Message Sent"
}
```

# 2. Login User
```bash
curl -L -X POST 'https://apis-staging.vitto.money/users/api/v1/ext/login' -H 'X-Partner-Id: ceba5f64579232655bd11627ae3f0023' -H 'X-Partner-API-Key: 7ba1d96dfc74f0eed67d351e0f7830d2dae8eb732f47e4e8e4a138143008765b' -H 'Content-Type: application/json' -d '{
  "phoneNumber": "+91-8094634634",
  "otp":"921298"
}'
```

```json
{
    "userData": {
        "id": "+91-8094634634",
        "name": null,
        "gender": null,
        "address": null,
        "dob": null,
        "email": null,
        "fcmToken": null,
        "preferredLanguageId": 2,
        "profilePic": null,
        "city": null,
        "state": null,
        "pinCode": null,
        "liveVideo": null,
        "isVerified": false,
        "isBanned": false,
        "cibilScore": null,
        "mobilityProbability": null,
        "photoAuthenticityScore": null,
        "taggedOrganizationID": null,
        "taggedBranchID": null,
        "onboardingLocationGeoHash": null,
        "onboardingMode": null,
        "isAgent": null,
        "agentUserId": null,
        "noOfLoansTaken": 0,
        "noOfLoansRepaid": 0,
        "noOfLoansPending": 0,
        "partnerOrgCustomerId": null,
        "loggedInPhoneNo": null,
        "fatherName": null,
        "lastLoggedInDate": null,
        "refreshTokenID": null,
        "hasLoggedIn": true,
        "maritalStatus": null,
        "bureauRegisteredPhoneNo": null,
        "metadata": null,
        "kycStatus": null,
        "createdAt": "2024-04-15T06:32:15.559Z",
        "updatedAt": "2024-04-15T06:32:15.559Z",
        "docs": {
            "panNo": null
        },
        "panVerified": false
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjbGllbnQiOnsiaWQiOiIrOTEtODA5NDYzNDYzNCIsIm5hbWUiOm51bGwsImdlbmRlciI6bnVsbCwiYWRkcmVzcyI6bnVsbCwiZG9iIjpudWxsLCJlbWFpbCI6bnVsbCwiZmNtVG9rZW4iOm51bGwsInByZWZlcnJlZExhbmd1YWdlSWQiOjIsInByb2ZpbGVQaWMiOm51bGwsImNpdHkiOm51bGwsInN0YXRlIjpudWxsLCJwaW5Db2RlIjpudWxsLCJsaXZlVmlkZW8iOm51bGwsImlzVmVyaWZpZWQiOmZhbHNlLCJpc0Jhbm5lZCI6ZmFsc2UsImNpYmlsU2NvcmUiOm51bGwsIm1vYmlsaXR5UHJvYmFiaWxpdHkiOm51bGwsInBob3RvQXV0aGVudGljaXR5U2NvcmUiOm51bGwsInRhZ2dlZE9yZ2FuaXphdGlvbklEIjpudWxsLCJ0YWdnZWRCcmFuY2hJRCI6bnVsbCwib25ib2FyZGluZ0xvY2F0aW9uR2VvSGFzaCI6bnVsbCwib25ib2FyZGluZ01vZGUiOm51bGwsImlzQWdlbnQiOm51bGwsImFnZW50VXNlcklkIjpudWxsLCJub09mTG9hbnNUYWtlbiI6MCwibm9PZkxvYW5zUmVwYWlkIjowLCJub09mTG9hbnNQZW5kaW5nIjowLCJwYXJ0bmVyT3JnQ3VzdG9tZXJJZCI6bnVsbCwibG9nZ2VkSW5QaG9uZU5vIjpudWxsLCJmYXRoZXJOYW1lIjpudWxsLCJsYXN0TG9nZ2VkSW5EYXRlIjpudWxsLCJyZWZyZXNoVG9rZW5JRCI6bnVsbCwiaGFzTG9nZ2VkSW4iOnRydWUsIm1hcml0YWxTdGF0dXMiOm51bGwsImJ1cmVhdVJlZ2lzdGVyZWRQaG9uZU5vIjpudWxsLCJtZXRhZGF0YSI6bnVsbCwia3ljU3RhdHVzIjpudWxsLCJjcmVhdGVkQXQiOiIyMDI0LTA0LTE1VDA2OjMyOjE1LjU1OVoiLCJ1cGRhdGVkQXQiOiIyMDI0LTA0LTE1VDA2OjMyOjE1LjU1OVoiLCJkb2NzIjp7InBhbk5vIjpudWxsfSwicGFuVmVyaWZpZWQiOmZhbHNlfSwiaWF0IjoxNzEzMTYyNzM1LCJleHAiOjE3MTMyNDkxMzV9.6Z2CNmKOQ_EzIJ5GVlkRDDZwc06Q8tIQOudxm-5KKJk"
}
```
# 3. Upload & Validate PAN
```bash
curl -L -X POST 'https://apis-staging.vitto.money/users/api/v1/ext/onboard/pan' -H 'X-Partner-Id: ceba5f64579232655bd11627ae3f0023' -H 'X-Partner-API-Key: 7ba1d96dfc74f0eed67d351e0f7830d2dae8eb732f47e4e8e4a138143008765b' -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjbGllbnQiOnsiaWQiOiIrOTEtODA5NDYzNDYzNCIsIm5hbWUiOm51bGwsImdlbmRlciI6bnVsbCwiYWRkcmVzcyI6bnVsbCwiZG9iIjpudWxsLCJlbWFpbCI6bnVsbCwiZmNtVG9rZW4iOm51bGwsInByZWZlcnJlZExhbmd1YWdlSWQiOjIsInByb2ZpbGVQaWMiOm51bGwsImNpdHkiOm51bGwsInN0YXRlIjpudWxsLCJwaW5Db2RlIjpudWxsLCJsaXZlVmlkZW8iOm51bGwsImlzVmVyaWZpZWQiOmZhbHNlLCJpc0Jhbm5lZCI6ZmFsc2UsImNpYmlsU2NvcmUiOm51bGwsIm1vYmlsaXR5UHJvYmFiaWxpdHkiOm51bGwsInBob3RvQXV0aGVudGljaXR5U2NvcmUiOm51bGwsInRhZ2dlZE9yZ2FuaXphdGlvbklEIjpudWxsLCJ0YWdnZWRCcmFuY2hJRCI6bnVsbCwib25ib2FyZGluZ0xvY2F0aW9uR2VvSGFzaCI6bnVsbCwib25ib2FyZGluZ01vZGUiOm51bGwsImlzQWdlbnQiOm51bGwsImFnZW50VXNlcklkIjpudWxsLCJub09mTG9hbnNUYWtlbiI6MCwibm9PZkxvYW5zUmVwYWlkIjowLCJub09mTG9hbnNQZW5kaW5nIjowLCJwYXJ0bmVyT3JnQ3VzdG9tZXJJZCI6bnVsbCwibG9nZ2VkSW5QaG9uZU5vIjpudWxsLCJmYXRoZXJOYW1lIjpudWxsLCJsYXN0TG9nZ2VkSW5EYXRlIjpudWxsLCJyZWZyZXNoVG9rZW5JRCI6bnVsbCwiaGFzTG9nZ2VkSW4iOnRydWUsIm1hcml0YWxTdGF0dXMiOm51bGwsImJ1cmVhdVJlZ2lzdGVyZWRQaG9uZU5vIjpudWxsLCJtZXRhZGF0YSI6bnVsbCwia3ljU3RhdHVzIjpudWxsLCJjcmVhdGVkQXQiOiIyMDI0LTA0LTE1VDA2OjMyOjE1LjU1OVoiLCJ1cGRhdGVkQXQiOiIyMDI0LTA0LTE1VDA2OjMyOjE1LjU1OVoiLCJkb2NzIjp7InBhbk5vIjpudWxsfSwicGFuVmVyaWZpZWQiOmZhbHNlfSwiaWF0IjoxNzEzMTYyNzM1LCJleHAiOjE3MTMyNDkxMzV9.6Z2CNmKOQ_EzIJ5GVlkRDDZwc06Q8tIQOudxm-5KKJk' -F 'panFront=@"/C:/Users/ragha/Downloads/CM Docs/docus/pan.jpg"'
```
```json
{
    "errorCode": "invalidPanFrontPic",
    "errorDescription": "The pan front pic is either not supplied or invalid",
    "debug-Ref-ID": "d8489890-faf2-11ee-ac09-57686e7f350e"
}
```
```json
{
    "status": "success",
    "profileDetails": {
        "name": "NARENDRAN MOHAN",
        "dob": "05/08/1995",
        "panNo": "FAIPM3778N",
        "dobDateType": "DOB"
    },
    "panURL": "https://dw5t3tc93tvnn.cloudfront.net/userData/%2B91-6284462133/uploads/pan/c81b860c-698b-4f21-af27-e7964f2899d3.jpeg"
}
```
```json
{
    "errorCode": "panAlreadyRegistered",
    "errorDescription": "The uploaded panNo is already registered with XXXXX01603, please login with that no.",
    "debug-Ref-ID": "31251270-af7d-11ee-9fe1-bb7ab223d57e"
}
```
# 4. Update Profile
```bash
curl -L -X PATCH 'https://apis-staging.vitto.money/users/api/v1/ext/profile' -H 'X-Partner-Id: ceba5f64579232655bd11627ae3f0023' -H 'X-Partner-API-Key: 7ba1d96dfc74f0eed67d351e0f7830d2dae8eb732f47e4e8e4a138143008765b' -H 'Content-Type: application/json' -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjbGllbnQiOnsiaWQiOiIrOTEtODA5NDYzNDYzNCIsIm5hbWUiOm51bGwsImdlbmRlciI6bnVsbCwiYWRkcmVzcyI6bnVsbCwiZG9iIjpudWxsLCJlbWFpbCI6bnVsbCwiZmNtVG9rZW4iOm51bGwsInByZWZlcnJlZExhbmd1YWdlSWQiOjIsInByb2ZpbGVQaWMiOm51bGwsImNpdHkiOm51bGwsInN0YXRlIjpudWxsLCJwaW5Db2RlIjpudWxsLCJsaXZlVmlkZW8iOm51bGwsImlzVmVyaWZpZWQiOmZhbHNlLCJpc0Jhbm5lZCI6ZmFsc2UsImNpYmlsU2NvcmUiOm51bGwsIm1vYmlsaXR5UHJvYmFiaWxpdHkiOm51bGwsInBob3RvQXV0aGVudGljaXR5U2NvcmUiOm51bGwsInRhZ2dlZE9yZ2FuaXphdGlvbklEIjpudWxsLCJ0YWdnZWRCcmFuY2hJRCI6bnVsbCwib25ib2FyZGluZ0xvY2F0aW9uR2VvSGFzaCI6bnVsbCwib25ib2FyZGluZ01vZGUiOm51bGwsImlzQWdlbnQiOm51bGwsImFnZW50VXNlcklkIjpudWxsLCJub09mTG9hbnNUYWtlbiI6MCwibm9PZkxvYW5zUmVwYWlkIjowLCJub09mTG9hbnNQZW5kaW5nIjowLCJwYXJ0bmVyT3JnQ3VzdG9tZXJJZCI6bnVsbCwibG9nZ2VkSW5QaG9uZU5vIjpudWxsLCJmYXRoZXJOYW1lIjpudWxsLCJsYXN0TG9nZ2VkSW5EYXRlIjpudWxsLCJyZWZyZXNoVG9rZW5JRCI6bnVsbCwiaGFzTG9nZ2VkSW4iOnRydWUsIm1hcml0YWxTdGF0dXMiOm51bGwsImJ1cmVhdVJlZ2lzdGVyZWRQaG9uZU5vIjpudWxsLCJtZXRhZGF0YSI6bnVsbCwia3ljU3RhdHVzIjpudWxsLCJjcmVhdGVkQXQiOiIyMDI0LTA0LTE1VDA2OjMyOjE1LjU1OVoiLCJ1cGRhdGVkQXQiOiIyMDI0LTA0LTE1VDA2OjMyOjE1LjU1OVoiLCJkb2NzIjp7InBhbk5vIjpudWxsfSwicGFuVmVyaWZpZWQiOmZhbHNlfSwiaWF0IjoxNzEzMTYyNzM1LCJleHAiOjE3MTMyNDkxMzV9.6Z2CNmKOQ_EzIJ5GVlkRDDZwc06Q8tIQOudxm-5KKJk' -d '{
  "name":"Himanshu Singh",
  "address":"New Delhi",
  "dob":"31-08-1999",
  "gender":"male",
  "maritalStatus": "Single",
  "pinCode":"110078"
}'
```
```json
{
    "status": "success"
}
```
```json
{
    "errorCode": "invalidGender",
    "errorDescription": "Please select a valid gender from following options ('male', 'female' , 'others') .",
    "debug-Ref-ID": "ae67ae60-af7c-11ee-9fe1-bb7ab223d57e"
}
```
# 5. Required Loan Details
```bash
curl -L -X GET 'https://apis-staging.vitto.money/loans/api/v1/loans/ext/fields/HSF/HPL' -H 'X-Partner-Id: ceba5f64579232655bd11627ae3f0023' -H 'X-Partner-API-Key: 7ba1d96dfc74f0eed67d351e0f7830d2dae8eb732f47e4e8e4a138143008765b' -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjbGllbnQiOnsiaWQiOiIrOTEtODA5NDYzNDYzNCIsIm5hbWUiOm51bGwsImdlbmRlciI6bnVsbCwiYWRkcmVzcyI6bnVsbCwiZG9iIjpudWxsLCJlbWFpbCI6bnVsbCwiZmNtVG9rZW4iOm51bGwsInByZWZlcnJlZExhbmd1YWdlSWQiOjIsInByb2ZpbGVQaWMiOm51bGwsImNpdHkiOm51bGwsInN0YXRlIjpudWxsLCJwaW5Db2RlIjpudWxsLCJsaXZlVmlkZW8iOm51bGwsImlzVmVyaWZpZWQiOmZhbHNlLCJpc0Jhbm5lZCI6ZmFsc2UsImNpYmlsU2NvcmUiOm51bGwsIm1vYmlsaXR5UHJvYmFiaWxpdHkiOm51bGwsInBob3RvQXV0aGVudGljaXR5U2NvcmUiOm51bGwsInRhZ2dlZE9yZ2FuaXphdGlvbklEIjpudWxsLCJ0YWdnZWRCcmFuY2hJRCI6bnVsbCwib25ib2FyZGluZ0xvY2F0aW9uR2VvSGFzaCI6bnVsbCwib25ib2FyZGluZ01vZGUiOm51bGwsImlzQWdlbnQiOm51bGwsImFnZW50VXNlcklkIjpudWxsLCJub09mTG9hbnNUYWtlbiI6MCwibm9PZkxvYW5zUmVwYWlkIjowLCJub09mTG9hbnNQZW5kaW5nIjowLCJwYXJ0bmVyT3JnQ3VzdG9tZXJJZCI6bnVsbCwibG9nZ2VkSW5QaG9uZU5vIjpudWxsLCJmYXRoZXJOYW1lIjpudWxsLCJsYXN0TG9nZ2VkSW5EYXRlIjpudWxsLCJyZWZyZXNoVG9rZW5JRCI6bnVsbCwiaGFzTG9nZ2VkSW4iOnRydWUsIm1hcml0YWxTdGF0dXMiOm51bGwsImJ1cmVhdVJlZ2lzdGVyZWRQaG9uZU5vIjpudWxsLCJtZXRhZGF0YSI6bnVsbCwia3ljU3RhdHVzIjpudWxsLCJjcmVhdGVkQXQiOiIyMDI0LTA0LTE1VDA2OjMyOjE1LjU1OVoiLCJ1cGRhdGVkQXQiOiIyMDI0LTA0LTE1VDA2OjMyOjE1LjU1OVoiLCJkb2NzIjp7InBhbk5vIjpudWxsfSwicGFuVmVyaWZpZWQiOmZhbHNlfSwiaWF0IjoxNzEzMTYyNzM1LCJleHAiOjE3MTMyNDkxMzV9.6Z2CNmKOQ_EzIJ5GVlkRDDZwc06Q8tIQOudxm-5KKJk'
```
```json
{
    "subCategoryName": "Home Purchase Loan",
    "reqdFields": [
        {
            "displayName": "Employment Type",
            "type": "enum",
            "value": [
                "Self_Employed",
                "Salaried"
            ],
            "field": "employmentType"
        },
        {
            "displayName": "Work Frequency",
            "type": "enum",
            "value": [
                "Regular",
                "Seasonal"
            ],
            "field": "workFrequency"
        },
        {
            "displayName": "Income Type",
            "type": "enum",
            "value": [
                "Daily",
                "Monthly",
                "Half_Yearly",
                "Yearly"
            ],
            "field": "incomeType"
        },
        {
            "displayName": "Monthly Income",
            "type": "double",
            "lowerBound": 1000,
            "upperBound": 200000,
            "field": "monthlyIncome"
        },
        {
            "displayName": "Loan Options",
            "type": "enum",
            "value": [
                "New_Loan",
                "Balance_Transfer"
            ],
            "field": "loanOption"
        },
        {
            "displayName": "When do you need loan?",
            "type": "enum",
            "value": [
                "Within_24_Hrs",
                "Next_3_days",
                "With_in_a_week",
                "More_than_a_week"
            ],
            "field": "loanReq"
        },
        {
            "displayName": "Property Identified",
            "type": "enum",
            "value": [
                "Yes",
                "No"
            ],
            "field": "propertyIdentified"
        },
        {
            "displayName": "Loan Amount",
            "type": "double",
            "lowerBound": 50000,
            "upperBound": 50000000,
            "field": "loanAmount"
        },
        {
            "displayName": "Loan Tenure",
            "type": "integer",
            "lowerBound": 1,
            "upperBound": 36,
            "field": "loanTenure"
        }
    ]
}
```
# 6. Apply Loan
```bash
curl -L -X POST 'https://apis-staging.vitto.money/loans/api/v1/loans/ext/leads' -H 'X-Partner-Id: ceba5f64579232655bd11627ae3f0023' -H 'X-Partner-API-Key: 7ba1d96dfc74f0eed67d351e0f7830d2dae8eb732f47e4e8e4a138143008765b' -H 'Content-Type: application/json' -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjbGllbnQiOnsiaWQiOiIrOTEtODA5NDYzNDYzNCIsIm5hbWUiOm51bGwsImdlbmRlciI6bnVsbCwiYWRkcmVzcyI6bnVsbCwiZG9iIjpudWxsLCJlbWFpbCI6bnVsbCwiZmNtVG9rZW4iOm51bGwsInByZWZlcnJlZExhbmd1YWdlSWQiOjIsInByb2ZpbGVQaWMiOm51bGwsImNpdHkiOm51bGwsInN0YXRlIjpudWxsLCJwaW5Db2RlIjpudWxsLCJsaXZlVmlkZW8iOm51bGwsImlzVmVyaWZpZWQiOmZhbHNlLCJpc0Jhbm5lZCI6ZmFsc2UsImNpYmlsU2NvcmUiOm51bGwsIm1vYmlsaXR5UHJvYmFiaWxpdHkiOm51bGwsInBob3RvQXV0aGVudGljaXR5U2NvcmUiOm51bGwsInRhZ2dlZE9yZ2FuaXphdGlvbklEIjpudWxsLCJ0YWdnZWRCcmFuY2hJRCI6bnVsbCwib25ib2FyZGluZ0xvY2F0aW9uR2VvSGFzaCI6bnVsbCwib25ib2FyZGluZ01vZGUiOm51bGwsImlzQWdlbnQiOm51bGwsImFnZW50VXNlcklkIjpudWxsLCJub09mTG9hbnNUYWtlbiI6MCwibm9PZkxvYW5zUmVwYWlkIjowLCJub09mTG9hbnNQZW5kaW5nIjowLCJwYXJ0bmVyT3JnQ3VzdG9tZXJJZCI6bnVsbCwibG9nZ2VkSW5QaG9uZU5vIjpudWxsLCJmYXRoZXJOYW1lIjpudWxsLCJsYXN0TG9nZ2VkSW5EYXRlIjpudWxsLCJyZWZyZXNoVG9rZW5JRCI6bnVsbCwiaGFzTG9nZ2VkSW4iOnRydWUsIm1hcml0YWxTdGF0dXMiOm51bGwsImJ1cmVhdVJlZ2lzdGVyZWRQaG9uZU5vIjpudWxsLCJtZXRhZGF0YSI6bnVsbCwia3ljU3RhdHVzIjpudWxsLCJjcmVhdGVkQXQiOiIyMDI0LTA0LTE1VDA2OjMyOjE1LjU1OVoiLCJ1cGRhdGVkQXQiOiIyMDI0LTA0LTE1VDA2OjMyOjE1LjU1OVoiLCJkb2NzIjp7InBhbk5vIjpudWxsfSwicGFuVmVyaWZpZWQiOmZhbHNlfSwiaWF0IjoxNzEzMTYyNzM1LCJleHAiOjE3MTMyNDkxMzV9.6Z2CNmKOQ_EzIJ5GVlkRDDZwc06Q8tIQOudxm-5KKJk' -d '{
    "loanCategory":"HSF",
    "loanSubCategory":"HPL",
    "loanApplicationDetails":{
        "employmentType":"Salaried",
        "workFrequency":"Regular",
        "incomeType":"Monthly",
        "monthlyIncome":"50000",
        "loanOption":"New_Loan",
        "loanReq":"With_in_a_week",
        "propertyIdentified":"Yes",
        "loanAmount":"50000",
        "loanTenure":"5"
    }
}'
```
```json
{
    "status": "success",
    "applicationID": "HSFHPL00606",
    "id": 606
}
```
```json
{
    "errorCode": "invalidLoanApplicationField",
    "errorDescription": "Request body has invalid/missing data for field: [object Object].",
    "debug-Ref-ID": "00491da0-faf4-11ee-ab37-c3b09c8c9466"
}
``` 
```json
{
    "errorCode": "activeApplicationPresent",
    "errorDescription": "You have already applied for loan in last 90 days. Please wait for 89 days more.",
    "debug-Ref-ID": "778b9d90-af7f-11ee-952a-958c305782e7"
}
```