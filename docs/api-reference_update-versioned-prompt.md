Versioned Prompts

Update versioned prompt



  



        



        



    



        



        



              



        



  



      



              


Update versioned prompt

cURL

Copy

```
`curl --request PUT \ --url https://api.vogent.ai/api/agents/{agentId}/versioned_prompts/{id} \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "aiModelId": "<string>", "agentType": "STANDARD", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {} } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "name": "<string>", "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "agentType": "STANDARD", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {}, "outputSchema": "<string>" } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "aiModelId": "<string>", "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] }`
```

Versioned Prompts

# Update versioned prompt

Updates a versioned prompt for a given agent.

PUT

/

agents

/

{agentId}

/

versioned_prompts

/

{id}

Try it

Update versioned prompt

cURL

Copy

```
`curl --request PUT \ --url https://api.vogent.ai/api/agents/{agentId}/versioned_prompts/{id} \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "aiModelId": "<string>", "agentType": "STANDARD", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {} } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "name": "<string>", "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "agentType": "STANDARD", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {}, "outputSchema": "<string>" } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "aiModelId": "<string>", "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] }`
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

[​](#parameter-id)

id

string

required

ID of the versioned prompt.

#### Body

application/json

Updates a versioned prompt

[​](#body-ai-model-id)

aiModelId

string

The ID of the model to use.

[​](#body-agent-type)

agentType

enum<string>

The type of agent that this prompt represents.

Available options: 

`STANDARD`, 

`CUSTOM_FLOW`

[​](#body-prompt)

prompt

string

[​](#body-flow-definition)

flowDefinition

object

For agents with agentType CUSTOM_FLOW, the flow definition that you want to use.

Show child attributes

[​](#body-flow-definition-nodes)

flowDefinition.nodes

object[]

Show child attributes

[​](#body-flow-definition-nodes-items-id)

flowDefinition.nodes.id

string

required

[​](#body-flow-definition-nodes-items-name)

flowDefinition.nodes.name

string

required

One of the allowed flow node types. View the available types at <https://docs.vogent.ai/flow>.

[​](#body-flow-definition-nodes-items-type)

flowDefinition.nodes.type

string

required

[​](#body-flow-definition-nodes-items-transition-rules)

flowDefinition.nodes.transitionRules

object[]

required

Show child attributes

[​](#body-flow-definition-nodes-items-transition-rules-items-condition-type)

flowDefinition.nodes.transitionRules.conditionType

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

[​](#body-flow-definition-nodes-items-transition-rules-items-transition-node-id)

flowDefinition.nodes.transitionRules.transitionNodeId

string

required

[​](#body-flow-definition-nodes-items-transition-rules-items-array-condition-type-one-of-0)

flowDefinition.nodes.transitionRules.arrayConditionType

enum<string> | null

The type of array condition to apply. 'any' means at least one element must match, 'all' means all elements must match.

Available options: 

`any`, 

`all`

[​](#body-flow-definition-nodes-items-transition-rules-items-field-one-of-0)

flowDefinition.nodes.transitionRules.field

string | null

[​](#body-flow-definition-nodes-items-transition-rules-items-value-one-of-0)

flowDefinition.nodes.transitionRules.value

string | null

[​](#body-flow-definition-nodes-items-transition-rules-items-values-one-of-0)

flowDefinition.nodes.transitionRules.values

string[] | null

[​](#body-flow-definition-nodes-items-node-data)

flowDefinition.nodes.nodeData

object

required

The node-specific configuration. View the configurations by node type at <https://docs.vogent.ai/flow>.

[​](#body-flow-definition-global-context-one-of-0)

flowDefinition.globalContext

string | null

[​](#body-flow-definition-ai-open)

flowDefinition.aiOpen

boolean

Deprecated, use openingLineType instead.

[​](#body-flow-definition-opening-line-type)

flowDefinition.openingLineType

enum<string>

Available options: 

`INBOUND_ONLY`, 

`INBOUND_OUTBOUND`, 

`NONE`

[​](#body-name)

name

string

[​](#body-model-option-values)

modelOptionValues

object[]

Show child attributes

[​](#body-model-option-values-items-option-id)

modelOptionValues.optionId

string

required

The ID of option.

[​](#body-model-option-values-items-value)

modelOptionValues.value

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

Unique identifier for the versioned prompt

[​](#response-name)

name

string

required

Human-readable name for the versioned prompt

[​](#response-agent-type)

agentType

enum<string>

required

The type of agent this prompt is designed for (STANDARD or CUSTOM_FLOW)

Available options: 

`STANDARD`, 

`CUSTOM_FLOW`

[​](#response-prompt-one-of-0)

prompt

string | null

required

The actual prompt content that will be used by the agent. Can be null for CUSTOM_FLOW agent types

[​](#response-flow-definition-one-of-0)

flowDefinition

object

The flow definition for the agent. Only defined for CUSTOM_FLOW agent types.

Show child attributes

[​](#response-flow-definition-one-of-0-nodes)

flowDefinition.nodes

object[]

required

Show child attributes

[​](#response-flow-definition-one-of-0-nodes-items-id)

flowDefinition.nodes.id

string

required

[​](#response-flow-definition-one-of-0-nodes-items-name)

flowDefinition.nodes.name

string

required

[​](#response-flow-definition-one-of-0-nodes-items-type)

flowDefinition.nodes.type

string

required

The node type. View the available types at <https://docs.vogent.ai/flow>.

[​](#response-flow-definition-one-of-0-nodes-items-transition-rules)

flowDefinition.nodes.transitionRules

object[]

required

Show child attributes

[​](#response-flow-definition-one-of-0-nodes-items-transition-rules-items-condition-type)

flowDefinition.nodes.transitionRules.conditionType

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

[​](#response-flow-definition-one-of-0-nodes-items-transition-rules-items-transition-node-id)

flowDefinition.nodes.transitionRules.transitionNodeId

string

required

[​](#response-flow-definition-one-of-0-nodes-items-transition-rules-items-array-condition-type-one-of-0)

flowDefinition.nodes.transitionRules.arrayConditionType

enum<string> | null

The type of array condition to apply. 'any' means at least one element must match, 'all' means all elements must match.

Available options: 

`any`, 

`all`

[​](#response-flow-definition-one-of-0-nodes-items-transition-rules-items-field-one-of-0)

flowDefinition.nodes.transitionRules.field

string | null

[​](#response-flow-definition-one-of-0-nodes-items-transition-rules-items-value-one-of-0)

flowDefinition.nodes.transitionRules.value

string | null

[​](#response-flow-definition-one-of-0-nodes-items-transition-rules-items-values-one-of-0)

flowDefinition.nodes.transitionRules.values

string[] | null

[​](#response-flow-definition-one-of-0-nodes-items-node-data)

flowDefinition.nodes.nodeData

object

required

The node-specific configuration. View the schemas by type at <https://docs.vogent.ai/flow>.

[​](#response-flow-definition-one-of-0-nodes-items-output-schema-one-of-0)

flowDefinition.nodes.outputSchema

string | null

The JSON schema describing the output of this node. This is generated automatically from the node type and node data.

[​](#response-flow-definition-one-of-0-global-context-one-of-0)

flowDefinition.globalContext

string | null

required

[​](#response-flow-definition-one-of-0-ai-open)

flowDefinition.aiOpen

boolean

required

Deprecated, use openingLineType instead.

[​](#response-flow-definition-one-of-0-opening-line-type)

flowDefinition.openingLineType

enum<string>

required

Available options: 

`INBOUND_ONLY`, 

`INBOUND_OUTBOUND`, 

`NONE`

[​](#response-ai-model-id)

aiModelId

string

The AI model ID to use for the agent.

[​](#response-model-option-values)

modelOptionValues

object[]

Show child attributes

[​](#response-model-option-values-items-option-id)

modelOptionValues.optionId

string

required

The ID of option.

[​](#response-model-option-values-items-value)

modelOptionValues.value

string

required

[Get versioned prompt](/api-reference/get-versioned-prompt)[Create versioned prompt](/api-reference/create-versioned-prompt)