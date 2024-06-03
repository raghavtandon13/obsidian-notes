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
        employemnet_status:"",
        loan_amount:""
}
```
```
https://credmantra.com/api/v1/partner-api/faircent/register
```
If successful take ```loan_id``` and ```customer_id``` for result.
<div style="page-break-after: always;"></div>

3. **Document Upload API** -
**FORMDATA**

| KEY      | VALUE                       |
| -------- | --------------------------- |
| docImage | //image here                |
| loan_id  | from Register API ressponse |
| token    | from Register API ressponse |
```
https://credmantra.com/api/v1/partner-api/faircent/upload
```