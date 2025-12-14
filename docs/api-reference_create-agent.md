Agents

Create Agent



  



        



        



    



        



        



              



        



  



      



              


Create Agent

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/agents \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "name": "<string>", "defaultVoiceId": "<string>", "defaultVersionedPrompt": { "aiModelId": "<string>", "agentType": "STANDARD", "name": "<string>", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {} } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] }, "defaultExtractor": { "name": "<string>", "extractorFieldsJsonSchema": "<string>" }, "inboundWebhookResponse": true, "inboundWebhookUrl": "<string>", "maxDurationSeconds": 10800, "openingLine": { "lineType": "INBOUND_ONLY", "content": "<string>" }, "voiceVolumeLevel": -100, "backgroundNoiseType": "office", "linkedFunctionDefinitionIds": [ "<string>" ], "linkedFunctionDefinitionInputs": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "metadata": {}, "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "aiVoiceId": "<string>", "taggingText": "<string>" }, "language": "en", "fillEmptyStringVariables": true } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "language": "<string>", "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "metadata": {}, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "aiVoiceId": "<string>", "taggingText": "<string>" }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "maxDurationSeconds": 10800, "defaultVoiceId": "<string>", "defaultVersionedPromptId": "<string>", "defaultExtractorId": "<string>", "linkedFunctionDefinitions": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "fillEmptyStringVariables": true }`
```

Agents

# Create Agent

Creates a new agent.

POST

/

agents

Try it

Create Agent

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/agents \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "name": "<string>", "defaultVoiceId": "<string>", "defaultVersionedPrompt": { "aiModelId": "<string>", "agentType": "STANDARD", "name": "<string>", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {} } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] }, "defaultExtractor": { "name": "<string>", "extractorFieldsJsonSchema": "<string>" }, "inboundWebhookResponse": true, "inboundWebhookUrl": "<string>", "maxDurationSeconds": 10800, "openingLine": { "lineType": "INBOUND_ONLY", "content": "<string>" }, "voiceVolumeLevel": -100, "backgroundNoiseType": "office", "linkedFunctionDefinitionIds": [ "<string>" ], "linkedFunctionDefinitionInputs": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "metadata": {}, "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "aiVoiceId": "<string>", "taggingText": "<string>" }, "language": "en", "fillEmptyStringVariables": true } '`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "language": "<string>", "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "metadata": {}, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "aiVoiceId": "<string>", "taggingText": "<string>" }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "maxDurationSeconds": 10800, "defaultVoiceId": "<string>", "defaultVersionedPromptId": "<string>", "defaultExtractorId": "<string>", "linkedFunctionDefinitions": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "fillEmptyStringVariables": true }`
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

Create a new agent

[​](#body-name)

name

string

required

The name of the agent.

[​](#body-default-voice-id)

defaultVoiceId

string

required

The ID of the voice to use.

[​](#body-default-versioned-prompt)

defaultVersionedPrompt

object

required

The default versioned prompt to use for this agent.

Show child attributes

[​](#body-default-versioned-prompt-ai-model-id)

defaultVersionedPrompt.aiModelId

string

required

The ID of the model to use.

[​](#body-default-versioned-prompt-agent-type)

defaultVersionedPrompt.agentType

enum<string>

required

The type of agent that this prompt represents.

Available options: 

`STANDARD`, 

`CUSTOM_FLOW`

[​](#body-default-versioned-prompt-name)

defaultVersionedPrompt.name

string

required

[​](#body-default-versioned-prompt-prompt-one-of-0)

defaultVersionedPrompt.prompt

string | null

[​](#body-default-versioned-prompt-flow-definition)

defaultVersionedPrompt.flowDefinition

object

For agents with agentType CUSTOM_FLOW, the flow definition that you want to use.

Show child attributes

[​](#body-default-versioned-prompt-flow-definition-nodes)

defaultVersionedPrompt.flowDefinition.nodes

object[]

Show child attributes

[​](#body-default-versioned-prompt-flow-definition-nodes-items-id)

defaultVersionedPrompt.flowDefinition.nodes.id

string

required

[​](#body-default-versioned-prompt-flow-definition-nodes-items-name)

defaultVersionedPrompt.flowDefinition.nodes.name

string

required

One of the allowed flow node types. View the available types at <https://docs.vogent.ai/flow>.

[​](#body-default-versioned-prompt-flow-definition-nodes-items-type)

defaultVersionedPrompt.flowDefinition.nodes.type

string

required

[​](#body-default-versioned-prompt-flow-definition-nodes-items-transition-rules)

defaultVersionedPrompt.flowDefinition.nodes.transitionRules

object[]

required

Show child attributes

[​](#body-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-condition-type)

defaultVersionedPrompt.flowDefinition.nodes.transitionRules.conditionType

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

[​](#body-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-transition-node-id)

defaultVersionedPrompt.flowDefinition.nodes.transitionRules.transitionNodeId

string

required

[​](#body-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-array-condition-type-one-of-0)

defaultVersionedPrompt.flowDefinition.nodes.transitionRules.arrayConditionType

enum<string> | null

The type of array condition to apply. 'any' means at least one element must match, 'all' means all elements must match.

Available options: 

`any`, 

`all`

[​](#body-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-field-one-of-0)

defaultVersionedPrompt.flowDefinition.nodes.transitionRules.field

string | null

[​](#body-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-value-one-of-0)

defaultVersionedPrompt.flowDefinition.nodes.transitionRules.value

string | null

[​](#body-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-values-one-of-0)

defaultVersionedPrompt.flowDefinition.nodes.transitionRules.values

string[] | null

[​](#body-default-versioned-prompt-flow-definition-nodes-items-node-data)

defaultVersionedPrompt.flowDefinition.nodes.nodeData

object

required

The node-specific configuration. View the configurations by node type at <https://docs.vogent.ai/flow>.

[​](#body-default-versioned-prompt-flow-definition-global-context-one-of-0)

defaultVersionedPrompt.flowDefinition.globalContext

string | null

[​](#body-default-versioned-prompt-flow-definition-ai-open)

defaultVersionedPrompt.flowDefinition.aiOpen

boolean

Deprecated, use openingLineType instead.

[​](#body-default-versioned-prompt-flow-definition-opening-line-type)

defaultVersionedPrompt.flowDefinition.openingLineType

enum<string>

Available options: 

`INBOUND_ONLY`, 

`INBOUND_OUTBOUND`, 

`NONE`

[​](#body-default-versioned-prompt-model-option-values)

defaultVersionedPrompt.modelOptionValues

object[]

Show child attributes

[​](#body-default-versioned-prompt-model-option-values-items-option-id)

defaultVersionedPrompt.modelOptionValues.optionId

string

required

The ID of option.

[​](#body-default-versioned-prompt-model-option-values-items-value)

defaultVersionedPrompt.modelOptionValues.value

string

required

[​](#body-default-extractor-one-of-0)

defaultExtractor

object

The default extractor to use for this agent.

Show child attributes

[​](#body-default-extractor-one-of-0-name)

defaultExtractor.name

string

required

[​](#body-default-extractor-one-of-0-extractor-fields-json-schema)

defaultExtractor.extractorFieldsJsonSchema

string

required

[​](#body-inbound-webhook-response)

inboundWebhookResponse

boolean

[​](#body-inbound-webhook-url)

inboundWebhookUrl

string

[​](#body-max-duration-seconds)

maxDurationSeconds

integer

default:10800

The maximum duration of the call in seconds.

[​](#body-opening-line-one-of-0)

openingLine

object

Details about the Agent's opening line. If unspecified, or null no opening line will be created.

Show child attributes

[​](#body-opening-line-one-of-0-line-type)

openingLine.lineType

enum<string>

required

An indication of when the opening line should be used.

Available options: 

`INBOUND_ONLY`, 

`INBOUND_OUTBOUND`, 

`NONE`

[​](#body-opening-line-one-of-0-content)

openingLine.content

string

required

The content of the opening line.

[​](#body-voice-volume-level-one-of-0)

voiceVolumeLevel

integer | null

default:-100

A value, generally between -300 and 300, indicating the volume level to use for the voice. The default is -100.

[​](#body-background-noise-type)

backgroundNoiseType

enum<string>

default:office

The background audio that's used by the agent.

Available options: 

`noise`, 

`office`, 

`silence`

[​](#body-linked-function-definition-ids)

linkedFunctionDefinitionIds

string[]

The function definitions that should be available to this agent (deprecated, use linkedFunctionDefinitionInputs instead)

[​](#body-linked-function-definition-inputs)

linkedFunctionDefinitionInputs

object[]

The function definitions that should be available to this agent with optional lifecycle message overrides

Show child attributes

[​](#body-linked-function-definition-inputs-items-function-definition-id)

linkedFunctionDefinitionInputs.functionDefinitionId

string

required

The ID of the function definition to link.

[​](#body-linked-function-definition-inputs-items-lifecycle-messages-override)

linkedFunctionDefinitionInputs.lifecycleMessagesOverride

object

Lifecycle messages to override the defaults for this function link, or null to not override.

Show child attributes

[​](#body-linked-function-definition-inputs-items-lifecycle-messages-override-started)

linkedFunctionDefinitionInputs.lifecycleMessagesOverride.started

string[]

required

Messages to display when the function starts executing. One will be chosen at random.

[​](#body-metadata)

metadata

object

Show child attributes

[​](#body-metadata-additional-properties)

metadata.{key}

any

[​](#body-transcriber-params-one-of-0)

transcriberParams

object

Show child attributes

[​](#body-transcriber-params-one-of-0-type)

transcriberParams.type

enum<string>

required

Available options: 

`deepgram`, 

`openai`

[​](#body-transcriber-params-one-of-0-keywords)

transcriberParams.keywords

string[]

Keywords to be used for transcription.

[​](#body-idle-message-config)

idleMessageConfig

object

Show child attributes

[​](#body-idle-message-config-enabled)

idleMessageConfig.enabled

boolean

required

Whether idle messages are enabled for this agent.

[​](#body-idle-message-config-messages)

idleMessageConfig.messages

string[]

The list of idle messages that the agent can say when the user is silent.

[​](#body-idle-message-config-idle-duration-milliseconds)

idleMessageConfig.idleDurationMilliseconds

integer

The duration in milliseconds that the user must be silent before an idle message is triggered.

Required range: `x >= 5000`

[​](#body-idle-message-config-max-idle-messages)

idleMessageConfig.maxIdleMessages

integer

The maximum number of idle messages that can be said during a call.

Required range: `x >= 1`

[​](#body-utterance-detector-config)

utteranceDetectorConfig

object

Show child attributes

[​](#body-utterance-detector-config-sensitivity)

utteranceDetectorConfig.sensitivity

enum<string>

required

Available options: 

`ULTRA_FAST`, 

`FAST`, 

`MEDIUM`, 

`SLOW`

[​](#body-endpoint-detector-config-one-of-0)

endpointDetectorConfig

object

Configuration for endpoint detection to determine when a user has finished speaking. If not specified, will default to a semantic detector in the default mode.

Show child attributes

[​](#body-endpoint-detector-config-one-of-0-type)

endpointDetectorConfig.type

enum<string>

required

The type of endpoint detector to use.

Available options: 

`SIMPLE`, 

`SEMANTIC`

[​](#body-endpoint-detector-config-one-of-0-mode-one-of-0)

endpointDetectorConfig.mode

enum<string> | null

The mode for the endpoint detector (only applicable for SEMANTIC type).

Available options: 

`CONSERVATIVE`, 

`DEFAULT`, 

`AGGRESSIVE`

[​](#body-ivr-configuration-one-of-0)

ivrConfiguration

object

The configuration for IVR detection and navigation including detection type, prompt, voice, and tagging settings.

Show child attributes

[​](#body-ivr-configuration-one-of-0-detection-type)

ivrConfiguration.detectionType

enum<string>

required

The type of IVR detection to use.

Available options: 

`NONE`, 

`STANDARD`

[​](#body-ivr-configuration-one-of-0-versioned-prompt-id-one-of-0)

ivrConfiguration.versionedPromptId

string | null

The versioned prompt ID to use for IVR detection.

[​](#body-ivr-configuration-one-of-0-ai-voice-id-one-of-0)

ivrConfiguration.aiVoiceId

string | null

The AI voice ID to use for IVR detection.

[​](#body-ivr-configuration-one-of-0-tagging-text-one-of-0)

ivrConfiguration.taggingText

string | null

The tagging text for IVR detection.

[​](#body-language)

language

string

default:en

The language to use for the agent.

[​](#body-fill-empty-string-variables-one-of-0)

fillEmptyStringVariables

boolean | null

If true, variables that are not specified will be filled with empty strings instead of being left as template placeholders.

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

[​](#response-language)

language

string

required

The language to use for the agent.

[​](#response-transcriber-params-one-of-0)

transcriberParams

object

Show child attributes

[​](#response-transcriber-params-one-of-0-type)

transcriberParams.type

enum<string>

required

Available options: 

`deepgram`, 

`openai`

[​](#response-transcriber-params-one-of-0-keywords)

transcriberParams.keywords

string[]

Keywords to be used for transcription.

[​](#response-metadata)

metadata

object

Show child attributes

[​](#response-metadata-additional-properties)

metadata.{key}

any

[​](#response-utterance-detector-config)

utteranceDetectorConfig

object

Show child attributes

[​](#response-utterance-detector-config-sensitivity)

utteranceDetectorConfig.sensitivity

enum<string>

required

Available options: 

`ULTRA_FAST`, 

`FAST`, 

`MEDIUM`, 

`SLOW`

[​](#response-endpoint-detector-config-one-of-0)

endpointDetectorConfig

object

Configuration for endpoint detection to determine when a user has finished speaking.

Show child attributes

[​](#response-endpoint-detector-config-one-of-0-type)

endpointDetectorConfig.type

enum<string>

required

The type of endpoint detector to use.

Available options: 

`SIMPLE`, 

`SEMANTIC`

[​](#response-endpoint-detector-config-one-of-0-mode-one-of-0)

endpointDetectorConfig.mode

enum<string> | null

The mode for the endpoint detector (only applicable for SEMANTIC type).

Available options: 

`CONSERVATIVE`, 

`DEFAULT`, 

`AGGRESSIVE`

[​](#response-ivr-configuration-one-of-0)

ivrConfiguration

object

The configuration for IVR detection and navigation including detection type, prompt, voice, and tagging settings.

Show child attributes

[​](#response-ivr-configuration-one-of-0-detection-type)

ivrConfiguration.detectionType

enum<string>

required

The type of IVR detection to use.

Available options: 

`NONE`, 

`STANDARD`

[​](#response-ivr-configuration-one-of-0-versioned-prompt-id-one-of-0)

ivrConfiguration.versionedPromptId

string | null

The versioned prompt ID to use for IVR detection.

[​](#response-ivr-configuration-one-of-0-ai-voice-id-one-of-0)

ivrConfiguration.aiVoiceId

string | null

The AI voice ID to use for IVR detection.

[​](#response-ivr-configuration-one-of-0-tagging-text-one-of-0)

ivrConfiguration.taggingText

string | null

The tagging text for IVR detection.

[​](#response-idle-message-config-one-of-0)

idleMessageConfig

object

Configuration for idle messages that the agent can say when the user is silent.

Show child attributes

[​](#response-idle-message-config-one-of-0-enabled)

idleMessageConfig.enabled

boolean

required

Whether idle messages are enabled for this agent.

[​](#response-idle-message-config-one-of-0-messages)

idleMessageConfig.messages

string[]

The list of idle messages that the agent can say when the user is silent.

[​](#response-idle-message-config-one-of-0-idle-duration-milliseconds)

idleMessageConfig.idleDurationMilliseconds

integer

The duration in milliseconds that the user must be silent before an idle message is triggered.

Required range: `x >= 5000`

[​](#response-idle-message-config-one-of-0-max-idle-messages)

idleMessageConfig.maxIdleMessages

integer

The maximum number of idle messages that can be said during a call.

Required range: `x >= 1`

[​](#response-max-duration-seconds)

maxDurationSeconds

integer

default:10800

The maximum duration of the call in seconds.

[​](#response-default-voice-id)

defaultVoiceId

string

The default voice ID to use for the agent.

[​](#response-default-versioned-prompt-id)

defaultVersionedPromptId

string

The default versioned prompt ID to use for the agent.

[​](#response-default-extractor-id-one-of-0)

defaultExtractorId

string | null

The default extractor ID to use for the agent.

[​](#response-linked-function-definitions)

linkedFunctionDefinitions

object[]

The function definitions that should be available to this agent.

Show child attributes

[​](#response-linked-function-definitions-items-function-definition-id)

linkedFunctionDefinitions.functionDefinitionId

string

required

The ID of the function definition to link.

[​](#response-linked-function-definitions-items-lifecycle-messages-override)

linkedFunctionDefinitions.lifecycleMessagesOverride

object

Lifecycle messages to override the defaults for this function link, or null to not override.

Show child attributes

[​](#response-linked-function-definitions-items-lifecycle-messages-override-started)

linkedFunctionDefinitions.lifecycleMessagesOverride.started

string[]

required

Messages to display when the function starts executing. One will be chosen at random.

[​](#response-fill-empty-string-variables)

fillEmptyStringVariables

boolean

If true, variables that are not specified will be filled with empty strings instead of being left as template placeholders.

[List Agents](/api-reference/list-agents)[Update Agent](/api-reference/update-agent)