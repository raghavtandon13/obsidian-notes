```Markdown
<!-- old html -->
<div class="signup_page">
  <nav class="navbar navbar-light">
    <div class="container nav_bar">
      <a class="navbar-brand" href="#">
        <img src="../../assets/values/Cred Mantra logo_page-0001 2.svg" alt="" loading="lazy" style="margin: 30px" />
      </a>
    </div>
  </nav>
  <div class="col-md-6">
    <img src="assets\image_processing20190919-32761-1vdd0xf.gif" />
  </div>

  <div class="center-heading"></div>
  <div class="col-md-12" style="display: flex">
    <div class="container signup_box">
      <div class="row phone_details">
        <div role="group">
          <h1
            style="
              font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
              font-size: 32px;
              font-weight: 400;
              text-align: center;
              margin-bottom: 40px;
            "
          >
            Log in to CredMantra
          </h1>
          <mat-form-field class="example-full-width">
            <mat-label>Name</mat-label>
            <input matInput [(ngModel)]="name" required pattern="[a-zA-Z ]*" \#nameInput="ngModel" />
            <mat-error *ngIf="nameInput.invalid && (nameInput.dirty || nameInput.touched)">
              <span class="error-message" *ngIf="nameInput.errors?.['required']">Name is required.</span>
              <span class="error-message" *ngIf="nameInput.errors?.['pattern']">Name should only contain alphabetic characters.</span>
            </mat-error> </mat-form-field
          ><br /><br /><br />

          <mat-form-field class="example-full-width">
            <mat-label>Mobile Number</mat-label>
            <input type="tel" maxlength="10" matInput placeholder="----------" [(ngModel)]="phone" name="phone" required pattern="[0-9]*" />
          </mat-form-field>
        </div>
        <br /><br /><br /><br />
        <button
          *ngIf="!loading"
          (click)="authenticate()"
          [disabled]="nameInput.invalid || phone.invalid"
          mat-raised-button
          color="primary"
          style="
            margin: 20px;
            width: 90%;
            align-items: center;
            display: flex;
            justify-content: center;
            left: 10px;
            background-color: black;
            color: white;
          "
          [ngStyle]="{ 'background-color': nameInput.invalid || phone.invalid ? 'black' : '' }"
        >
          SEND OTP
        </button>
        <!-- <button mat-raised-button color="primary" (click)="sendOTP()" [disabled]="nameInput.invalid || phone.invalid">Send OTP</button> -->

        <div *ngIf="loading" class="spinner">
          <mat-spinner class="spinner" diameter="30"></mat-spinner>
        </div>

        <div id="error"></div>
        <!-- <div class="divider">or</div>
        <button
        routerLink="/new-account"
          mat-raised-button
          style="
            margin: 20px;
            width: 90%;
            align-items: center;
            display: flex;
            justify-content: center;
            left: 10px;
            background-color: rgb(80, 80, 80);
            color: white;
          "
        >
          Create New Account
        </button> -->
        <br />

        <!-- <div style="display:flex;justify-content:center;align-items:center;size:900%;">
                  <asl-google-signin-button type='standard' size='large' theme="outline" logo_alignment="center" ></asl-google-signin-button>
              </div> -->

        <!-- </div>
      </div>
  </div> -->
      </div>
    </div>
  </div>
</div>
```