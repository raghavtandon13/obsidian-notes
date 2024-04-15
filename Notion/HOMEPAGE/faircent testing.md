```Go
sent-
{
    "consent": "Y",
    "tnc_link": "https://www.faircent.in/terms-conditions",
    "gender": "M",
    "fname": "raghav",
    "lname": "tandon",
    "dob": "1999-09-13",
    "pan": "BUSPM0452L",
    "mobile": 8094634635,
    "state": "DELHI",
    "address": "adr2222",
    "locality": "delhi",
    "pin": 110009,
    "city": "delhi",
    "employment_status": "Salaried",
    "mail": "raghavtandon14@gmail.com",
    "monthly_income": 55000,
    "loan_purpose": 1364,
    "loan_amount": 45000,
    "sign_ip": "122.161.8.133",
    "sign_time": 1234567890
}
```

  

```Go
{
    "message": "Account Created Successfully!",
    "success": true,
    "result": {
        "loan_id": 1004198451,
        "uid": 1000000645,
        "status": "REJECTED",
        "msg": "No ENV Found!!",
        "user_type": "NEW",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHBpcmVkQXQiOjMzMjA5NzY4NzI2MTA3LCJ1aWQiOiIxMDAwMDAwNjQ1IiwiaWF0IjoxNzA1MzA0NzI2fQ.e2s_7jFgFHQqG4spQdeRQXw5jfekaHd6HntwklmbSXQ"
    },
    "count": 0
}


{
    "message": "PAN Already Exists",
    "success": false,
    "result": "",
    "count": 0
}
```

# dedupe

```Go
{
    "pan": "PRPPK6963H",
    "mobile": "8292484663",
    "email": "gurmeetsingh458@gmail.com"
}
```

```Go
{
    "message": "Sucessfully Fetched The Data",
    "success": true,
    "result": {
        "status": true,
        "message": "No Duplicate Record Found."
    },
    "count": 0
}
```