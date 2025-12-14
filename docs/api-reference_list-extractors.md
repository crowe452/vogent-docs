Extractors

List extractors



  



        



        



    



        



        



              



        



  



      



              


List extractors

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/agents/{agentId}/extractors \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "extractors": [ { "id": "<string>", "name": "<string>", "extractorFieldsJsonSchema": "<string>" } ] }`
```

Extractors

# List extractors

List all extractors for a given agent.

GET

/

agents

/

{agentId}

/

extractors

Try it

List extractors

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/agents/{agentId}/extractors \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "extractors": [ { "id": "<string>", "name": "<string>", "extractorFieldsJsonSchema": "<string>" } ] }`
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

#### Response

200

application/json

Successful operation

[​](#response-extractors)

extractors

object[]

required

Show child attributes

[​](#response-extractors-items-id)

extractors.id

string

required

[​](#response-extractors-items-name)

extractors.name

string

required

[​](#response-extractors-items-extractor-fields-json-schema)

extractors.extractorFieldsJsonSchema

string

required

[Get extractor](/api-reference/get-extractor)[Create extractor](/api-reference/create-extractor)