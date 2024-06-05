1. **Dedupe API** -
```json
{
        mobileNumber: //phone,
        panNumber: //pan,
        personalEmailId: //email,
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
https://credmantra.com/api/v1/partner-api/upwards/create
```
If successful take ```loan_id``` and ```customer_id``` for result.
<div style="page-break-after: always;"></div>

3. **Complete API** -
```json
{
	loan_id: "from prev result",
    customer_id: "from prev result"
}
```
```
https://credmantra.com/api/v1/partner-api/upwards/complete
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