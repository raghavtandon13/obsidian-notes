1. **Dedupe API** -
```json
{
        mobile: "8094634634"
        email: "abc@xyz.com",
        pan: "XXXXX0000X",
}
```
```
https://credmantra.com/api/v1/partner-api/faircent/dedupe
```
If ```is_eligible === true``` move forward

2. **Register API** -
```json
 {
        fname: "",
        lname: "",
        dob: 1988-12-29,
        gender: "",
        pan: "",
        mobile: "9999999999",
        gender: "M/F",
        email: "",
        address:"",
        locality:"",
        pin:"",
        city:"",
        state:"",
        monthly_income:"",
        employemnet_status:"", //['Salaried', 'Self Employed'];
        loan_amount:""
        //--------
        // Below details are same for every request
	    "consent": 'Y',
        "tnc_link": 'https://www.faircent.in/terms-conditions',
        "sign_ip": '122.161.8.133',
        "sign_time": 1234567890,
        "loan_purpose": 1364,

}
```
```
https://credmantra.com/api/v1/partner-api/faircent/register
```
If successful take ```loan_id``` and ```customer_id``` for result.
<div style="page-break-after: always;"></div>

3. **Document Upload API** -
**FORMDATA**
IF 

| KEY      | VALUE                           |
| -------- | ------------------------------- |
| docImage | //image here                    |
| loan_id  | from Register API ressponse     |
| token    | from Register API ressponse     |
| type     | AADHAAR/BANK_STATEMENT/PANCARD/ |
```
https://credmantra.com/api/v1/partner-api/faircent/upload
```