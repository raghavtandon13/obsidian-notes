# DEDUPE

```sh
curl -X POST https://stg-api.mpkt.in/acquisition-affiliate/v1/dedupe/check \
     -H "Content-Type: application/json" \
     -H "api-key: 59D8AB0B311246C58001D9363D35A" \
     -d '{"email_id": "aGVsbG93QGdtYWlsLmNvbQ==", "mobile_number": "ODA5NDExMTk5OQ=="}'

{
    "data": {},
    "message": "New User",
    "status_code": "1205",
    "success": true
}
```

# LEAD PUSH

```sh
curl --location --request POST 'https://stg-api.mpkt.in/acquisition-affiliate/v1/user' \
--header 'api-key: 59D8AB0B311246C58001D9363D35A' \
--header 'Content-Type: application/json' \
--data-raw '{
    "email_id": "hellow@gmail.com",
    "mobile_no": "8094111999",
    "full_name": "santosh mohapatra",
    "first_name": "santosh",
    "middle_name": "",
    "last_name": "mohapatra",
    "date_of_birth": "01-01-2021",
    "gender": "male",
    "profession": "salaried",
    "additional_info": {
        "loan_amount": "50000",
        "loan_tenure": "6 Months",
        "company_type": "private",
        "industry_type": "Information technology",
        "company_name": "TCS",
        "current_designation": "Software Engineer",
        "company_address": "high sky tower",
        "company_pincode": "570001",
        "company_city": "Bangalore",
        "company_state": "Karnataka",
        "current_company_working_years": "3",
        "net_monthly_income": "45000",
        "salary_mode": "Bank",
        "bank_name": "ICICI",
        "pancard": "CXERE5830A",
        "enter_fname_as_per_pancard": "JImmy",
        "enter_lname_as_per_pancard": "Sam",
        "current_address": "4th floor prestige tower",
        "current_pincode": "560001",
        "current_city": "Bangalore",
        "current_state": "Karnataka",
        "current_residence_type": "Rented",
        "years_stayed_in_current_address": "2",
        "education_qualification": "Btech",
        "marital_status": "Single",
        "father_name": "Sam",
        "mother_name": "Jerry",
        "current_total_emi_paid_per_month": "10000",
        "active_creditcard_holder": "Y",
        "offical_email_id": "abc@mpokket.com"
    }
}'

{
    "data": {
        "requestId": "b3a5b079-fc1b-4389-84ae-52899d2aa3b5"
    },
    "message": "Data Accepted Successfully",
    "status_code": "1200",
    "success": true
}
```

# STATUS

```sh
curl -X GET 'https://stg-api.mpkt.in/acquisition-affiliate/v1/user?request_id=b3a5b079-fc1b-4389-84ae-52899d2aa3b5' \
-H 'api-key: 59D8AB0B311246C58001D9363D35A' \
--data-raw ''

{
    "data": {
        "acquisition_status": "Rejected On Request",
        "message": {
            "duplicate_mobile": "Mobile Number Already Exists"
        },
        "request_id": "b3a5b079-fc1b-4389-84ae-52899d2aa3b5",
        "user_id": "NA"
    },
    "message": "Data Fetched Successfully",
    "status_code": "1202",
    "success": true
}
```
