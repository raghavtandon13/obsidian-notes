```bash
curl --location 'https://mltm.ivrobd.com/api/v1/astrixdispatcher/v2/lead?isDND=true' \
--header 'Content-Type: application/json' \
--data '{
    "leadName": "data_04042024",
    "campaignId": "1566",
    "userId": 116,
    "ukey": "971XCfS3czzXuI4t",
    "retryInfo": {
        "retryType": "R",
        "retryOnFail": 3,
        "retryTimeOnFail": 30,
        "retryOnBusy": 3,
        "retryTimeOnBusy": 30,
        "retryOnAns": 0,
        "retryTimeOnAns": 0,
        "retryOnNoAns": 3,
        "retryTimeOnNoAns": 30,
        "noOfRetry": 3
    },
    "leadSchedule": {
        "scheduleDay": "1,2,3,4,5,6,7",
        "scheduleStartDtm": "2024-04-04 13:05:00",
        "scheduleEndDtm": "2024-04-04 13:07:59"
    },
    "phoneNumberDetails": [
        {
            "phoneNumber": "9289387338"
        }
    ]
}'

```