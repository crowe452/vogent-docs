Functions

Create a function



  



        



        



    



        



        



              



        



  



      



              


Create a function

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/functions \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "name": "<string>", "description": "<string>", "allowedNumbers": [ { "number": "<string>" } ], "type": "transfer", "lifecycleMessages": { "started": [ "<string>" ] } } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "description": "<string>", "type": "transfer", "allowedNumbers": [ { "number": "<string>" } ], "lifecycleMessages": { "started": [ "<string>" ] } }`
```

Functions

# Create a function

Creates a function.

POST

/

functions

Try it

Create a function

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/functions \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "name": "<string>", "description": "<string>", "allowedNumbers": [ { "number": "<string>" } ], "type": "transfer", "lifecycleMessages": { "started": [ "<string>" ] } } '`
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

#### Body

application/json

  * Transfer

  * API




[​](#body-one-of-0-name)

name

string

required

The name of the function.

[​](#body-one-of-0-description)

description

string

required

A description of what the function does.

[​](#body-one-of-0-allowed-numbers)

allowedNumbers

object[]

required

The numbers that the agent is allowed to transfer to in e.164 format (+11234567890).

Show child attributes

[​](#body-one-of-0-allowed-numbers-items-number)

allowedNumbers.number

string

required

The number in e.164 format.

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

[Delete Phone Number](/api-reference/delete-phone-number)[Get function](/api-reference/get-function)