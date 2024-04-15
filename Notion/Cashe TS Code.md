```TypeScript
import { Component, OnInit, ViewEncapsulation } from '@angular/core';
import { MenuItem } from 'primeng/api';
import { HttpClient } from '@angular/common/http';

@Component({
  selector: 'app-cashe-page',
  templateUrl: './cashe-page.component.html',
  styleUrl: './cashe-page.component.css',
  encapsulation: ViewEncapsulation.None,
})
export class CashePageComponent implements OnInit {
  panRegex = "[A-Z]{5}[0-9]{4}[A-Z]{1}";
  activeIndex = 0;
  steps: MenuItem[] = [];

  genders = [
    { name: 'Male', value: 'male' },
    { name: 'Female', value: 'female' },
  ];

  formFields: { label: string; name: string; type: string }[] = [
    { label: 'Name', name: 'name', type: 'text' },
    { label: 'Date of Birth', name: 'dob', type: 'date' },
    { label: 'Gender', name: 'gender', type: 'text' },
    { label: 'PAN', name: 'pan', type: 'text' },
    { label: 'Mobile Number', name: 'mobile', type: 'tel' },
    { label: 'Address Line 1', name: 'addressLine1', type: 'text' },
    { label: 'Locality', name: 'locality', type: 'text' },
    { label: 'Pincode', name: 'pincode', type: 'text' },
    { label: 'State', name: 'state', type: 'text' },
    { label: 'City', name: 'city', type: 'text' },
    { label: 'Salary', name: 'salary', type: 'number' },
    { label: 'Employment Type', name: 'employmentType', type: 'text' },
    { label: 'Salary Received Type', name: 'salaryReceivedType', type: 'text' },
    { label: 'Email ID', name: 'email', type: 'email' },
    { label: 'Company Name', name: 'companyName', type: 'text' },
    { label: 'Loan Amount', name: 'loanAmount', type: 'number' },
  ];

  formData: any = {};

  constructor(private http: HttpClient) {}

  ngOnInit() {
    this.steps = [{ label: 'Personal Details' }, { label: 'Address' }, { label: 'Employment Details' }, { label: 'Loan Details' }];
  }

  next() {
    this.activeIndex++;
  }

  prev() {
    this.activeIndex--;
  }

  submit() {
    this.http.post('https://jsonplaceholder.typicode.com/posts', this.formData).subscribe((response) => {
      console.log('API Response:', response);
    });
  }
}
```

  

# Next button

```JavaScript
[hidden]="activeIndex == steps.length - 1"
[disabled]="activeIndex === steps.length - 1 || !stepperForm.form.valid"
```

# Submit Button

```JavaScript
[hidden]="activeIndex !== steps.length - 1"
[disabled]="!checked || !stepperForm.form.valid"
```