Phone Numbers

Update Phone Number



  



        



        



    



        



        



              



        



  



      



              


Update Phone Number

cURL

Copy

```
`curl --request PUT \ --url https://api.vogent.ai/api/phone_numbers/{id} \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "agentId": "<string>" } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "number": "+18001234567", "type": "PSTN", "agentId": "<string>" }`
```

Phone Numbers

# Update Phone Number

Update a phone number’s properties

PUT

/

phone_numbers

/

{id}

Try it

Update Phone Number

cURL

Copy

```
`curl --request PUT \ --url https://api.vogent.ai/api/phone_numbers/{id} \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "agentId": "<string>" } '`
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

#### Body

application/json

Update phone number properties

[​](#body-agent-id)

agentId

string

The ID of the agent to link this phone number to. Set to the empty string to unlink an agent.

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

[Get Phone Number](/api-reference/get-phone-number)[Create a phone number](/api-reference/create-number)