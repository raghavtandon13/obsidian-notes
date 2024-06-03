1. **Dedupe API** -
```json
{
        mobile_number: "8094634634"
        social_email_id: "abc@xyz.com",
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
        first_name: "",
        last_name: "",
        pan: "",
        dob: 1988-12-29,
        gender: "male/female",
        social_email_id: "",
        mobile_number1: "9999999999",
        current_pincode: "121212",
        current_city: "",
        current_state: "",
        company: "company",
        employment_status_id: 3, // check below
        profession_type_id: 21, // check below
        salary_payment_mode_id: 2, // check below
        salary: 75000, //integer
        consent: true,
}
```
```
https://credmantra.com/api/v1/partner-api/faircent/register
```
If successful take ```loan_id``` and ```customer_id``` for result.
<div style="page-break-after: always;"></div>

3. **Document Upload API** -

| KEY      | VALUE                        |
| -------- | --------------------------- |
| docImage | //image he                e  |
| loan_id from Register API ressponse PI  |
```
https://credmantra.com/api/v1/partner-api/faircent/upload
```