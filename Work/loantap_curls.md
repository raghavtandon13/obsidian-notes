# SALARIED

```json
curl -s -L -X POST 'https://prod.thearks.in/v1-application/transact' -H 'Content-Type: application/json' -H 'X-API-AUTH: X6NOFheJCHcIHwjwkvDd9w==' -H 'REQ-PRODUCT-ID: It-personal-term-loan-reducing' -H 'PARTNER-ID: creadmantra' --data-raw '{
    "add_application": {
        "job_type": "salaried",
        "full_name": "Abhijeet Rajendra Patait",
        "personal_email": "abhijeet@loantap.in",
        "mobile_number": "9999999999",
        "dob": "19761210",
        "gender": "male",
        "marital_status": "single",
        "home_ownership_type": "owned",
        "home_addr_line1": "1/12 Ashirwad Banglow",
        "home_addr_line2": "Centarl Avenue Road",
        "home_city": "Pune",
        "home_zipcode": "411003",
        "address_landmark": "Opposite ICICI Bank",
        "pan_card": "AHPPB3922J",
        "req_amount": "100000",
        "req_tenure": "12",
        "req_interest_rate": "22",
        "doc_combo": "sal_bs6",
        "loan_city": "pune",
        "fixed_income": "90000",
        "mothers_maiden_name": "Archana",
        "fathers_name": "Rajendra",
        "permanent_addr_line1": "1/12 Ashirwad Banglow",
        "permanent_addr_line2": "Centarl Avenue Road",
        "permanent_zipcode": "411003",
        "permanent_city": "Pune",
        "employer_name": "Loantap Finance Technology Pvt. Ltd.",
        "office_addr_line1": "Office No: 103, Hermes Waves",
        "office_addr_line2": "Central Avenue Road, Kalyaninagar",
        "office_city": "Pune",
        "office_zipcode": "411006",
        "official_email": "abhijeet@loantap.in",
        "emi_outflow": "5000",
        "rent_outflow": "0",
        "educational_qualification": "graduate",
        "no_of_dependents": 4,
        "total_work_experience": 4,
        "passport_number": "288898888",
        "aadhar_uid": "7729349876",
        "years_at_current_residence": "5",
        "employment_duration": "2",
        "office_landline_no": "022-3398773",
        "salary_account_no": "1021234569874",
        "salary_bank_name": "ICICI",
        "company_mca_id": "U 12345 DL 2020 PLC 098765",
        "cibil_active_id": "750",
        "ecs_bank_acc_no": "1021234569874",
        "ecs_bank_branch": "Pune",
        "ecs_bank": "ICICI",
        "ecs_cust_name": "Abhijeet Patait",
        "ecs_ifsc_code": "ICICI",
        "ecs_bank_city": "pune",
        "ecs_account_type": "saving",
        "ecs_micr_code": "478596998",
        "ongoing_loan": "yes",
        "is_consent": "cm12908094"
    }
}'
```

```json
{
  "add_application": {
    "question": {
      "job_type": "salaried",
      "full_name": "Abhijeet Rajendra Patait",
      "personal_email": "abhijeet@loantap.in",
      "mobile_number": "9999999999",
      "dob": "19761210",
      "gender": "male",
      "marital_status": "single",
      "home_ownership_type": "owned",
      "home_addr_line1": "1/12 Ashirwad Banglow",
      "home_addr_line2": "Centarl Avenue Road",
      "home_city": "Pune",
      "home_zipcode": "411003",
      "address_landmark": "Opposite ICICI Bank",
      "pan_card": "AHPPB3922J",
      "req_amount": "100000",
      "req_tenure": "12",
      "req_interest_rate": "22",
      "doc_combo": "sal_bs6",
      "loan_city": "pune",
      "fixed_income": "90000",
      "mothers_maiden_name": "Archana",
      "fathers_name": "Rajendra",
      "permanent_addr_line1": "1/12 Ashirwad Banglow",
      "permanent_addr_line2": "Centarl Avenue Road",
      "permanent_zipcode": "411003",
      "permanent_city": "Pune",
      "employer_name": "Loantap Finance Technology Pvt. Ltd.",
      "office_addr_line1": "Office No: 103, Hermes Waves",
      "office_addr_line2": "Central Avenue Road, Kalyaninagar",
      "office_city": "Pune",
      "office_zipcode": "411006",
      "official_email": "abhijeet@loantap.in",
      "emi_outflow": "5000",
      "rent_outflow": "0",
      "educational_qualification": "graduate",
      "no_of_dependents": 4,
      "total_work_experience": 4,
      "passport_number": "288898888",
      "aadhar_uid": "7729349876",
      "years_at_current_residence": "5",
      "employment_duration": "2",
      "office_landline_no": "022-3398773",
      "salary_account_no": "1021234569874",
      "salary_bank_name": "ICICI",
      "company_mca_id": "U 12345 DL 2020 PLC 098765",
      "cibil_active_id": "750",
      "ecs_bank_acc_no": "1021234569874",
      "ecs_bank_branch": "Pune",
      "ecs_bank": "ICICI",
      "ecs_cust_name": "Abhijeet Patait",
      "ecs_ifsc_code": "ICICI",
      "ecs_bank_city": "pune",
      "ecs_account_type": "saving",
      "ecs_micr_code": "478596998",
      "ongoing_loan": "yes",
      "is_consent": "cm12908094"
    },
    "answer": {
      "status": "success",
      "status_code": "200",
      "message": "Application created successfully",
      "data": {
        "lapp_id": "APP1800207685049151",
        "link": "https://prod.thearks.in/apply/home/APP1800207685049151"
      },
      "soft_eligibililty": {
        "status": "fail",
        "message": "Soft eligibility has failed.",
        "reason": "{\"status\":\"error\",\"message\":\"Something went wrong\",\"reason\":\"Loan City is invalid\",\"no_offers_id\":\"\"}"
      }
    }
  }
}
```

# SELF-EMPLOYED

```json
curl -s -L -X POST 'https://prod.thearks.in/v1-application/transact' -H 'Content-Type: application/json' -H 'X-API-AUTH: X6NOFheJCHcIHwjwkvDd9w==' -H 'REQ-PRODUCT-ID: It-personal-term-loan-reducing' -H 'PARTNER-ID: creadmantra' --data-raw '{
    "add_application": {
        "job_type": "self-employed",
        "full_name": "PRADEEP KUMAR SHARMA",
        "personal_email": "sharmaji9452@gmail.com",
        "mobile_number": "7007025097",
        "dob": "19971015",
        "gender": "Male",
        "business_addr_line1": "JEEVAN JAGRITI SEVA SANSTHAN BHOPATPUR",
        "business_city": "Phulpur-Prayagraj",
        "business_zipcode": "221507",
        "pan_card": "EFKPS8730A",
        "req_amount": 700000.0,
        "req_tenure": "60",
        "loan_city": "allahabad",
        "fathers_name": "SHIV PRASAD SHARMA",
        "permanent_addr_line1": "S/O Shiv Prasad Sharma, ., Gram- Bhopatpur, ., Thana- Tharwai , Block- Bahadurpur, Sahson, 221507, Sahson, Phulpur, Allahabad, Uttar Pradesh, India",
        "permanent_zipcode": "221507",
        "permanent_city": "Phulpur-Prayagraj",
        "ecs_bank_acc_no": "50200038230940",
        "ecs_bank": "HDFC BANK",
        "ecs_cust_name": "PRADEEP KUMAR SHARMA",
        "ecs_ifsc_code": "HDFC0002434",
        "ecs_account_type": "saving",
        "business_name": "JEEVAN JAGRITI SEVA KENDRA",
        "is_consent": "cm12908095"
    }
}'
```

```json
{
  "add_application": {
    "question": {
      "job_type": "self-employed",
      "full_name": "PRADEEP KUMAR SHARMA",
      "personal_email": "sharmaji9452@gmail.com",
      "mobile_number": "7007025097",
      "dob": "19971015",
      "gender": "Male",
      "business_addr_line1": "JEEVAN JAGRITI SEVA SANSTHAN BHOPATPUR",
      "business_city": "Phulpur-Prayagraj",
      "business_zipcode": "221507",
      "pan_card": "EFKPS8730A",
      "req_amount": 700000,
      "req_tenure": "60",
      "loan_city": "allahabad",
      "fathers_name": "SHIV PRASAD SHARMA",
      "permanent_addr_line1": "S/O Shiv Prasad Sharma, ., Gram- Bhopatpur, ., Thana- Tharwai , Block- Bahadurpur, Sahson, 221507, Sahson, Phulpur, Allahabad, Uttar Pradesh, India",
      "permanent_zipcode": "221507",
      "permanent_city": "Phulpur-Prayagraj",
      "ecs_bank_acc_no": "50200038230940",
      "ecs_bank": "HDFC BANK",
      "ecs_cust_name": "PRADEEP KUMAR SHARMA",
      "ecs_ifsc_code": "HDFC0002434",
      "ecs_account_type": "saving",
      "business_name": "JEEVAN JAGRITI SEVA KENDRA",
      "is_consent": "cm12908095"
    },
    "answer": {
      "status": "success",
      "status_code": "200",
      "message": "Application created successfully",
      "data": {
        "lapp_id": "APP1800207772055272",
        "link": "https://prod.thearks.in/apply/home/APP1800207772055272"
      },
      "soft_eligibililty": {
        "status": "fail",
        "message": "Soft eligibility has failed.",
        "reason": "{\"status\":\"error\",\"message\":\"Something went wrong\",\"reason\":\"Loan City is invalid\",\"no_offers_id\":\"\"}"
      }
    }
  }
}
```

# Salaried Short json

```sh
curl --request POST \
--url https://loantap.in/v1-application/transact \
--header 'PARTNER-ID: creadmantra' \
--header 'REQ-PRODUCT-ID: It-personal-term-loan-reducing' \
--header 'X-API-AUTH: aF/wW6yCCyPNzhaM0qCOTA==' \
--header 'content-type: application/json' \
--data '{
"add_application": {
"job_type": "salaried",
"full_name": "Vikaram Paliwal",
"personal_email": "vikkypal@gamil.com",
"mobile_number": "8080912368",
"dob": "19861229",
"gender": "male",
"marital_status": "single",
"home_city": "Mumbai",
"home_zipcode": "400003",
"pan_card": "BUQPT0232L",
"req_amount": "100000",
"req_tenure": "12",
"req_interest_rate": "22",
"loan_city": "mumbai",
"fixed_income": "90000",
"permanent_zipcode": "400001",
"permanent_city": "Mumbai",
"employer_name": "Om Hotel",
"office_city": "Pune",
"office_zipcode": "400001",
"official_email": "vikkypal@gamil.com",
"is_consent": "12937098"
}
}'
```

```json
{
  "add_application": {
    "question": {
      "job_type": "salaried",
      "full_name": "Vikaram Paliwal",
      "personal_email": "vikkypal@gamil.com",
      "mobile_number": "8080912368",
      "dob": "19861229",
      "gender": "male",
      "marital_status": "single",
      "home_city": "Mumbai",
      "home_zipcode": "400003",
      "pan_card": "BUQPT0232L",
      "req_amount": "100000",
      "req_tenure": "12",
      "req_interest_rate": "22",
      "loan_city": "mumbai",
      "fixed_income": "90000",
      "permanent_zipcode": "400001",
      "permanent_city": "Mumbai",
      "employer_name": "Om Hotel",
      "office_city": "Pune",
      "office_zipcode": "400001",
      "official_email": "vikkypal@gamil.com",
      "is_consent": "12937098"
    },
    "answer": {
      "status": "success",
      "status_code": "200",
      "message": "Application created successfully",
      "data": {
        "lapp_id": "APP1800370656748360",
        "link": "https://loantap.in/apply/home/APP1800370656748360"
      }
    }
  }
}
```






curl --request POST \
--url https://loantap.in/v1-application/transact \
--header 'PARTNER-ID: creadmantra' \
--header 'REQ-PRODUCT-ID: It-personal-term-loan-reducing' \
--header 'X-API-AUTH: obqY9Jl+lhPL8UnJx3mTJg==' \
--header 'content-type: application/json' \
--data '{
"add_application": {
"job_type": "salaried",
"full_name": "Vikaram Paliwal",
"personal_email": "vikkypal@gamil.com",
"mobile_number": "8080912368",
"dob": "19861229",
"gender": "male",
"marital_status": "single",
"home_city": "Mumbai",
"home_zipcode": "400003",
"pan_card": "BUQPT0232L",
"req_amount": "100000",
"req_tenure": "12",
"req_interest_rate": "22",
"loan_city": "mumbai",
"fixed_income": "90000",
"permanent_zipcode": "400001",
"permanent_city": "Mumbai",
"employer_name": "Om Hotel",
"office_city": "Pune",
"office_zipcode": "400001",
"official_email": "vikkypal@gamil.com",
"is_consent": "12937098"
}
}'

