#
```bash
curl -L -X POST 'https://growth-01.stg.whizdm.com/atlas/v1/token' -H 'Content-Type: application/json' -d '{
∙ "partnerCode": 172,
∙ "userName": "credmantra",
∙ "password": "mN*y4jsD3,"
∙ }'
```
```bash
{"status":"success","message":"success","token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJBVExBUyIsInN1YiI6IjhhODM4NTFlOGU5YjdkODUwMThlOWQ3MTE4NDgxZDNkIiwiaWF0IjoxNzEzOTU1OTAzLCJleHAiOjE3MTQwNDIzMDMsInBhcnRuZXJJZCI6IjI1OCJ9.kCuVKCUlUuKS_2ArMCUwj7Q7TXPDaGCPOaZyMMoexrs","ttl":0}
```
## 2nd
```bash
curl -L -X POST 'https://growth-01.stg.whizdm.com/atlas/v1/lead' -H 'Content-Type: application/json' -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJBVExBUyIsInN1YiI6IjhhODM4NTFlOGU5YjdkODUwMThlOWQ3MTE4NDgxZDNkIiwiaWF0IjoxNzEzOTU1OTAzLCJleHAiOjE3MTQwNDIzMDMsInBhcnRuZXJJZCI6IjI1OCJ9.kCuVKCUlUuKS_2ArMCUwj7Q7TXPDaGCPOaZyMMoexrs' --data-raw '{
∙    "partnerCode": 172,
∙    "partnerRef": "cm_9985718",
∙    "name": "FirstName LastName",
∙    "phone": "9999999999",
∙    "pan": "TESPJ8613G",
∙    "dateOfBirth": "1988-05-03",
∙    "bureauPermission": true,
∙    "addressList": [
∙        {
∙            "pincode": "560102",
∙            "residenceType": "rented",
∙            "addressType": "current"
∙        },
∙        {
∙            "pincode": "560103",
∙            "residenceType": "rented",
∙            "addressType": "work"
∙        }
∙    ],
∙    "declaredIncome": 80000,
∙    "employmentType": "salaried",
∙    "incomeMode": "online",
∙    "emailList": [
∙        {
∙            "email": "sri.test@gmail.com",
∙            "type": "primary_device"
∙        }
∙    ]
∙ }'
```
```bash
{"status":"success","message":"success","leadId":"8a8385368ef2a9a3018f0fd767bd5b99"}
```
## 3rd
```bash
curl -L -X GET 'https://growth-01.stg.whizdm.com/atlas/v1/lead/status/8a8385368ef2a9a3018f0fd767bd5b99' -H 'token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJBVExBUyIsInN1YiI6IjhhODM4NTFlOGU5YjdkODUwMThlOWQ3MTE4NDgxZDNkIiwiaWF0IjoxNzEzOTU1OTAzLCJleHAiOjE3MTQwNDIzMDMsInBhcnRuZXJJZCI6IjI1OCJ9.kCuVKCUlUuKS_2ArMCUwj7Q7TXPDaGCPOaZyMMoexrs'
```
```bash
{"status":"success","message":"success","loanStatus":"created","leadStatus":"created"}
```
## 4th
```bash
curl -L -X GET 'https://growth-01.stg.whizdm.com/atlas/v1/offers/8a8385368ef2a9a3018f0fd767bd5b99' -H 'token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJBVExBUyIsInN1YiI6IjhhODM4NTFlOGU5YjdkODUwMThlOWQ3MTE4NDgxZDNkIiwiaWF0IjoxNzEzOTU1OTAzLCJleHAiOjE3MTQwNDIzMDMsInBhcnRuZXJJZCI6IjI1OCJ9.kCuVKCUlUuKS_2ArMCUwj7Q7TXPDaGCPOaZyMMoexrs'
```
```bash
{"status":"failure","code":"8011","message":"Please retry to get offers"}
```