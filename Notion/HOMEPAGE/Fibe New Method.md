# form Data

```JavaScript
formData: any = {
    mobilenumber: '',
    firstname: '',
    lastname: '',
    dob: '',
    profile: {
      profession: '',
      address1: '',
      address2: '',
      landmark: '',
      city: '',
      pincode: '',
      maritalstatus: '',
    },
    finance: {
      pan: '',
    },
    employeedetails: {
      employername: '',
      officeaddress: '',
      officeCity: '',
      officepincode: '',
      salary: '',
    },
    consent: false,
    consentDatetime: '',
  };
```

  

# form field

```JavaScript
formFields: { label: string; name: string; type: string; group: string }[] = [
    { label: 'Mobile Number', name: 'mobilenumber', type: 'number', group: '' },
    { label: 'First Name', name: 'firstname', type: 'text', group: '' },
    { label: 'Last Name', name: 'lastname', type: 'text', group: '' },
    { label: 'Date of Birth', name: 'dob', type: 'date', group: '' },

    { label: 'City', name: 'city', type: 'text', group: 'profile' },
    { label: 'Profession', name: 'profession', type: 'text', group: 'profile' },
    { label: 'Address Line 1', name: 'address1', type: 'text', group: 'profile' },
    { label: 'Address Line 2', name: 'address2', type: 'text', group: 'profile' },
    { label: 'Landmark', name: 'landmark', type: 'text', group: 'profile' },
    { label: 'Pincode', name: 'pincode', type: 'text', group: 'profile' },
    { label: 'Marital Status', name: 'maritalstatus', type: 'text', group: 'profile' },

    { label: 'PAN', name: 'pan', type: 'text', group: 'finance' },

    { label: 'Employer Name', name: 'employername', type: 'text', group: 'employeedetails' },
    { label: 'Office Address', name: 'officeaddress', type: 'text', group: 'employeedetails' },
    { label: 'Office City', name: 'officeCity', type: 'text', group: 'employeedetails' },
    { label: 'Office Pincode', name: 'officepincode', type: 'text', group: 'employeedetails' },
    { label: 'Salary', name: 'salary', type: 'number', group: 'employeedetails' },

    { label: 'Consent', name: 'consent', type: 'checkbox', group: '' },
    { label: 'Consent Date and Time', name: 'consentDatetime', type: 'datetime', group: '' },
  ];
```