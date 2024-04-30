---
id: Leads API Docs
aliases: []
tags: []
---


# **Basic Payload Structure**
```json
{
    "lead": {
        "phone": "9793586735",
        "firstName": "anoop",
        "lastName": "pal",
        "dob": "1998-03-11",
        "email": "anooppal19793@gmaik.com",
        "gender": "MALE",
        "city": "NEW DELHI",
        "state": "DELHI",
        "pincode": "110005",
        "pan": "EVUPP4678E",
        "empName": "NULL",
        "salary": "20833"
    }
}
```

<div style="page-break-after: always;"></div>

## **example**

```bash
curl -s -L 'http://localhost:3000/api/v1/leads/inject'
-H 'x-api-key: vs65Cu06K1GB2qSdJejP'
-H 'Content-Type: application/json'
--data-raw '{
    "lead": {
        "phone": "9460646842",
        "firstName": "Hari",
        "lastName": "Taroliya",
        "dob": "1993-01-15",
        "email": "harisinghtaroliya57@gmail.com",
        "gender": "MALE",
        "city": "Gurgaon",
        "state": "HARYANA",
        "pincode": "122010",
        "pan": "AXNPT8654K",
        "empName": "MOBIHUB REFURB INTERNATIONAL",
        "salary": "78040"
    }
}' | jq
```
<div style="page-break-after: always;"></div>


```bash
curl -s -L 'https://credmantra.com/api/v1/leads/inject' -H 'x-api-key: vs65Cu06K1GB2qSdJejP' -H 'Content-Type: application/json' --data-raw '{"lead": {"phone": "9460646842", "firstName": "Hari", "lastName": "Taroliya", "dob": "1993-01-15", "email": "harisinghtaroliya57@gmail.com", "gender": "MALE", "city": "Gurgaon", "state": "HARYANA", "pincode": "122010", "pan": "AXNPT8654K", "empName": "MOBIHUB REFURB INTERNATIONAL", "salary": "78040"}}' | jq
```

```json
[
  {
    "_id": "660ce42631720cd8144ec0c8",
    "name": "SOLLETI THEJA",
    "phone": "7981590409",
    "accounts": [],
    "role": "USER",
    "pan": "GVUPS0734J",
    "dob": "1992-06-26",
    "email": "sbrteja@gmail.com",
    "city": "Cuddapah",
    "state": "Andhra Pradesh",
    "gender": "MALE",
    "employment": "Salaried",
    "income": "85000",
    "partner": "MoneyTap",
    "pincode": "516227",
    "detailsFilled": false,
    "eformFilled": false,
    "createdAt": "2024-04-03T05:07:50.785Z",
    "updatedAt": "2024-04-03T05:07:50.785Z",
    "__v": 0
  },
```

