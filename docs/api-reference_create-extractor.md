Extractors

Create extractor



  



        



        



    



        



        



              



        



  



      



              


Create extractor

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/agents/{agentId}/extractors \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "name": "<string>", "extractorFieldsJsonSchema": "<string>" } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "extractorFieldsJsonSchema": "<string>" }`
```

Extractors

# Create extractor

Create a new extractor for a given agent.

POST

/

agents

/

{agentId}

/

extractors

Try it

Create extractor

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/agents/{agentId}/extractors \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "name": "<string>", "extractorFieldsJsonSchema": "<string>" } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "extractorFieldsJsonSchema": "<string>" }`
```

#### Authorizations

[​](#authorization-authorization)

Authorization

string

header

required

In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.

#### Path Parameters

[​](#parameter-agent-id)

agentId

string

required

ID of the agent.

#### Body

application/json

Create a new extractor

[​](#body-name)

name

string

required

[​](#body-extractor-fields-json-schema)

extractorFieldsJsonSchema

string

required

#### Response

200

application/json

Successful operation

[​](#response-id)

id

string

required

[​](#response-name)

name

string

required

[​](#response-extractor-fields-json-schema)

extractorFieldsJsonSchema

string

required

[List extractors](/api-reference/list-extractors)[Update extractor](/api-reference/update-extractor)