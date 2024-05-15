1. **Dedupe API** -
```json
{
        mobile_number: "8094634634"
        social_email_id: "abc@xyz.com",
        pan: "XXXXX0000X",
}
```
```
https://credmantra.com/api/v1/partner-api/upwards/eligibility
```
If ```is_eligible === true``` move forward

1. **Create API** -
```json
 {
        first_name: lead.firstName,
        last_name: lead.lastName,
        pan: lead.pan,
        dob: lead.dob,
        gender: lead.gender.toLowerCase(),
        social_email_id: lead.email,
        mobile_number1: lead.phone.toString(),
        current_pincode: lead.pincode.toString(),
        current_city: lead.city,
        current_state: lead.state,
        company: lead.empName || "company",
        employment_status_id: 3,
        profession_type_id: 21,
        salary_payment_mode_id: 2,
        salary: parseInt(lead.salary),
        consent: true,
}
```