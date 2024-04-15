**DeDupe API-**  
req-  

{  
"partner_name": "CredMantra_Partner1",  
"mobile_no": 8094634634,  
"email_id": "  
131415wow@gmail.com"  
}  

res-

{  
"status": "OK",  
"message": "NO",  
"payLoad": "NO",  
"statusCode": 200,  
"duplicateStatusCode": 1  
}  

**preApproval API-**

req-

{  
"partner_name": "CredMantra_Partner1",  
"gender": "M",  
"name": "himanshu singh",  
"dob": "1999-10-12 00:00:00",  
"pan": "BUSCM4562P",  
"mobileNo": 7229970843,  
"state": "DELHI",  
"addressLine1": "1501 outram lane gtb nagar",  
"locality": "gtb nagar",  
"pinCode": 110009,  
"city": "delhi",  
"employmentType": 1,  
"salaryReceivedType": 1,  
"emailId": "  
hemusingh@gmail.com",  
"companyName": "bajaj",  
"salary": 45000,  
"loanAmount": 60000  
}  

res-  
  

{  
"status": "OK",  
"message": "Success",  
"payLoad": {  
"amount": null,  
"status": "rejected"  
},  
"statusCode": 200  
}