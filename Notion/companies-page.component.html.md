```JavaScript
<div class="container-flex">
  <div class="row title">
    <h1>
      <b style="color: aliceblue; margin-top: 200px"> {{ heading }} </b>
    </h1>
  </div>
  <div class="d-flex justify-content-center">
    <div class="col-md-8">
      <table class="table-centered">
        <thead class="thead-dark" style="font-size: 20px; text-align: center">
          <tr style="color: rgb(242, 235, 235)">
            <th scope="col">OFFERS</th>
            <th scope="col">LOAN TENURE</th>
            <th scope="col">LOAN AMOUNT</th>
            <th scope="col">INTEREST</th>
            <th scope="col">PROCEED</th>
          </tr>
        </thead>
        <tbody style="font-size: 20px">
          <tr>
            <td>
              <img src="assets\values\MONEY-WIDE.svg" style="width: 70px" />
            </td>
            <td>6 to 36 Months</td>
            <td>20,000-3Lakhs</td>
            <td>10% - 26%</td>
            <!-- <td><button>APPLY NOW</button></td> -->
            <td>
              <!-- <button (click)="navigateToMoneyWide()">APPLY NOW</button> -->
              <button routerLink="/moneywideform">APPLY NOW</button>
            </td>
            <!-- <td><button (click)="navigateToMoneyWide()">APPLY NOW</button></td> -->
          </tr>
          <tr>
            <td>
              <img
                src="assets\FIBE.webp"
                style="width: 100px"
              />
            </td>
            <td>12 to 36 Months</td>
            <td>20,000-5Lakhs</td>
            <td>1.85 Months(starts)</td>
            <td><button routerLink="/fibe">APPLY NOW</button></td>
          </tr>
          <tr>
            <td>
              <img src="assets\values\Finnable.svg" style="width: 100px" />
            </td>
            <td>6 to 60 Months</td>
            <td>upto 10 Lakhs</td>
            <td>12% - 28%</td>
            <td><button>APPLY NOW</button></td>
          </tr>
          <tr>
            <td>
              <img
                src="assets\values\Paysence_service 1 (1).svg"
                style="width: 100px"
              />
            </td>
            <td>12 to 60 Months</td>
            <td>5000-5Lakhs</td>
            <td>10% - 26%</td>
            <td><button>APPLY NOW</button></td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</div>
```

```JavaScript
/* Base styles for the container and rows */
.container-flex {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20px;
  box-sizing: border-box;
}

/* Styles for the title */
.title {
  text-align: center;
  margin-bottom: 20px;
}

.title h1 {
  font-size: 2rem;
}

/* Styles for the table */
.table-centered {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
  box-sizing: border-box;
}

/* Adjusting the content alignment within the cells to achieve left padding */
.table-centered th,
.table-centered td {
  border: 1px solid \#ccc;
  padding: 10px;
  text-align: center;
  box-sizing: border-box;
}

/* CSS for table header */
.thead-dark {
  background-color: \#343a40;
  color: \#fff;
}

/* CSS for table body */
tbody {
  font-size: 1.25rem;
  color: rgb(219, 212, 212);
}

/* CSS for table buttons */
table td button {
  background-color: \#007bff;
  color: \#fff;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

table td button:hover {
  background-color: \#0056b3;
}

/* Media Query for mobile devices */
@media only screen and (max-width: 767px) {
  /* Adjust the padding for better spacing on mobile */
  .table-centered th,
  .table-centered td {
    padding: 5px;
  }

  /* Reduce the font size for table header and body */
  .table-centered {
    font-size: 1rem;
  }

  .thead-dark {
    font-size: 1.125rem;
  }

  /* Reduce button font size and padding for mobile */
  table td button {
    font-size: 0.75rem;
    padding: 6px 12px;
  }

  /* Adjust margin for a more compact layout */
  .container-flex {
    margin-top: 10px;
  }

  /* Reduce font size for the title on mobile */
  .title h1 {
    font-size: 1.5rem;
  }
}
```