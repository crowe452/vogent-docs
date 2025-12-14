Phone Numbers

Purchase available number (deprecated, use /phone_numbers instead)



  



        



        



    



        



        



              



        



  



      



              


Purchase available number (deprecated, use /phone_numbers instead)

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/phone_numbers/purchase \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "number": "<string>" } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "number": "+18001234567", "type": "PSTN", "agentId": "<string>" }`
```

Phone Numbers

# Purchase available number (deprecated, use /phone_numbers instead)

Purchase an available phone number.

POST

/

phone_numbers

/

purchase

Try it

Purchase available number (deprecated, use /phone_numbers instead)

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/phone_numbers/purchase \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "number": "<string>" } '`
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

#### Body

application/json

[​](#body-number)

number

string

required

The number as returned by the phone number search endpoint.

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

[Search for available numbers](/api-reference/search-for-available-numbers)[Delete Phone Number](/api-reference/delete-phone-number)