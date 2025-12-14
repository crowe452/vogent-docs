Dials

Hangup Dial.



  



        



        



    



        



        



              



        



  



      



              


Hangup Dial.

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/dials/{id}/hangup \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "success": true }`
```

Dials

# Hangup Dial.

Hangs up an in-progress dial.

POST

/

dials

/

{id}

/

hangup

Try it

Hangup Dial.

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/dials/{id}/hangup \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "success": true }`
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

[​](#response-success)

success

boolean

required

Example:

`true`

[Create a new dial](/api-reference/create-a-new-dial)[Get Dial](/api-reference/get-dial)