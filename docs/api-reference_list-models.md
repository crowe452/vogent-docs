Models

List Models



  



        



        



    



        



        



              



        



  



      



              


List Models

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/models \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "name": "<string>", "modelOptions": [ { "id": "<string>", "name": "<string>", "valueType": "STRING", "default": "<string>" } ] } ], "cursor": "<string>" }`
```

Models

# List Models

List the models available on your account.

GET

/

models

Try it

List Models

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/models \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "name": "<string>", "modelOptions": [ { "id": "<string>", "name": "<string>", "valueType": "STRING", "default": "<string>" } ] } ], "cursor": "<string>" }`
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

The maximum number of records to fetch.

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

[​](#response-data-items-name)

data.name

string

required

[​](#response-data-items-model-options)

data.modelOptions

object[]

required

Show child attributes

[​](#response-data-items-model-options-items-id)

data.modelOptions.id

string

required

[​](#response-data-items-model-options-items-name)

data.modelOptions.name

string

required

[​](#response-data-items-model-options-items-value-type)

data.modelOptions.valueType

enum<string>

required

Available options: 

`STRING`, 

`INT`, 

`FLOAT`

[​](#response-data-items-model-options-items-default)

data.modelOptions.default

string

required

[​](#response-cursor-one-of-0)

cursor

string | null

required

A cursor you can pass to /agents to fetch the next page. If no next page exists, the cursor will be null.

[Delete function](/api-reference/delete-function)[Run TTS Model](/api-reference/run-tts-model)