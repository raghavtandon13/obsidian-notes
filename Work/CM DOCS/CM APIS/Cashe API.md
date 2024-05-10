# Stage 1 - Dedupe Check
```json
    {
        partner_name: "CredMantra_Partner1", // DO NOT CHNAGE
        mobile_no: "8094634634", 
        email_id: "ragahv@credmantra.com",
    };
```

```
https://credmantra.com/api/v1/partner-api/cashe/checkDuplicateLead
```
 If  ```Payload  === "NO" ``` then move to stage 2 else show "**Customer Already Registered with Cashe**"
 
 ----
# Stage 2 - PreApproval
```json
    {
            partner_name: "CredMantra_Partner1",
            pan: "BUSPT0022l",
            mobileNo: "8094634634",
            name: "firstname lastname"
            addressLine1: "addressLine1",
            locality: "locality",
            pinCode: "101010",
            gender: "M"/"F"
            salary: 50000
            state: "DELHI"
            city: "Delhi"
            dob: "1998-10-10 00:00:00",
            employmentType: 1,
            salaryReceivedType: 3,
            emailId: "email@gmail.com",
            companyName: "company",
            loanAmount: 200000,
        };
```

```
https://credmantra.com/api/v1/partner-api/cashe/preApproval
```
 
 If  ```message === "Success" ``` then move to stage 3 else show recieved error.

----

# Stage 3 - Create Customer

> USER will not fill this form, this form is exactly  the same as previous, when user clicks on "Apply " after stage 2 this form should automatically be sent to the 

```json
{
                partner_name: "CredMantra_Partner1",
                "Personal Information": {
                    "First Name": lead.firstName,
                    Gender: lead.gender[0].toUpperCase() + lead.gender.slice(1).toLowerCase(),
                    "Address Line 1": casheReq.addressLine1,
                    Pincode: casheReq.pinCode,
                    City: casheReq.city,
                    State: casheReq.state,
                    PAN: casheReq.pan,
                },
                "Applicant Information": {
                    "Company Name": casheReq.companyName || "OTHERS",
                    "Monthly Income": casheReq.salary,
                    "Employment Type": "Salaried full-time",
                    SalaryReceivedTypeId: casheReq.salaryReceivedType,
                },
                "Contact Information": {
                    Mobile: casheReq.mobileNo,
                    "Email Id": casheReq.emailId,
                },
            }
```

```
https://credmantra.com/api/v1/partner-api/cashe/createCustomer
```
 If  ```Payload  === "NO" ``` then move to stage 2 else show "**Customer Already Registered with Cashe**"