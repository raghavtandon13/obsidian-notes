---
id: cm-apis
aliases:
  - CM APIs
tags: []
---

# CM APIs

- Fibe - Live in Prod
- Cashe - Live in Prod (major pending)

-----------

- Faircent - Live in UAT
  - requires another upload
  - asked about udyam document
  - added two docs (ITR and udyam)
  - meeting today
- Upwads - Live in UAT
  - requires consent thing
  - asked for exact consent text
- LendingKArt - Live in UAT (major pending)
  - had meeting today (19-feb)
  - x-api-key is valid in UAT

-----------

- MoneyTap -  front back complete (credentials not working, ip whitelist maybe ?)
- Finnable - front back complete (no meeting yet)
- Finzy - front back complete (no meeting yet)

----------------------------------------------------------------
----------------------------------------------------------------
curl --location '<https://lkext.lendingkart.com/admin/lead/v2/partner/leads/create-application>' \
--header 'Content-Type: application/json' \
--header 'X-Api-Key: 2e067259-5f4a-4ed1-880f-ece8e7b1b9dd' \
--data-raw '{
  "businessRunBy": "Self",
  "companyEmail": "<hemusingh12@bajaj.co.in>",
  "consentDatetime": "2024-02-21T05:11:58.099Z",
  "email": "<gemu44@gmail.com>",
  "firstName": "hinanshu",
  "lastName": "singh",
  "mobile": 7994470867,
  "natureOfBusiness": ["Importer"],
  "personalAadhaar": "987865479807",
  "personalDob": "1991-09-13",
  "personalPAN": "BUSPR0451L",
  "productCategory": "Advisory services (legal, business, educational, psychological etc.)",
  "registeredAs": "Proprietorship",
  "consent": true,
  "businessRevenue": 1000000,
  "businessAge": 50
}'

- [ ] business age
- [ ] business revenue
- [ ] nature of business shoulbe be an array
- [x] company email not correct
- [ ]
- [ ]
- [ ]
