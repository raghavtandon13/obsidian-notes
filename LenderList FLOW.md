**GET REQ**
**Header** : Authorization: Bearer token (saved in local storage)
```
https://credmantra.com/api/v1/auth/verify-user
```
If user has ```eformFilled === false``` then show form to eligibility form to user.
If user has ```eformFilled === true``` then move on to lender list.

**POST REQ**
```
https://credmantra.com/api/v1/auth/eli
```
**BODY**
```
    {
        name: '',
        email: '',
        phone: '',
        dob: '',
        employmentType: '',
        ammount: '',
        income: '',
        pincode: '',
    };

```