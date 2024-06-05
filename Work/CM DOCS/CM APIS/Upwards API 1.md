1. **Dedupe API** -
```json
{
        mobileNumber: "" //phone,
        panNumber: "" //pan,
        personalEmailId: "" //email,
        productName: "pl",
    }
```
```
https://credmantra.com/api/v1/partner-api/prefr/dedupe
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
                currentAddressPincode: "110",
                currentAddress: "address 1",
}
```
```
https://credmantra.com/api/v1/partner-api/prefr/details
```
if prev is successful then ->
4. **Decision API** -
```json
{
	loan_id: "from prev result",
    customer_id: "from prev result"
}
```
```
https://credmantra.com/api/v1/partner-api/upwards/decision
```
5.  **Transition API** - 
Finally show button "Go to UPWARDS" and redirect to transition url.
```json
{
	loan_id: "from prev result",
    customer_id: "from prev result"
}
```
```
https://credmantra.com/api/v1/partner-api/upwards/transition
```


![[Pasted image 20240515141624.png]]
![[Pasted image 20240515141652.png]]