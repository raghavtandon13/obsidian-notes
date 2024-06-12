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

---

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

---



3. **Cibil API** -
```json
{
        address: "address city state",
        dob: "yyyy-mm-dd",
        email: "email@email.com",
        first_name: "firstName",
        gender: "Male", // "Female"
        last_name: "lastName",
        pan_card_number: "ABCDEXXXXF",
        phone_number: "9876543210",
        pin_code: "110011",
        token: "token", // from REGISTER api
}
```
```
https://credmantra.com/api/v1/partner-api/payme/cibil
```

---

4. **Limit API** -
```json
{
            phone_number: "9876543210",
            token: "token", // from REGISTER api
}
```
```
https://credmantra.com/api/v1/partner-api/payme/limit
```

---
