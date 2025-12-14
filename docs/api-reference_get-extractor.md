Extractors

Get extractor



  



        



        



    



        



        



              



        



  



      



              


Get extractor

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/agents/{agentId}/extractors/{extractorId} \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "extractorFieldsJsonSchema": "<string>" }`
```

Extractors

# Get extractor

Get an extractor for a given agent.

GET

/

agents

/

{agentId}

/

extractors

/

{extractorId}

Try it

Get extractor

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/agents/{agentId}/extractors/{extractorId} \ --header 'Authorization: Bearer <token>'`
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

[Create versioned prompt](/api-reference/create-versioned-prompt)[List extractors](/api-reference/list-extractors)