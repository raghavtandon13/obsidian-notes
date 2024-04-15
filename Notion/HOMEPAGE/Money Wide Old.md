# HTML

```JavaScript
<app-navbar></app-navbar>
<div class="fibe-title">
  <h1>Connect with Money Wide</h1>
</div>
<div class="form-container">
  <form [formGroup]="myForm" (submit)="onSubmit()">
    <!-- UTM Source -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>UTM Source</mat-label>
      <input matInput formControlName="utm_source" />
    </mat-form-field>

    <!-- UTM Medium -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>UTM Medium</mat-label>
      <input matInput formControlName="utm_medium" />
    </mat-form-field>

    <!-- UTM Campaign -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>UTM Campaign</mat-label>
      <input matInput formControlName="utm_campaign" />
    </mat-form-field>

    <!-- Occupation Type -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Occupation Type</mat-label>
      <input matInput formControlName="occupation_type" type="number" />
    </mat-form-field>

    <!-- Phone Number -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Phone Number</mat-label>
      <input matInput formControlName="phone_no" type="number" />
    </mat-form-field>

    <!-- Pincode -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Pincode</mat-label>
      <input matInput formControlName="pincode" type="number" />
    </mat-form-field>

    <!-- City Name -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>City Name</mat-label>
      <input matInput formControlName="city_name" />
    </mat-form-field>

    <!-- PAN -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>PAN</mat-label>
      <input matInput formControlName="pan" />
    </mat-form-field>

    <!-- Email -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Email</mat-label>
      <input matInput formControlName="email" type="email" />
    </mat-form-field>

    <!-- Marital Status -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Marital Status</mat-label>
      <input matInput formControlName="marital_status" />
    </mat-form-field>

    <!-- Residence Type -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Residence Type</mat-label>
      <input matInput formControlName="residence_type" />
    </mat-form-field>

    <!-- Net Monthly Income -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Net Monthly Income</mat-label>
      <input matInput formControlName="net_monthly_incm" type="number" />
    </mat-form-field>

    <!-- Employer Type -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Employer Type</mat-label>
      <input matInput formControlName="employer_type" type="number" />
    </mat-form-field>

    <!-- Mode of Salary -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Mode of Salary</mat-label>
      <input matInput formControlName="mode_of_salary" type="number" />
    </mat-form-field>

    <!-- Bank Name -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Bank Name</mat-label>
      <input matInput formControlName="bank_name" />
    </mat-form-field>

    <!-- Loan Amount -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Loan Amount</mat-label>
      <input matInput formControlName="loan_amount" type="number" />
    </mat-form-field>

    <!-- Purpose of Loan -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Purpose of Loan</mat-label>
      <input matInput formControlName="purpose_of_loan" type="number" />
    </mat-form-field>

    <!-- Purpose Name -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Purpose Name</mat-label>
      <input matInput formControlName="purpose_name" />
    </mat-form-field>

    <!-- Monthly Rent Amount -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Monthly Rent Amount</mat-label>
      <input matInput formControlName="monthly_rent_amount" />
    </mat-form-field>

    <!-- Loan Type -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Loan Type</mat-label>
      <input matInput formControlName="loan_type" type="number" />
    </mat-form-field>

    <!-- Employer Name -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Employer Name</mat-label>
      <input matInput formControlName="employer_name" />
    </mat-form-field>

    <!-- Gender -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Gender</mat-label>
      <input matInput formControlName="gender" type="number" />
    </mat-form-field>

    <!-- Full Name -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Full Name</mat-label>
      <input matInput formControlName="full_name" />
    </mat-form-field>

    <!-- Date of Birth -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Date of Birth</mat-label>
      <input matInput formControlName="dob" type="date" />
    </mat-form-field>

    <!-- Designation -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Designation</mat-label>
      <input matInput formControlName="designation" />
    </mat-form-field>

    <!-- Current Work Experience -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Current Work Experience</mat-label>
      <input matInput formControlName="current_work_exp" type="date" />
    </mat-form-field>

    <!-- Total Work Experience -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Total Work Experience</mat-label>
      <input matInput formControlName="total_work_exp" type="date" />
    </mat-form-field>

    <!-- Office Pincode -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Office Pincode</mat-label>
      <input matInput formControlName="office_pincode" type="number" />
    </mat-form-field>

    <!-- Office City Name -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Office City Name</mat-label>
      <input matInput formControlName="office_city_name" />
    </mat-form-field>

    <!-- Education Qualification -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Education Qualification</mat-label>
      <input matInput formControlName="education_qualification" />
    </mat-form-field>

    <!-- Is Office Email -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Is Office Email</mat-label>
      <input matInput formControlName="is_office_email" type="number" />
    </mat-form-field>

    <!-- Official Email ID -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Official Email ID</mat-label>
      <input matInput formControlName="offical_email_id" type="email" />
    </mat-form-field>

    <!-- Industry ID -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Industry ID</mat-label>
      <input matInput formControlName="Industry_id" type="number" />
    </mat-form-field>

    <!-- IP Address -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>IP Address</mat-label>
      <input matInput formControlName="ip_address" />
    </mat-form-field>

    <!-- Consent -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Consent</mat-label>
      <input matInput formControlName="consent" type="number" />
    </mat-form-field>

    <!-- Consent Datetime -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Consent Datetime</mat-label>
      <input matInput formControlName="consent_datetime" type="datetime-local" />
    </mat-form-field>

    <button class="file-btn" mat-flat-button color="primary" type="submit">
      Submit
    </button>
  </form>
</div>
<app-footer></app-footer>
```

# TS

```JavaScript
import { Component, OnInit, ViewEncapsulation } from '@angular/core';
import { MenuItem } from 'primeng/api';
import { HttpClient } from '@angular/common/http';

@Component({
  selector: 'app-mwpage',
  templateUrl: './mwpage.component.html',
  styleUrls: ['./mwpage.component.css'],
  encapsulation: ViewEncapsulation.None,
})
export class MwpageComponent {
  myForm: FormGroup;

  constructor(private fb: FormBuilder, private http: HttpClient) {
    this.myForm = this.fb.group({
      utm_source: ['',],
      utm_medium: ['',],
      utm_campaign: ['',],
      occupation_type: [,],
      phone_no: [,],
      pincode: [,],
      city_name: ['',],
      pan: ['',],
      email: ['',],
      marital_status: ['',],
      residence_type: ['',],
      net_monthly_incm: [,],
      employer_type: [,],
      mode_of_salary: [,],
      bank_name: ['',],
      loan_amount: [,],
      purpose_of_loan: [,],
      purpose_name: ['',],
      monthly_rent_amount: ['',],
      loan_type: [,],
      employer_name: ['',],
      gender: [,],
      full_name: ['',],
      dob: ['',],
      designation: ['',],
      current_work_exp: ['',],
      total_work_exp: ['',],
      office_pincode: [,],
      office_city_name: ['',],
      education_qualification: ['',],
      is_office_email: [,],
      offical_email_id: ['',],
      Industry_id: [,],
      ip_address: ['',],
      consent: [,],
      consent_datetime: ['',],
    });
  }

  onSubmit() {
    console.log('Submit button clicked');
    if (this.myForm.valid) {
      const formData = this.myForm.value;
      console.log('Form Data:', formData);
      // You can send the formData to your API endpoint here.
    } else {
      console.log('Form is invalid');
    }
  }
}
```

# CSS

```JavaScript
@import url("https://fonts.googleapis.com/css2?family=Cabin:wght@400;500;600;700&family=Gabarito:wght@400;500;600&family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap");
.form-container {
  /* font-family: 'Gabarito', sans-serif; */
  display: flex;
  flex-direction: column; /* Stack child elements vertically */
  align-items: center; /* Center child elements horizontally */
  justify-content: center; /* Center child elements vertically */
  /* min-height: 70vh; Adjust the minimum height as needed */
  /* background-color: rgb(28, 28, 28); */
}
.form-container form {
  width: 400px;
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.empd {
  display: flex;
  flex-direction: column;
}
.custom-input {
  border: 1px solid \#ccc; /* Add your desired border styles */
}
.fibe-title {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.fibe-title h1 {
  font-family: "Gabarito", sans-serif;
  font-size: 36px;
  padding: 10px;
  margin: 10px;
}
.mat-form-field {
  margin: 10px;
}
.custom-inputs {
  margin: 2px;
}
.file-btn {
  margin: 2px;
  margin-bottom: 10px;
}



/*  */
.form-container {
  display: flex;
  flex-wrap: wrap;
}

.input-row {
  display: flex;
  flex: 1;
  margin-right: 10px; /* Adjust as needed for spacing between columns */
}

.custom-inputs {
  flex: 1;
  margin-right: 10px; /* Adjust as needed for spacing between inputs */
}

/*  */
@media screen and (max-width: 600px) {
  div * {
    align-items: center;
    flex-direction: column;
    display: flex; /* Optional */
  }
}
```