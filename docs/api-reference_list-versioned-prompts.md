Versioned Prompts

List versioned prompts



  



        



        



    



        



        



              



        



  



      



              


List versioned prompts

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/agents/{agentId}/versioned_prompts \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "name": "<string>", "agentType": "STANDARD", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {}, "outputSchema": "<string>" } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "aiModelId": "<string>", "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] } ], "cursor": "<string>" }`
```

Versioned Prompts

# List versioned prompts

Lists versioned prompts for a given agent.

GET

/

agents

/

{agentId}

/

versioned_prompts

Try it

List versioned prompts

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/agents/{agentId}/versioned_prompts \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "name": "<string>", "agentType": "STANDARD", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {}, "outputSchema": "<string>" } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "aiModelId": "<string>", "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] } ], "cursor": "<string>" }`
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

#### Query Parameters

[​](#parameter-limit)

limit

integer

default:100

The maximum number of prompts to list.

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

Unique identifier for the versioned prompt

[​](#response-data-items-name)

data.name

string

required

Human-readable name for the versioned prompt

[​](#response-data-items-agent-type)

data.agentType

enum<string>

required

The type of agent this prompt is designed for (STANDARD or CUSTOM_FLOW)

Available options: 

`STANDARD`, 

`CUSTOM_FLOW`

[​](#response-data-items-prompt-one-of-0)

data.prompt

string | null

required

The actual prompt content that will be used by the agent. Can be null for CUSTOM_FLOW agent types

[​](#response-data-items-flow-definition-one-of-0)

data.flowDefinition

object

The flow definition for the agent. Only defined for CUSTOM_FLOW agent types.

Show child attributes

[​](#response-data-items-flow-definition-one-of-0-nodes)

data.flowDefinition.nodes

object[]

required

Show child attributes

[​](#response-data-items-flow-definition-one-of-0-nodes-items-id)

data.flowDefinition.nodes.id

string

required

[​](#response-data-items-flow-definition-one-of-0-nodes-items-name)

data.flowDefinition.nodes.name

string

required

[​](#response-data-items-flow-definition-one-of-0-nodes-items-type)

data.flowDefinition.nodes.type

string

required

The node type. View the available types at <https://docs.vogent.ai/flow>.

[​](#response-data-items-flow-definition-one-of-0-nodes-items-transition-rules)

data.flowDefinition.nodes.transitionRules

object[]

required

Show child attributes

[​](#response-data-items-flow-definition-one-of-0-nodes-items-transition-rules-items-condition-type)

data.flowDefinition.nodes.transitionRules.conditionType

enum<string>

required

The condition used to evaluate the transition rule. If language, the value will be used as a natural language condition to describe when to execute a transition.

Available options: 

`always`, 

`equal`, 

`in`, 

`greater`, 

`less`, 

`language`

[​](#response-data-items-flow-definition-one-of-0-nodes-items-transition-rules-items-transition-node-id)

data.flowDefinition.nodes.transitionRules.transitionNodeId

string

required

[​](#response-data-items-flow-definition-one-of-0-nodes-items-transition-rules-items-array-condition-type-one-of-0)

data.flowDefinition.nodes.transitionRules.arrayConditionType

enum<string> | null

The type of array condition to apply. 'any' means at least one element must match, 'all' means all elements must match.

Available options: 

`any`, 

`all`

[​](#response-data-items-flow-definition-one-of-0-nodes-items-transition-rules-items-field-one-of-0)

data.flowDefinition.nodes.transitionRules.field

string | null

[​](#response-data-items-flow-definition-one-of-0-nodes-items-transition-rules-items-value-one-of-0)

data.flowDefinition.nodes.transitionRules.value

string | null

[​](#response-data-items-flow-definition-one-of-0-nodes-items-transition-rules-items-values-one-of-0)

data.flowDefinition.nodes.transitionRules.values

string[] | null

[​](#response-data-items-flow-definition-one-of-0-nodes-items-node-data)

data.flowDefinition.nodes.nodeData

object

required

The node-specific configuration. View the schemas by type at <https://docs.vogent.ai/flow>.

[​](#response-data-items-flow-definition-one-of-0-nodes-items-output-schema-one-of-0)

data.flowDefinition.nodes.outputSchema

string | null

The JSON schema describing the output of this node. This is generated automatically from the node type and node data.

[​](#response-data-items-flow-definition-one-of-0-global-context-one-of-0)

data.flowDefinition.globalContext

string | null

required

[​](#response-data-items-flow-definition-one-of-0-ai-open)

data.flowDefinition.aiOpen

boolean

required

Deprecated, use openingLineType instead.

[​](#response-data-items-flow-definition-one-of-0-opening-line-type)

data.flowDefinition.openingLineType

enum<string>

required

Available options: 

`INBOUND_ONLY`, 

`INBOUND_OUTBOUND`, 

`NONE`

[​](#response-data-items-ai-model-id)

data.aiModelId

string

The AI model ID to use for the agent.

[​](#response-data-items-model-option-values)

data.modelOptionValues

object[]

Show child attributes

[​](#response-data-items-model-option-values-items-option-id)

data.modelOptionValues.optionId

string

required

The ID of option.

[​](#response-data-items-model-option-values-items-value)

data.modelOptionValues.value

string

required

[​](#response-cursor-one-of-0)

cursor

string | null

required

A cursor you can pass to fetch the next page. If no next page exists, the cursor will be null.

[List Voices](/api-reference/list-voices)[Get versioned prompt](/api-reference/get-versioned-prompt)