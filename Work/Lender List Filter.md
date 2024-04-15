## First check - Age 

```js
function filterLendersByAge(age) {
    const eligibleLenders = [];
    const lenders = {
        "Fibe": { minAge: 21, maxAge: 55 },
        "Upwards": { minAge: 21, maxAge: 55 },
        "Cashe": { minAge: 18, maxAge: 60 },
        "Faircent": { minAge: 25, maxAge: 55 },
        "Prefr": { minAge: 22, maxAge: 55 }
    };
    for (const lender in lenders) {
        if (Object.prototype.hasOwnProperty.call(lenders, lender)) {
            const { minAge, maxAge } = lenders[lender];
            if (age >= minAge && age <= maxAge) {
                eligibleLenders.push(lender);
            }
        }
    }
    return eligibleLenders;
}

// Example usage
const userAge = 30;
const eligibleLenders = filterLendersByAge(userAge);
console.log("Eligible lenders based on age:", eligibleLenders);
```

```js
// Function to filter lenders by age and salary
function filterLenders(age, salary) {
    const eligibleLenders = [
        { name: "Fibe", minAge: 21, maxAge: 55, minSalary: 15000 },
        { name: "Upwards", minAge: 21, maxAge: 55, minSalary: 18000 },
        { name: "Cashe", minAge: 18, maxAge: 60, minSalary: 15000 },
        { name: "Faircent", minAge: 25, maxAge: 55, minSalary: 25000 },
        { name: "Prefr", minAge: 22, maxAge: 55, minSalary: 15000 }
    ];
    
    return eligibleLenders.filter(lender => 
        lender.minAge <= age && 
        lender.maxAge >= age && 
        lender.minSalary <= salary
    );
}

// Example usage
const userAge = 30;
const userSalary = 20000;
const filteredLenders = filterLenders(userAge, userSalary);
console.log("Filtered lenders based on age and salary:", filteredLenders);

```