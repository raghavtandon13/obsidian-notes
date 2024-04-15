# HTML

```JavaScript
<app-navbar></app-navbar>
<div class="fibe-title">
  <h1>Connect with Finnable</h1>
</div>
<div class="form-container">
  <form [formGroup]="myForm" (submit)="onSubmit()">
    <!-- PAN -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>PAN</mat-label>
      <input matInput formControlName="pan" required />
    </mat-form-field>

    <!-- Personal Email -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Personal Email</mat-label>
      <input matInput formControlName="personalEmail" required />
    </mat-form-field>

    <!-- First Name -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>First Name</mat-label>
      <input matInput formControlName="firstName" required />
    </mat-form-field>

    <!-- Last Name -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Last Name</mat-label>
      <input matInput formControlName="lastName" required />
    </mat-form-field>

    <!-- Middle Name (Optional) -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Middle Name</mat-label>
      <input matInput formControlName="middleName" />
    </mat-form-field>

    <!-- Date of Birth -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Date of Birth (yyyy-MM-dd)</mat-label>
      <input matInput formControlName="dateOfBirth" type="date" required />
    </mat-form-field>

    <!-- Gender (Optional) -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Gender</mat-label>
      <input matInput formControlName="gender" />
    </mat-form-field>

    <!-- Marital Status (Optional) -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Marital Status</mat-label>
      <input matInput formControlName="maritalStatus" />
    </mat-form-field>

    <!-- Highest Education (Optional) -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Highest Education</mat-label>
      <input matInput formControlName="highestEducation" />
    </mat-form-field>

    <!-- Current Address -->
    <div class="finnable-input" formGroupName="currentAddress">
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Address Line 1</mat-label>
        <input matInput formControlName="line1" />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Address Line 2</mat-label>
        <input matInput formControlName="line2" />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Landmark</mat-label>
        <input matInput formControlName="landmark" />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>City</mat-label>
        <input matInput formControlName="city" required />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>State</mat-label>
        <input matInput formControlName="state" required />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Pincode</mat-label>
        <input matInput formControlName="pinCode" type="number" required />
      </mat-form-field>
    </div>

    <!-- Type of Residence (Optional) -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Type of Residence</mat-label>
      <input matInput formControlName="typeOfResidence" />
    </mat-form-field>

    <!-- Duration of Residence in Months (Optional) -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Duration of Residence (Months)</mat-label>
      <input
        matInput
        formControlName="durationOfResidenceInMonths"
        type="number"
      />
    </mat-form-field>

    <!-- Employment -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Company</mat-label>
      <input matInput formControlName="company" required />
    </mat-form-field>

    <!-- Designation (Optional) -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Designation</mat-label>
      <input matInput formControlName="designation" />
    </mat-form-field>

    <!-- Total Experience in Months (Optional) -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Total Experience (Months)</mat-label>
      <input matInput formControlName="totalExperienceInMonths" type="number" />
    </mat-form-field>

    <!-- Work Email (Optional) -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Work Email</mat-label>
      <input matInput formControlName="workEmail" />
    </mat-form-field>

    <!-- Monthly Income -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Monthly Income</mat-label>
      <input matInput formControlName="monthlyIncome" type="number" required />
    </mat-form-field>

    <!-- Office Address -->
    <div class="finnable-input" formGroupName="officeAddress">
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Address Line 1</mat-label>
        <input matInput formControlName="line1" />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Address Line 2</mat-label>
        <input matInput formControlName="line2" />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Landmark</mat-label>
        <input matInput formControlName="landmark" />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>City</mat-label>
        <input matInput formControlName="city" required />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>State</mat-label>
        <input matInput formControlName="state" required />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Pincode</mat-label>
        <input matInput formControlName="pinCode" type="number" required />
      </mat-form-field>
    </div>

    <!-- Photo URL (Optional) -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Photo URL</mat-label>
      <input matInput formControlName="photoURL" />
    </mat-form-field>

    <!-- Consent Details -->
    <div formArrayName="consentDetails">
      <div
        *ngFor="
          let consentDetail of myForm.get('consentDetails')?.value;
          let i = index
        "
      >
        <div class="consent-detail finnable-input">
          <mat-form-field appearance="outline" class="custom-inputs">
            <mat-label>Consent Type</mat-label>
            <input matInput [formControlName]="i + '.type'" required />
          </mat-form-field>

          <mat-form-field appearance="outline" class="custom-inputs">
            <mat-label>Consent</mat-label>
            <input
              matInput
              [formControlName]="i + '.consent'"
              value="Yes"
              readonly
            />
          </mat-form-field>

          <mat-form-field appearance="outline" class="custom-inputs">
            <mat-label>Consent Date</mat-label>
            <input
              matInput
              [formControlName]="i + '.date'"
              type="datetime-local"
              required
            />
          </mat-form-field>
        </div>
      </div>
    </div>

    <button class="file-btn" mat-flat-button color="primary" type="submit">
      Submit
    </button>
  </form>
</div>
<app-footer></app-footer>
```

# TS

```JavaScript
import { Component, OnInit } from '@angular/core';
import { NavbarComponent } from '../../navbar/navbar.component'; // Import the navbar component
import { AuthService } from '../../services/auth.service'; // Import any required services
import { FooterComponent } from 'src/app/basic_components/footer/footer.component';
import { AbstractControl, ValidationErrors } from '@angular/forms';
import { FormBuilder, FormGroup, Validators, FormArray } from '@angular/forms';
import { HttpClient } from '@angular/common/http';

@Component({
  selector: 'app-finnable-page',
  templateUrl: './finnable-page.component.html',
  styleUrls: ['./finnable-page.component.css'],
})
export class FinnablePageComponent {
  myForm: FormGroup;

  constructor(private fb: FormBuilder) {
    this.myForm = this.fb.group({
      pan: ['', Validators.required],
      personalEmail: ['', Validators.required],
      firstName: ['', Validators.required],
      lastName: ['', Validators.required],
      middleName: [''],
      dateOfBirth: ['', Validators.required],
      gender: [''],
      maritalStatus: [''],
      highestEducation: [''],
      currentAddress: this.fb.group({
        line1: [''],
        line2: [''],
        landmark: [''],
        city: ['', Validators.required],
        state: ['', Validators.required],
        pinCode: [null, Validators.required], // You can add validation for Pincode
      }),
      typeOfResidence: [''],
      durationOfResidenceInMonths: [null],
      company: ['', Validators.required],
      designation: [''],
      totalExperienceInMonths: [null],
      workEmail: [''],
      monthlyIncome: [null, Validators.required],
      officeAddress: this.fb.group({
        line1: [''],
        line2: [''],
        landmark: [''],
        city: ['', Validators.required],
        state: ['', Validators.required],
        pinCode: [null, Validators.required], // You can add validation for Pincode
      }),
      photoURL: [''],
      consentDetails: this.fb.array([this.createConsentDetailFormGroup()]),
    });
  }

  createConsentDetailFormGroup() {
    return this.fb.group({
      type: ['', Validators.required],
      consent: ['Yes'],
      date: ['', Validators.required],
    });
  }

  addConsentDetail() {
    const consentDetails = this.myForm.get('consentDetails') as FormArray;
    consentDetails.push(this.createConsentDetailFormGroup());
  }

  removeConsentDetail(index: number) {
    const consentDetails = this.myForm.get('consentDetails') as FormArray;
    consentDetails.removeAt(index);
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
.finnable-input {
  display: flex;
  align-items: stretch;
  flex-direction: column;
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
    align-items: stretch;
    flex-direction: column;
    display: flex; /* Optional */
  }
  .form-container form {
    width: 300px;
  }
}
```