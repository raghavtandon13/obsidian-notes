# HTML

```JavaScript
<app-navbar></app-navbar>
<div class="fibe-title">
  <h1>Connect with Fibe</h1>
  <div class="logo">
    <img src="assets\FIBE.webp" alt="" />
  </div>
</div>
<div class="wrapper colored-div">
  <div class="form-container">
    <h1>Fill the details asked below.</h1>
    <form [formGroup]="myForm" (submit)="onSubmit()">
      <mat-vertical-stepper linear>
        <!-- Step 1: Mobile Number -->
        <mat-step>
          <ng-template matStepLabel>Mobile Number</ng-template>
          <div>
            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>First Name</mat-label>
              <input matInput formControlName="firstname" />
            </mat-form-field>

            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Last Name</mat-label>
              <input matInput formControlName="lastname" />
            </mat-form-field>
          </div>
          <div>
            <mat-form-field appearance="outline" class="custom-inputs" color="primary">
              <mat-label>Mobile Number</mat-label>
              <input matInput formControlName="mobilenumber" type="number" onKeyPress="if(this.value.length==10) return false;" />
            </mat-form-field>

            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Date of Birth</mat-label>
              <input matInput formControlName="dob" type="date" />
            </mat-form-field>
          </div>

          <div>
            <button mat-stroked-button color="primary" matStepperNext>Next</button>
          </div>
        </mat-step>

        <!-- Step 2: Profile Section -->
        <mat-step>
          <ng-template matStepLabel>Profile</ng-template>
          <div formGroupName="profile">
            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Address Line 1</mat-label>
              <input matInput formControlName="address1" />
            </mat-form-field>

            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Address Line 2</mat-label>
              <input matInput formControlName="address2" />
            </mat-form-field>

            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Landmark</mat-label>
              <input matInput formControlName="landmark" />
            </mat-form-field>

            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Pincode</mat-label>
              <input matInput formControlName="pincode" type="number" onKeyPress="if(this.value.length==6) return false;" />
            </mat-form-field>
            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>City</mat-label>
              <input matInput formControlName="city" />
            </mat-form-field>

            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Marital Status</mat-label>
              <mat-select formControlName="maritalstatus">
                <mat-option value="Single">Single</mat-option>
                <mat-option value="Married">Married</mat-option>
              </mat-select>
            </mat-form-field>
            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Profession</mat-label>
              <mat-select formControlName="profession">
                <mat-option value="Salaried">Salaried</mat-option>
                <mat-option value="Self-employed">Self-employed</mat-option>
              </mat-select>
            </mat-form-field>
            <!-- <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Profession</mat-label>
              <input matInput formControlName="profession" />
            </mat-form-field> -->
            <div>
              <button mat-stroked-button matStepperPrevious>Back</button>
              <button mat-stroked-button matStepperNext>Next</button>
            </div>
          </div>
        </mat-step>

        <!-- Step 3: Finance Section -->
        <mat-step>
          <ng-template matStepLabel>Finance</ng-template>
          <div formGroupName="finance">
            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>PAN</mat-label>
              <input matInput formControlName="pan" maxlength="10" />
            </mat-form-field>

            <div>
              <button mat-stroked-button matStepperPrevious>Back</button>
              <button mat-stroked-button matStepperNext>Next</button>
            </div>
          </div>
        </mat-step>

        <!-- Step 4: Employee Details Section -->
        <mat-step>
          <ng-template matStepLabel>Employee Details</ng-template>
          <div formGroupName="employeedetails">
            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Employer Name</mat-label>
              <input matInput formControlName="employername" />
            </mat-form-field>

            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Office Address</mat-label>
              <input matInput formControlName="officeaddress" />
            </mat-form-field>

            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Office City</mat-label>
              <input matInput formControlName="officeCity" />
            </mat-form-field>

            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Office Pincode</mat-label>
              <input matInput formControlName="officepincode" type="number" onKeyPress="if(this.value.length==6) return false;" />
            </mat-form-field>

            <mat-form-field appearance="outline" class="custom-inputs">
              <mat-label>Salary</mat-label>
              <input matInput formControlName="salary" type="number" />
            </mat-form-field>
            <!-- consent -->
            <div class="custom-inputs">
              <label>
                <input type="checkbox" formControlName="consent" [value]="true" />
                I agree
              </label>
            </div>
            <!-- consent -->
          </div>
          <div class="sub-btn-div">
            <button mat-stroked-button matStepperPrevious>Back</button>
            <button class="file-btn" mat-flat-button color="primary" (click)="onSubmit()">Submit</button>
          </div>
        </mat-step>

        <!-- Final Step: Submit Button -->
      </mat-vertical-stepper>
    </form>
  </div>
</div>

<app-footer></app-footer>
```

# TS

```JavaScript
import { Component, OnInit, ViewEncapsulation } from '@angular/core';
import { LocationService } from 'src/app/services/locationService';
import { AbstractControl, ValidationErrors } from '@angular/forms';
import { FormBuilder, FormGroup, Validators } from '@angular/forms';
import { HttpClient } from '@angular/common/http';
import { Router } from '@angular/router';

@Component({
  selector: 'app-fibe',
  templateUrl: './fibe.component.html',
  styleUrls: ['./fibe.component.css'],
  encapsulation: ViewEncapsulation.None, // Add this line
})
export class FibeComponent {
  myForm: FormGroup;

  constructor(private fb: FormBuilder, private http: HttpClient, private router: Router, private locationService: LocationService) {
    this.myForm = this.fb.group({
      mobilenumber: ['', Validators.required],
      firstname: ['', Validators.required],
      lastname: ['', Validators.required],
      dob: ['', Validators.required],
      profile: this.fb.group({
        profession: ['', Validators.required],
        address1: ['', Validators.required],
        address2: ['', Validators.required],
        landmark: ['', Validators.required],
        city: ['', Validators.required],
        pincode: ['', Validators.required],
        maritalstatus: ['', Validators.required],
      }),
      finance: this.fb.group({
        pan: ['', [this.uppercaseAndMaxLength]],
      }),
      employeedetails: this.fb.group({
        employername: ['', Validators.required],
        officeaddress: ['', Validators.required],
        officeCity: ['', Validators.required],
        officepincode: ['', [Validators.pattern(/^\d{6}$/)]], // 6-digit numeric pattern
        salary: ['', Validators.required],
      }),
      consent: ['true'],
      consentDatetime: [''],
    });
    this.myForm.get('profile.pincode')?.valueChanges.subscribe((pincode) => {
      if (pincode) {
        // Call your service to fetch city data based on the pincode.
        this.locationService.getCityByPincode(pincode).subscribe((response) => {
          // Extract the "adminName2" from the API response and update the "city" form control.
          const city = response;
          this.myForm.get('profile.city')?.setValue(city);
        });
      }
    });
  }

  getCityByPincode(pincode: string) {
    // Replace with the actual API endpoint for fetching city data based on the pincode.
    return this.http.get('YOUR_API_ENDPOINT/' + pincode);
  }

  uppercaseAndMaxLength(control: AbstractControl): ValidationErrors | null {
    const value = control.value;
    // Convert the value to uppercase
    const uppercaseValue = value.toUpperCase();
    if (value !== uppercaseValue) {
      control.setValue(uppercaseValue, { emitEvent: false });
    }
    // Check if the length is exactly 10 characters
    if (uppercaseValue.length !== 10) {
      return { invalidLength: true };
    }
    return null;
  }

  ngOnInit(): void {}

  onSubmit() {
    console.log(this.myForm.value);
    if (this.myForm.valid) {
      console.log('valid');
      const formData = this.myForm.value;

      const currentDatetime = new Date().toISOString().replace('T', ' ').slice(0, 19);
      // Assign the generated datetime to the formData
      formData.consentDatetime = currentDatetime;

      // Send a POST request to the API endpoint
      this.http.post('http://localhost:3000/api/v1/partner-api/fibe', formData).subscribe(
        (response) => {
          console.log('API Response:', response);
          this.router.navigate(['/fibe/result'], {
            queryParams: { data: JSON.stringify(response) },
          });
        },
        (error) => {
          console.error('API Error:', error);
          // Handle error, e.g., display an error message to the user
        }
      );
    } else {
      console.log('form invalid');
    }
  }
}
```

# CSS

```JavaScript
@import url("https://fonts.googleapis.com/css2?family=Cabin:wght@400;500;600;700&family=Gabarito:wght@400;500;600&family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap");
.wrapper {
  /* margin-top: 40px; */
  display: flex;
  flex-direction: row;
}
/* .logo {
  width: 40px;
} */
.logo img {
  width: 150px;
}
.form-container {
  flex: 2;
  height: max-content;
  min-height: 90vh;
  /* font-family: 'Gabarito', sans-serif; */
  display: flex;
  flex-direction: column; /* Stack child elements vertically */
  align-items: center; /* Center child elements horizontally */
  /* Center child elements vertically */
  /* min-height: 70vh; Adjust the minimum height as needed */
  /* background-color: rgb(28, 28, 28); */
}
.form-container h1 {
  font-family: "Gabarito", sans-serif;
  /* text-align: start; */
  margin: 0;
  margin-top: 10px;
  margin-left: 30px;
  margin-bottom: 10px;
}
.form-container form {
  width: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.empd {
  display: flex;
  flex-direction: column;
}
.custom-input {
  border: 1px solid \#ccc; /* Add your desired border styles */
}
.fibe-title {
  position: relative;
  display: flex;
  background-color: antiquewhite;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  z-index: 9999;
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
@media screen and (max-width: 600px) {
  div * {
    align-items: center;
    flex-direction: column;
    display: flex; /* Optional */
  }
  .wrapper {
    flex-direction: column;
  }
}
button {
  margin: 1px;
}
.sub-btn-div {
  display: flex;
  flex-direction: row;
  align-items: baseline;
}

.mdc-notched-outline__leading {
  border-radius: 10px 0px 0px 10px !important;
  border-color: rgb(34, 106, 208) !important;
  border-width: medium !important;
}
.mdc-notched-outline__trailing {
  border-radius: 0px 10px 10px 0px !important;
  border-width: medium !important;
  border-color: rgb(34, 106, 208) !important;
}
.mdc-notched-outline__notch {
  border-left: none !important;
  border-width: medium !important;
  border-top-color: rgb(34, 106, 208) !important;
  border-bottom-color: rgb(34, 106, 208) !important;
}

/* mat-step ng-tns-c21-0 ng-star-inserted */
.mat-step {
  display: flex;
  align-items: center;
}
.mat-step-header {
  background-color: tran !important;
  flex: 1;
}
.mat-vertical-content-container {
  /* background-color: aqua; */
  flex: 5;
}

.mat-vertical-content-container {
  margin-left: 0 !important;
}
/* .mat-stepper-vertical-line::before  */
.mat-stepper-vertical-line::before {
  /* display: none; */
  content: "";
  /* height: 200%; */
  /* height: 100%; */
  /* margin-top: -200px; */
  /* margin-bottom: -100px; */
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  border-left-width: 2px !important;
  border-left-style: solid black !important;
  border-color: gray !important;
  z-index: 9;
}
.mat-stepper-vertical {
  border: 1px solid lightgray;
  padding: 30px;
  border-radius: 10px;
  /* background-color: aliceblue; */
  box-shadow: 0px 0px 7px 0px rgba(0, 0, 0, 0.2);
}
```