1. **Dedupe API** -
```json
{
        mobileNumber: "", //phone,
        panNumber: "", //pan,
        personalEmailId: "", //email,
        productName: "pl",
    }
```
```
https://credmantra.com/api/api/v1/partner-api/zype/dedupe
```
If ```status === "ACCEPT"``` move forward
2. **Offer API** -
```json
{
            mobileNumber: "12345678",
            email: "email@email.com",
            panNumber: "ABCDEXXXXL",
            name: "full name",
            dob: "YYYY-MM-DD",
            employmentType: "", //‘salaried’ or ‘selfemployed’
            income: 90000, // Number
            orgName: "my company",
            bureauType: 3, // fixed value
}
```
```
https://credmantra.com/api/v1/partner-api/zype/offer
```