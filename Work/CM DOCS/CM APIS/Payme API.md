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
If ```duplicateFound === false``` move forward

2. **START API** -
```json
{
	mobileNo: //phone
}
```
```
https://credmantra.com/api/v1/partner-api/prefr/start2
```
If successful take ```loan_id``` and ```customer_id``` for result.
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