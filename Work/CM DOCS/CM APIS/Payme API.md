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
If `````` move forward
<div style="page-break-after: always;"></div>

3. **Details API** -
```json
{
                loanId: "", //from start api response
                firstName: "",
                lastName: "",
                personalEmailId: "",
                gender: "Male", // "Female"
                dob: "28/10/1998", // dd/mm/yyyy
                panNumber: "",
                employmentType: "salaried",
                desiredLoanAmount: 150000, // Number
                netMonthlyIncome: 50000, // Number
                currentAddressPincode: "110009",
                currentAddress: "address 1",
}
```
```
https://credmantra.com/api/v1/partner-api/prefr/details
```