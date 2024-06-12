1. **Dedupe API** -
```json
{
        pan_card_number: "ABCDEXXXXF",
        email: "email@email.com",
        phone_number: "9876543210",
}
```
```
https://credmantra.com/api/v1/partner-api/payme/dedupe
```
If ```message = "user_not_found"``` move forward

2. **REGISTER API** -
```json
{
        email: "email@email.com",
        phone_number: "9876543210",
        full_name: "firstName lastName"
}
```
```
https://credmantra.com/api/v1/partner-api/payme/register
```
If ```message = "Signed-in Successfully"``` move forward
<div style="page-break-after: always;"></div>

3. **Details API** -
```json
{
        address: lead.city + " " + lead.state,
        dob: lead.dob,
        email: lead.email,
        first_name: lead.firstName,
        gender: lead.gender[0].toUpperCase() + lead.gender.slice(1).toLowerCase(),
        last_name: lead.lastName,
        pan_card_number: lead.pan,
        phone_number: lead.phone,
        pin_code: lead.pincode,
        token: p2Res.data.data.token,
    }
```
```
https://credmantra.com/api/v1/partner-api/prefr/details
```