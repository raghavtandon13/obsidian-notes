# 1. Register User
```bash
curl -L -X POST 'https://weedori.paymeindia.in/api/authentication/register_user_merchant/' -H 'Content-Type: application/json' --data-raw '{
  "email": "cmtestuser@gmail.com",
  "merchant_id": "98cdbb76-30c2-4bc8-9656-774350eabe8d",
  "phone_number": "8096656656",
  "full_name": "Rahul Mehta"
}'
```

```json
{"message":"Signed-in Successfully","data":{"refresh":"eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTcxNDg4ODY5NywianRpIjoiZjI3ZTlmZDUwM2ZmNDlmMTgzYzk2MWQ1NWQ0ZDc0NDciLCJlbWFpbCI6ImNtdGVzdHVzZXJAZ21haWwuY29tIn0.pXfVWUnHl0d-Q1xH9JNCiAz7F5H_jJ00TBV5LQiCz3I","token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNzE0NjM2Njk3LCJqdGkiOiIwNjBlYmNlMTBlNGE0ODU2YjIyMDY0ODMwYzgwOTM4OSIsImVtYWlsIjoiY210ZXN0dXNlckBnbWFpbC5jb20ifQ.-WxlfvvlCaOoKzZgXWs_znyBnPOZ8DonbeM1OvFoNOI"},"user_id":5556932}%
```


# 0. Check USER
```bash
 curl -L -X POST 'https://weedori.paymeindia.in/api/authentication/check_user_merchant' -H 'Content-Type: application/json' --data-raw '{
    "merchant_id": "98cdbb76-30c2-4bc8-9656-774350eabe8d",
    "pan_card_number": "BHNPC2752A",
    "email": "string@gmail.com",
    "phone_number": "+919818241609"
}'
```

```json
{"message":"Authenticate Api Stucked into exception!!","error":"phone_number required !!"}%
```


# 3. Check USER
```bash
 curl -L -X POST 'https://weedori.paymeindia.in/api/authentication/check_user_merchant' -H 'Content-Type: application/json' --data-raw '{
    "merchant_id": "98cdbb76-30c2-4bc8-9656-774350eabe8d",
    "pan_card_number": "BHNPC2752A",
    "email": "string@gmail.com",
    "phone_number": "+919818241609"
}'
```

```json
{"message":"Authenticate Api Stucked into exception!!","error":"phone_number required !!"}%
```


