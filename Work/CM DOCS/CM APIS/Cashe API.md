# Stage 1 - Dedupe Check
```json
    {
        partner_name: "CredMantra_Partner1", // DO NOT CHNAGE
        mobile_no: "8094634634", 
        email_id: "ragahv@credmantra.com",
    };
```

```
https://credmantra.com/api/v1/partner-api/cashe/checkDuplicateLead
```
 If Payload  === "NO" then move to stage 2 else show "Customer Already Registered with Cashe"