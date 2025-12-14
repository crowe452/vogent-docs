Phone Numbers

List phone numbers



  



        



        



    



        



        



              



        



  



      



              


List phone numbers

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/phone_numbers \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "number": "+18001234567", "type": "PSTN", "agentId": "<string>" } ], "cursor": "<string>" }`
```

Phone Numbers

# List phone numbers

List phone numbers in your workspace.

GET

/

phone_numbers

Try it

List phone numbers

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/phone_numbers \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "number": "+18001234567", "type": "PSTN", "agentId": "<string>" } ], "cursor": "<string>" }`
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

default:100

The maximum number of phone numbers to list.

[​](#parameter-cursor)

cursor

string

The pagination cursor returned by the previous request. Feed the result provided by vogent verbatim.

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

[​](#response-data-items-number)

data.number

string

required

The number in e.164 format, or the SIP username, if the type is SIP_USERNAME.

Example:

`"+18001234567"`

[​](#response-data-items-type)

data.type

enum<string>

required

Available options: 

`PSTN`, 

`SIP_USERNAME`

[​](#response-data-items-agent-id-one-of-0)

data.agentId

string | null

required

The ID of the linked agent, if the phone number is linked to one.

[​](#response-cursor-one-of-0)

cursor

string | null

required

A cursor you can pass to fetch the next page. If no next page exists, the cursor will be null.

[Update extractor](/api-reference/update-extractor)[Get Phone Number](/api-reference/get-phone-number)