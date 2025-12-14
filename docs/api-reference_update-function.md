Functions

Update function



  



        



        



    



        



        



              



        



  



      



              


Update function

cURL

Copy

```
`curl --request PUT \ --url https://api.vogent.ai/api/functions/{id} \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "allowedNumbers": [ { "number": "<string>" } ], "name": "<string>", "description": "<string>", "type": "transfer", "lifecycleMessages": { "started": [ "<string>" ] } } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "description": "<string>", "type": "transfer", "allowedNumbers": [ { "number": "<string>" } ], "lifecycleMessages": { "started": [ "<string>" ] } }`
```

Functions

# Update function

Updates a specific function.

PUT

/

functions

/

{id}

Try it

Update function

cURL

Copy

```
`curl --request PUT \ --url https://api.vogent.ai/api/functions/{id} \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "allowedNumbers": [ { "number": "<string>" } ], "name": "<string>", "description": "<string>", "type": "transfer", "lifecycleMessages": { "started": [ "<string>" ] } } '`
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

#### Body

application/json

Update function properties

  * Transfer

  * API




[​](#body-one-of-0-allowed-numbers)

allowedNumbers

object[]

required

The numbers that the agent is allowed to transfer to.

Show child attributes

[​](#body-one-of-0-allowed-numbers-items-number)

allowedNumbers.number

string

required

The number in e.164 format.

[​](#body-one-of-0-name)

name

string

The name of the function.

[​](#body-one-of-0-description)

description

string

A description of what the function does.

[​](#body-one-of-0-type)

type

enum<string>

Available options: 

`transfer`, 

`api`

[​](#body-one-of-0-lifecycle-messages)

lifecycleMessages

object

Messages to display during function execution lifecycle events.

Show child attributes

[​](#body-one-of-0-lifecycle-messages-started)

lifecycleMessages.started

string[]

required

Messages to display when the function starts executing. One will be chosen at random.

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

[Get function](/api-reference/get-function)[Delete function](/api-reference/delete-function)