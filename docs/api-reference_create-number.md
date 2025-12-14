Phone Numbers

Create a phone number



  



        



        



    



        



        



              



        



  



      



              


Create a phone number

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/phone_numbers \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "type": "purchase", "purchase": { "number": "<string>" }, "sipImport": { "phoneNumber": "<string>", "terminationUri": "<string>", "username": "<string>", "password": "<string>" }, "vogentSip": { "sipPrefix": "<string>", "username": "<string>", "password": "<string>" } } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "number": "+18001234567", "type": "PSTN", "agentId": "<string>" }`
```

Phone Numbers

# Create a phone number

Creates a phone number of various types (purchase, SIP import, or Vogent SIP).

POST

/

phone_numbers

Try it

Create a phone number

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/phone_numbers \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "type": "purchase", "purchase": { "number": "<string>" }, "sipImport": { "phoneNumber": "<string>", "terminationUri": "<string>", "username": "<string>", "password": "<string>" }, "vogentSip": { "sipPrefix": "<string>", "username": "<string>", "password": "<string>" } } '`
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

Create a new phone number

[​](#body-type)

type

enum<string>

required

The type of phone number creation operation.

Available options: 

`purchase`, 

`sip_import`, 

`vogent_sip`

[​](#body-purchase-one-of-0)

purchase

object

Required when type is 'purchase'.

Show child attributes

[​](#body-purchase-one-of-0-number)

purchase.number

string

required

The number as returned by the phone number search endpoint.

[​](#body-sip-import-one-of-0)

sipImport

object

Required when type is 'sip_import'.

Show child attributes

[​](#body-sip-import-one-of-0-phone-number)

sipImport.phoneNumber

string

required

The phone number in E.164 format.

[​](#body-sip-import-one-of-0-termination-uri)

sipImport.terminationUri

string

required

The termination URI for the SIP trunk.

[​](#body-sip-import-one-of-0-username)

sipImport.username

string

required

The username for SIP authentication.

[​](#body-sip-import-one-of-0-password)

sipImport.password

string

required

The password for SIP authentication.

[​](#body-vogent-sip-one-of-0)

vogentSip

object

Required when type is 'vogent_sip'.

Show child attributes

[​](#body-vogent-sip-one-of-0-sip-prefix)

vogentSip.sipPrefix

string

required

The SIP prefix/username.

[​](#body-vogent-sip-one-of-0-username)

vogentSip.username

string

required

The username for SIP authentication (minimum 5 characters).

[​](#body-vogent-sip-one-of-0-password)

vogentSip.password

string

required

The password for SIP authentication (minimum 5 characters).

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

[Update Phone Number](/api-reference/update-phone-number)[Search for available numbers](/api-reference/search-for-available-numbers)