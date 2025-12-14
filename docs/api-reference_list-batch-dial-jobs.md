Batch Dials

List Batch Jobs



  



        



        



    



        



        



              



        



  



      



              


List Batch Jobs

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/batch_dial_jobs \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "maxConcurrentDials": 123, "name": "<string>", "status": "INIT", "callAgentId": "<string>", "createdAt": "2023-11-07T05:31:56Z", "fromPhoneNumberIds": [ "<string>" ], "schedule": { "days": [ { "dayOfWeek": 123, "timeSlots": [ { "startTime": "<string>", "endTime": "<string>" } ] } ], "timezone": "<string>" } } ], "cursor": "<string>" }`
```

Batch Dials

# List Batch Jobs

Lists batch dial jobs for the workspace.

GET

/

batch_dial_jobs

Try it

List Batch Jobs

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/batch_dial_jobs \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "maxConcurrentDials": 123, "name": "<string>", "status": "INIT", "callAgentId": "<string>", "createdAt": "2023-11-07T05:31:56Z", "fromPhoneNumberIds": [ "<string>" ], "schedule": { "days": [ { "dayOfWeek": 123, "timeSlots": [ { "startTime": "<string>", "endTime": "<string>" } ] } ], "timezone": "<string>" } } ], "cursor": "<string>" }`
```

#### Authorizations

[​](#authorization-authorization)

Authorization

string

header

required

In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.

#### Query Parameters

[​](#parameter-limit)

limit

integer

The number of jobs to return.

[​](#parameter-cursor)

cursor

string

The cursor for pagination.

[​](#parameter-status)

status

enum<string>

Available options: 

`INIT`, 

`ACTIVE`, 

`PAUSED`, 

`COMPLETE`, 

`CANCELLED`

[​](#parameter-call-agent-id)

callAgentId

string

[​](#parameter-user-id)

userId

string

#### Response

200

application/json

Successful operation

[​](#response-data)

data

object[]

required

Show child attributes

[​](#response-data-items-id)

data.id

string

required

[​](#response-data-items-max-concurrent-dials)

data.maxConcurrentDials

integer

required

[​](#response-data-items-name)

data.name

string

required

[​](#response-data-items-status)

data.status

enum<string>

required

Available options: 

`INIT`, 

`ACTIVE`, 

`PAUSED`, 

`COMPLETE`, 

`CANCELLED`

[​](#response-data-items-call-agent-id)

data.callAgentId

string

required

[​](#response-data-items-created-at)

data.createdAt

string<date-time>

required

[​](#response-data-items-from-phone-number-ids)

data.fromPhoneNumberIds

string[]

[​](#response-data-items-schedule-one-of-0)

data.schedule

object

Show child attributes

[​](#response-data-items-schedule-one-of-0-days)

data.schedule.days

object[]

required

Show child attributes

[​](#response-data-items-schedule-one-of-0-days-items-day-of-week)

data.schedule.days.dayOfWeek

integer

required

[​](#response-data-items-schedule-one-of-0-days-items-time-slots)

data.schedule.days.timeSlots

object[]

required

Show child attributes

[​](#response-data-items-schedule-one-of-0-days-items-time-slots-items-start-time)

data.schedule.days.timeSlots.startTime

string

required

[​](#response-data-items-schedule-one-of-0-days-items-time-slots-items-end-time)

data.schedule.days.timeSlots.endTime

string

required

[​](#response-data-items-schedule-one-of-0-timezone)

data.schedule.timezone

string

required

[​](#response-cursor-one-of-0)

cursor

string | null

required

[Websocket TTS](/api-reference/voicelab-websocket-tts)[Create Batch Job](/api-reference/create-a-new-batch-dial-job)