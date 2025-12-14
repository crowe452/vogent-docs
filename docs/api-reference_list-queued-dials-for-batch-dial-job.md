Batch Dials

List Queued Batch Dials



  



        



        



    



        



        



              



        



  



      



              


List Queued Batch Dials

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/batch_dial_jobs/{id}/queue \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "toNumber": "<string>", "batchDialJobId": "<string>", "createdAt": "2023-11-07T05:31:56Z", "inputs": {} } ], "cursor": "<string>" }`
```

Batch Dials

# List Queued Batch Dials

Lists all rows that are queued as part of the batch job.

GET

/

batch_dial_jobs

/

{id}

/

queue

Try it

List Queued Batch Dials

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/batch_dial_jobs/{id}/queue \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "toNumber": "<string>", "batchDialJobId": "<string>", "createdAt": "2023-11-07T05:31:56Z", "inputs": {} } ], "cursor": "<string>" }`
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

#### Query Parameters

[​](#parameter-limit)

limit

integer

The number of specs to return.

[​](#parameter-cursor)

cursor

string

The cursor for pagination.

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

[​](#response-data-items-to-number)

data.toNumber

string

required

[​](#response-data-items-batch-dial-job-id)

data.batchDialJobId

string

required

[​](#response-data-items-created-at)

data.createdAt

string<date-time>

required

[​](#response-data-items-inputs)

data.inputs

object

Show child attributes

[​](#response-data-items-inputs-additional-properties)

data.inputs.{key}

any

[​](#response-cursor-one-of-0)

cursor

string | null

required

[Update Batch Job](/api-reference/update-batch-dial-job)[Pause/Resume Batch Job](/api-reference/set-batch-dial-job-paused)