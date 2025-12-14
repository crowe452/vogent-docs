Dials

Get Dial Token



  



        



        



    



        



        



              



        



  



      



              


Get Dial Token

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/dials/{id}/token \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "dialToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZXN0IjoidGVzdCJ9.9EQaLsDRKDVXLUVLR9JgDTjEULaT2-OMbHayQAzgZH8" }`
```

Dials

# Get Dial Token

Gets a token for a given dial.

POST

/

dials

/

{id}

/

token

Try it

Get Dial Token

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/dials/{id}/token \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "dialToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZXN0IjoidGVzdCJ9.9EQaLsDRKDVXLUVLR9JgDTjEULaT2-OMbHayQAzgZH8" }`
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

ID of the dial.

#### Response

200

application/json

Successful operation

[​](#response-dial-token)

dialToken

string

required

You can pass this dial token to Elto's web UI, or use this token to authorize any requests for this dial. It's safe to pass this token to a client -- it only allows users to run requests against the dial associated with this session.

Example:

`"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZXN0IjoidGVzdCJ9.9EQaLsDRKDVXLUVLR9JgDTjEULaT2-OMbHayQAzgZH8"`

[Get Dial](/api-reference/get-dial)[List Agents](/api-reference/list-agents)