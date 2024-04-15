```JavaScript
</div>
<div class="form-container">
  <form [formGroup]="myForm" (submit)="onSubmit()">
    <!-- Mobile Number -->
    <mat-form-field appearance="outline" class="custom-inputs" color="primary">
      <mat-label>Mobile Number</mat-label>
      <input matInput formControlName="mobilenumber" required type="number" />
    </mat-form-field>

    <!-- Profile Section -->
    <div formGroupName="profile">
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
        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>Date of Birth</mat-label>
          <input matInput formControlName="dob" type="date" />
        </mat-form-field>

        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>Profession</mat-label>
          <input matInput formControlName="profession" />
        </mat-form-field>
      </div>
      <div>
        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>Address Line 1</mat-label>
          <input matInput formControlName="address1" />
        </mat-form-field>

        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>Address Line 2</mat-label>
          <input matInput formControlName="address2" />
        </mat-form-field>
      </div>
      <div>
        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>Landmark</mat-label>
          <input matInput formControlName="landmark" />
        </mat-form-field>

        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>City</mat-label>
          <input matInput formControlName="city" />
        </mat-form-field>
      </div>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Pincode</mat-label>
        <input matInput formControlName="pincode" type="number" />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Marital Status</mat-label>
        <mat-select formControlName="maritalstatus">
          <mat-option value="Single">Single</mat-option>
          <mat-option value="Married">Married</mat-option>
        </mat-select>
      </mat-form-field>
    </div>

    <!-- Finance Section -->
    <div formGroupName="finance">
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>PAN</mat-label>
        <input matInput formControlName="pan" required />
      </mat-form-field>
    </div>

    <!-- Employee Details Section -->
    <div class="empd" formGroupName="employeedetails">
      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Employer Name</mat-label>
        <input matInput formControlName="employername" />
      </mat-form-field>

      <div>
        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>Office Address</mat-label>
          <input matInput formControlName="officeaddress" />
        </mat-form-field>

        <mat-form-field appearance="outline" class="custom-inputs">
          <mat-label>Office City</mat-label>
          <input matInput formControlName="officeCity" />
        </mat-form-field>
      </div>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Office Pincode</mat-label>
        <input matInput formControlName="officepincode" type="number" />
      </mat-form-field>

      <mat-form-field appearance="outline" class="custom-inputs">
        <mat-label>Salary</mat-label>
        <input matInput formControlName="salary" type="number" />
      </mat-form-field>
    </div>

    <button class="file-btn" mat-flat-button color="primary" type="submit">
      Submit
    </button>
  </form>
</div>
```