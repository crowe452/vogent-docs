Extractors

Update extractor



  



        



        



    



        



        



              



        



  



      



              


Update extractor

cURL

Copy

```
`curl --request PUT \ --url https://api.vogent.ai/api/agents/{agentId}/extractors/{extractorId} \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "name": "<string>", "extractorFieldsJsonSchema": "<string>" } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "extractorFieldsJsonSchema": "<string>" }`
```

Extractors

# Update extractor

Update an extractor for a given agent.

PUT

/

agents

/

{agentId}

/

extractors

/

{extractorId}

Try it

Update extractor

cURL

Copy

```
`curl --request PUT \ --url https://api.vogent.ai/api/agents/{agentId}/extractors/{extractorId} \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "name": "<string>", "extractorFieldsJsonSchema": "<string>" } '`
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

[​](#parameter-extractor-id)

extractorId

string

required

ID of the extractor.

#### Body

application/json

Update an extractor

[​](#body-name)

name

string

[​](#body-extractor-fields-json-schema)

extractorFieldsJsonSchema

string

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

[Create extractor](/api-reference/create-extractor)[List phone numbers](/api-reference/list-phone-numbers)