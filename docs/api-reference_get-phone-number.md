Phone Numbers

Get Phone Number



  



        



        



    



        



        



              



        



  



      



              


Get Phone Number

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/phone_numbers/{id} \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "number": "+18001234567", "type": "PSTN", "agentId": "<string>" }`
```

Phone Numbers

# Get Phone Number

Retrieve a phone number

GET

/

phone_numbers

/

{id}

Try it

Get Phone Number

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/phone_numbers/{id} \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "number": "+18001234567", "type": "PSTN", "agentId": "<string>" }`
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

ID of the versioned prompt.

#### Response

200

application/json

Successful operation

[​](#response-id)

id

string

required

[​](#response-number)

number

string

required

The number in e.164 format, or the SIP username, if the type is SIP_USERNAME.

Example:

`"+18001234567"`

[​](#response-type)

type

enum<string>

required

Available options: 

`PSTN`, 

`SIP_USERNAME`

[​](#response-agent-id-one-of-0)

agentId

string | null

required

The ID of the linked agent, if the phone number is linked to one.

[List phone numbers](/api-reference/list-phone-numbers)[Update Phone Number](/api-reference/update-phone-number)