- [x] Mobile Number: `**mobile**`
- [x] First Name: `**firstName**`
- [x] Last Name: `**lastName**`
- [x] Date of Birth: `**dob**`
- [ ] Email: `**email**` **(change gender to email)**
- [x] Marital Status: `**maritalstatus**`

  

- [x] Address Line 1: `**address1**`
- [x] Address Line 2: `**address2**`
- [x] Landmark: `**landmark**`
- [x] City: `**city**`
- [x] Pincode: `**pincode**`
- [x] state (added by me)

  

1. Aadhar: `**personalAadhaar**`
2. PAN (Personal): `**personalPAN**`

- [ ] Profession: `**profession**`

  

- [x] Company Email: `**companyEmail**`
- [x] Company PAN: `**companyPAN**`
- [x] Company GST: `**companyGstNumber**`
- [x] Registered As: `**registeredAs**`
- [x] Business Run By: `**businessRunBy**`
- [x] Product Category: `**productCategory**`

  

```Go
<div class="form-container">
  <form (ngSubmit)="submit()" \#stepperForm="ngForm">
    <!-- Mobile Number -->
    <mat-form-field appearance="outline" class="custom-inputs" color="primary">
      <mat-label>Mobile Number</mat-label>
      <input matInput formControlName="mobile" required type="text" pattern="^[6-9]{1}[0-9]{9}$" />
      <mat-error *ngIf="myForm.get('mobile')?.hasError('pattern')"> Invalid mobile number format. </mat-error>
    </mat-form-field>

    <!-- First Name and Last Name -->
    <div class="empd" formGroupName="profile">
      <div>
        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>First Name</mat-label>
          <input matInput formControlName="firstName" pattern="^[\p{L} .'-]+$" />
          <mat-error *ngIf="myForm.get('profile.firstName')?.hasError('pattern')"> Invalid first name format. </mat-error>
        </mat-form-field>

        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>Last Name</mat-label>
          <input matInput formControlName="lastName" pattern="^[\p{L} .'-]+$" />
          <mat-error *ngIf="myForm.get('profile.lastName')?.hasError('pattern')"> Invalid last name format. </mat-error>
        </mat-form-field>
      </div>

      <!-- Date of Birth -->
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Date of Birth</mat-label>
        <input matInput formControlName="dob" type="date" required />
        <mat-error *ngIf="myForm.get('profile.dob')?.hasError('required')"> Date of Birth is required. </mat-error>
      </mat-form-field>
      <!-- Email -->
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Email</mat-label>
        <input matInput formControlName="email" type="email" required />
        <mat-error *ngIf="myForm.get('profile.email')?.hasError('required')"> Email is required. </mat-error>
      </mat-form-field>
      <!-- Company Email -->
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Company Email</mat-label>
        <input matInput formControlName="companyEmail" type="email" required />
        <mat-error *ngIf="myForm.get('profile.companyEmail')?.hasError('required')"> Company Email is required. </mat-error>
      </mat-form-field>

      <!-- Profession -->
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Profession</mat-label>
        <input matInput formControlName="profession" required />
        <mat-error *ngIf="myForm.get('profile.profession')?.hasError('required')"> Profession is required. </mat-error>
      </mat-form-field>

      <!-- Address Line 1 and Line 2 -->
      <div>
        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>Address Line 1</mat-label>
          <input matInput formControlName="address1" required />
          <mat-error *ngIf="myForm.get('profile.address1')?.hasError('required')"> Address Line 1 is required. </mat-error>
        </mat-form-field>

        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>Address Line 2</mat-label>
          <input matInput formControlName="address2" />
        </mat-form-field>
      </div>

      <!-- Landmark -->
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Landmark</mat-label>
        <input matInput formControlName="landmark" />
      </mat-form-field>

      <!-- City -->
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>City</mat-label>
        <input matInput formControlName="city" required />
        <mat-error *ngIf="myForm.get('profile.city')?.hasError('required')"> City is required. </mat-error>
      </mat-form-field>

      <!-- Pincode -->
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Pincode</mat-label>
        <input matInput formControlName="pincode" type="text" pattern="^\d{6}$" required />
        <mat-error *ngIf="myForm.get('profile.pincode')?.hasError('pattern')"> Invalid pincode format. (Should be 6-digit numeric) </mat-error>
        <mat-error *ngIf="myForm.get('profile.pincode')?.hasError('required')"> Pincode is required. </mat-error>
      </mat-form-field>

      <!-- Marital Status -->
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Marital Status</mat-label>
        <mat-select formControlName="maritalstatus" required>
          <mat-option value="Single">Single</mat-option>
          <mat-option value="Married">Married</mat-option>
        </mat-select>
        <mat-error *ngIf="myForm.get('profile.maritalstatus')?.hasError('required')"> Marital Status is required. </mat-error>
      </mat-form-field>
    </div>
    <!-- Aadhar -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Aadhar</mat-label>
      <input matInput formControlName="personalAadhaar" required />
      <mat-error *ngIf="myForm.get('finance.personalAadhaar')?.hasError('pattern')"> Invalid Aadhar format. </mat-error>
      <mat-error *ngIf="myForm.get('finance.personalAadhaar')?.hasError('required')"> PAN is required. </mat-error>
    </mat-form-field>
    <!-- Finance Section -->
    <div class="empd" formGroupName="finance">
      <!-- PAN -->
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>PAN</mat-label>
        <input matInput formControlName="personalPAN" required pattern="^[A-Z]{5}[0-9]{4}[A-Z]$" />
        <mat-error *ngIf="myForm.get('finance.personalPAN')?.hasError('pattern')"> Invalid PAN format. </mat-error>
        <mat-error *ngIf="myForm.get('finance.personalPAN')?.hasError('required')"> PAN is required. </mat-error>
      </mat-form-field>
    </div>

    <!--Company PAN -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Company PAN</mat-label>
      <input matInput formControlName="companyPAN" required pattern="^[A-Z]{5}[0-9]{4}[A-Z]$" />
      <mat-error *ngIf="myForm.get('finance.companyPAN')?.hasError('pattern')"> Invalid PAN format. </mat-error>
      <mat-error *ngIf="myForm.get('finance.companyPAN')?.hasError('required')"> Compnay PAN is required. </mat-error>
    </mat-form-field>

    <!--Company GST-->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Company GST</mat-label>
      <input matInput formControlName="companyGstNumber" required pattern="^[0-9]{2}[A-Z]{5}[0-9]{4}[A-Z]{1}[A-Z0-9]{1}[A-Z]{1}[A-Z0-9]{1}$" />
      <mat-error *ngIf="myForm.get('finance.companyGstNumber')?.hasError('pattern')"> Invalid GST format. </mat-error>
      <mat-error *ngIf="myForm.get('finance.companyGstNumber')?.hasError('required')"> Compnay GST is required. </mat-error>
    </mat-form-field>

    <!-- Registered As -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Registered As</mat-label>
      <mat-select formControlName="registeredAs" required>
        <mat-option *ngFor="let option of registeredAsEnum | keyvalue" [value]="option.key">
          {{ option.value }}
        </mat-option>
      </mat-select>
      <mat-error *ngIf="myForm.get('profile.registeredAs')?.hasError('required')"> Registered As is required. </mat-error>
    </mat-form-field>

    <!-- Business Run By -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Business Run By</mat-label>
      <mat-select formControlName="businessRunBy" required>
        <mat-option *ngFor="let option of businessRunByEnum | keyvalue" [value]="option.key">
          {{ option.value }}
        </mat-option>
      </mat-select>
      <mat-error *ngIf="myForm.get('profile.businessRunBy')?.hasError('required')"> Business Run By is required. </mat-error>
    </mat-form-field>
    <!-- Business Run By -->
    <mat-form-field appearance="outline" class="custom-inputs">
      <mat-label>Product Category</mat-label>
      <mat-select formControlName="productCategory" required>
        <mat-option *ngFor="let option of productCategoryEnum | keyvalue" [value]="option.key">
          {{ option.value }}
        </mat-option>
      </mat-select>
      <mat-error *ngIf="myForm.get('profile.productCategory')?.hasError('required')"> Product Category is required. </mat-error>
    </mat-form-field>

    <!-- Other sections and fields here -->

    <button class="file-btn" mat-flat-button color="primary" type="submit">Submit</button>
  </form>
</div>
```