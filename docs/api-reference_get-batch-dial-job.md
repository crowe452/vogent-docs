Batch Dials

Get Batch Job



  



        



        



    



        



        



              



        



  



      



              


Get Batch Job

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/batch_dial_jobs/{id} \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "maxConcurrentDials": 123, "name": "<string>", "status": "INIT", "callAgentId": "<string>", "createdAt": "2023-11-07T05:31:56Z", "fromPhoneNumberIds": [ "<string>" ], "schedule": { "days": [ { "dayOfWeek": 123, "timeSlots": [ { "startTime": "<string>", "endTime": "<string>" } ] } ], "timezone": "<string>" } }`
```

Batch Dials

# Get Batch Job

Get metadata for a batch dial job.

GET

/

batch_dial_jobs

/

{id}

Try it

Get Batch Job

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/batch_dial_jobs/{id} \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "maxConcurrentDials": 123, "name": "<string>", "status": "INIT", "callAgentId": "<string>", "createdAt": "2023-11-07T05:31:56Z", "fromPhoneNumberIds": [ "<string>" ], "schedule": { "days": [ { "dayOfWeek": 123, "timeSlots": [ { "startTime": "<string>", "endTime": "<string>" } ] } ], "timezone": "<string>" } }`
```

#### Authorizations

[​](#authorization-authorization)

Authorization

string

header

required

In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.

#### Path Parameters

[​](#parameter-id)

id

string

required

ID of the batch dial job.

#### Response

200

application/json

Successful operation

[​](#response-id)

id

string

required

[​](#response-max-concurrent-dials)

maxConcurrentDials

integer

required

[​](#response-name)

name

string

required

[​](#response-status)

status

enum<string>

required

Available options: 

`INIT`, 

`ACTIVE`, 

`PAUSED`, 

`COMPLETE`, 

`CANCELLED`

[​](#response-call-agent-id)

callAgentId

string

required

[​](#response-created-at)

createdAt

string<date-time>

required

[​](#response-from-phone-number-ids)

fromPhoneNumberIds

string[]

[​](#response-schedule-one-of-0)

schedule

object

Show child attributes

[​](#response-schedule-one-of-0-days)

schedule.days

object[]

required

Show child attributes

[​](#response-schedule-one-of-0-days-items-day-of-week)

schedule.days.dayOfWeek

integer

required

[​](#response-schedule-one-of-0-days-items-time-slots)

schedule.days.timeSlots

object[]

required

Show child attributes

[​](#response-schedule-one-of-0-days-items-time-slots-items-start-time)

schedule.days.timeSlots.startTime

string

required

[​](#response-schedule-one-of-0-days-items-time-slots-items-end-time)

schedule.days.timeSlots.endTime

string

required

[​](#response-schedule-one-of-0-timezone)

schedule.timezone

string

required

[Create Batch Job](/api-reference/create-a-new-batch-dial-job)[Update Batch Job](/api-reference/update-batch-dial-job)