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