IDEA
```js
let user;
try {
  user = await User.findOne({ phone: mobileNo });
  if (!user) {
    console.log("creating");
    const newUser = new User({ phone: mobileNo });
    user = await newUser.save();
    console.log("User created successfully:", user);
  }
} catch (mongoError) {
  console.error("MongoDB error:", mongoError);
}

if (!user.accounts) {
  console.log("Initializing accounts array...");
  user.accounts = [];
  await user.save();
}
//--------------------------------------//
// call to some partner API
//--------------------------------------//

const prefrAccountData = {
  name: "Prefr",
  id: response.data.data.loanId,
  sent: requestData,
  res: responseData,
};

const prefrAccountIndex = user.accounts.findIndex(
  (account) => account.name === "Prefr",
);
if (prefrAccountIndex !== -1) {
  user.accounts[prefrAccountIndex] = prefrAccountData;
  console.log("found index", prefrAccountIndex);
} else {
  user.accounts.push(prefrAccountData);
  console.log("pushing...");
}
await user.save();

```

ABSTRACTED FUNCTIONS

```js
async function createUser(mobileNo) {
  let user;
  try {
    user = await User.findOne({ phone: mobileNo });
    if (!user) {
      console.log("creating");
      const newUser = new User({ phone: mobileNo });
      user = await newUser.save();
      console.log("User created successfully:", user);
    }
  } catch (mongoError) {
    console.error("MongoDB error:", mongoError);
  }

  if (!user.accounts) {
    console.log("Initializing accounts array...");
    user.accounts = [];
    await user.save();
  }
  return user;
}
```

```js
async function addToUser(user, data) {
  const AccountData = {
    ...data,
  };

  const AccountIndex = user.accounts.findIndex((account) => account.name === data.name);
  if (AccountIndex !== -1) {
    user.accounts[AccountIndex] = AccountData;
    console.log("found index", AccountIndex);
  } else {
    user.accounts.push(AccountData);
    console.log("pushing...");
  }
  await user.save();
}
```

```js
async function updateUser(user, data) {
  const AccountData = {
    ...data,
  };

  const AccountIndex = user.accounts.findIndex((account) => account.name === data.name);
  if (AccountIndex !== -1) {
  const existingAccount = user.accounts[AccountIndex];
    user.accounts[AccountIndex] = {
    ...existingAccount, ...AccountData,
    };
    console.log("found index", AccountIndex);
  } else {
    user.accounts.push(AccountData);
    console.log("pushing...");
  }
  await user.save();
}
```

USAGE

```js
    const user = await createUser(mobile);
    
	await addToUser(user, {
      name: "Faircent",
      id: fResponse.data.result.loan_id,
      status: fResponse.data.result.status,
      req: data,
      res: fResponse.data,
    });
```