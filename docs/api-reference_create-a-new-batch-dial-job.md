Batch Dials

Create Batch Job



  



        



        



    



        



        



              



        



  



      



              


Create Batch Job

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/batch_dial_jobs \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "callAgentId": "<string>", "maxConcurrentDials": 123, "name": "<string>", "rows": [ { "toNumber": "<string>", "inputs": {} } ], "fromPhoneNumberIds": [ "<string>" ], "schedule": { "days": [ { "dayOfWeek": 123, "timeSlots": [ { "startTime": "<string>", "endTime": "<string>" } ] } ], "timezone": "<string>", "disableSchedule": true } } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "maxConcurrentDials": 123, "name": "<string>", "status": "INIT", "callAgentId": "<string>", "createdAt": "2023-11-07T05:31:56Z", "fromPhoneNumberIds": [ "<string>" ], "schedule": { "days": [ { "dayOfWeek": 123, "timeSlots": [ { "startTime": "<string>", "endTime": "<string>" } ] } ], "timezone": "<string>" } }`
```

Batch Dials

# Create Batch Job

Creates a new batch dial job. You must start the job with the `/paused` endpoint for calls to begin.

POST

/

batch_dial_jobs

Try it

Create Batch Job

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/batch_dial_jobs \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "callAgentId": "<string>", "maxConcurrentDials": 123, "name": "<string>", "rows": [ { "toNumber": "<string>", "inputs": {} } ], "fromPhoneNumberIds": [ "<string>" ], "schedule": { "days": [ { "dayOfWeek": 123, "timeSlots": [ { "startTime": "<string>", "endTime": "<string>" } ] } ], "timezone": "<string>", "disableSchedule": true } } '`
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

#### Body

application/json

[​](#body-call-agent-id)

callAgentId

string

required

[​](#body-max-concurrent-dials)

maxConcurrentDials

integer

required

[​](#body-name)

name

string

required

[​](#body-rows)

rows

object[]

required

Show child attributes

[​](#body-rows-items-to-number)

rows.toNumber

string

required

[​](#body-rows-items-inputs)

rows.inputs

object

Must be a string => string map.

Show child attributes

[​](#body-rows-items-inputs-additional-properties)

rows.inputs.{key}

any

[​](#body-from-phone-number-ids)

fromPhoneNumberIds

string[]

[​](#body-schedule-one-of-0)

schedule

object

Show child attributes

[​](#body-schedule-one-of-0-days)

schedule.days

object[]

required

Show child attributes

[​](#body-schedule-one-of-0-days-items-day-of-week)

schedule.days.dayOfWeek

integer

required

[​](#body-schedule-one-of-0-days-items-time-slots)

schedule.days.timeSlots

object[]

required

Show child attributes

[​](#body-schedule-one-of-0-days-items-time-slots-items-start-time)

schedule.days.timeSlots.startTime

string

required

[​](#body-schedule-one-of-0-days-items-time-slots-items-end-time)

schedule.days.timeSlots.endTime

string

required

[​](#body-schedule-one-of-0-timezone)

schedule.timezone

string

required

[​](#body-schedule-one-of-0-disable-schedule)

schedule.disableSchedule

boolean

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

[List Batch Jobs](/api-reference/list-batch-dial-jobs)[Get Batch Job](/api-reference/get-batch-dial-job)