Functions

Delete function



  



        



        



    



        



        



              



        



  



      



              


Delete function

cURL

Copy

```
`curl --request DELETE \ --url https://api.vogent.ai/api/functions/{id} \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "description": "<string>", "type": "transfer", "allowedNumbers": [ { "number": "<string>" } ], "lifecycleMessages": { "started": [ "<string>" ] } }`
```

Functions

# Delete function

Deletes a function, and unlinks it from any agents.

DELETE

/

functions

/

{id}

Try it

Delete function

cURL

Copy

```
`curl --request DELETE \ --url https://api.vogent.ai/api/functions/{id} \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "description": "<string>", "type": "transfer", "allowedNumbers": [ { "number": "<string>" } ], "lifecycleMessages": { "started": [ "<string>" ] } }`
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

ID of the function.

#### Response

200

application/json

Successful operation

  * Transfer

  * API




[​](#response-one-of-0-id)

id

string

required

[​](#response-one-of-0-name)

name

string

required

The name of the function.

[​](#response-one-of-0-description)

description

string

required

A description of what the function does.

[​](#response-one-of-0-type)

type

enum<string>

required

Available options: 

`transfer`, 

`api`

[​](#response-one-of-0-allowed-numbers)

allowedNumbers

object[]

required

The numbers that the agent is allowed to transfer to.

Show child attributes

[​](#response-one-of-0-allowed-numbers-items-number)

allowedNumbers.number

string

required

The number in e.164 format.

[​](#response-one-of-0-lifecycle-messages)

lifecycleMessages

object

Messages to display during function execution lifecycle events.

Show child attributes

[​](#response-one-of-0-lifecycle-messages-started)

lifecycleMessages.started

string[]

required

Messages to display when the function starts executing. One will be chosen at random.

[Update function](/api-reference/update-function)[List Models](/api-reference/list-models)