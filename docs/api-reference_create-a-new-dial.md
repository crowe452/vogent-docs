Dials

Create a new dial



  



        



        



    



        



        



              



        



  



      



              


Create a new dial

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/dials \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "callAgentId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "webhookUrl": "https://test.com/webhook", "browserCall": false, "toNumber": "+11234567890", "fromNumberId": "1caec78c-4bba-477d-82cf-bcfce2b73856", "fromNumberPoolId": "1caec78c-4bba-477d-82cf-bcfce2b73856", "aiVoiceId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "voiceOptionValues": [ { "optionId": "<string>", "value": "<string>" } ], "voiceVolumeLevel": -100, "versionedModelId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "ivrVersionedPromptId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "overrideTranscriberFinalDurationMs": 500, "timeoutMinutes": 10, "callAgentExtractorId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "callAgentInput": {}, "agentOverrides": { "defaultVoiceId": "<string>", "defaultVersionedPrompt": { "aiModelId": "<string>", "agentType": "STANDARD", "name": "<string>", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {} } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] }, "inboundWebhookResponse": true, "inboundWebhookUrl": "<string>", "maxDurationSeconds": 123, "openingLine": { "lineType": "INBOUND_ONLY", "content": "<string>" }, "voiceVolumeLevel": 123, "backgroundNoiseType": "noise", "linkedFunctionDefinitionIds": [ "<string>" ], "linkedFunctionDefinitionInputs": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "metadata": {}, "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "versionedPrompt": { "aiModelId": "<string>", "agentType": "STANDARD", "name": "<string>", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {} } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] }, "aiVoiceId": "<string>", "taggingText": "<string>" }, "language": "<string>", "fillEmptyStringVariables": true }, "keywords": [ "<string>" ] } '`
```

200

400

422

Copy

```
`{ "dialToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZXN0IjoidGVzdCJ9.9EQaLsDRKDVXLUVLR9JgDTjEULaT2-OMbHayQAzgZH8", "sessionId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "dialId": "57555c5e-5a56-49ca-8fe8-24946d2fbc3e" }`
```

Dials

# Create a new dial

Creates a one-off dial session, either for phone dials or browser dials.

POST

/

dials

Try it

Create a new dial

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/dials \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "callAgentId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "webhookUrl": "https://test.com/webhook", "browserCall": false, "toNumber": "+11234567890", "fromNumberId": "1caec78c-4bba-477d-82cf-bcfce2b73856", "fromNumberPoolId": "1caec78c-4bba-477d-82cf-bcfce2b73856", "aiVoiceId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "voiceOptionValues": [ { "optionId": "<string>", "value": "<string>" } ], "voiceVolumeLevel": -100, "versionedModelId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "ivrVersionedPromptId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "overrideTranscriberFinalDurationMs": 500, "timeoutMinutes": 10, "callAgentExtractorId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "callAgentInput": {}, "agentOverrides": { "defaultVoiceId": "<string>", "defaultVersionedPrompt": { "aiModelId": "<string>", "agentType": "STANDARD", "name": "<string>", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {} } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] }, "inboundWebhookResponse": true, "inboundWebhookUrl": "<string>", "maxDurationSeconds": 123, "openingLine": { "lineType": "INBOUND_ONLY", "content": "<string>" }, "voiceVolumeLevel": 123, "backgroundNoiseType": "noise", "linkedFunctionDefinitionIds": [ "<string>" ], "linkedFunctionDefinitionInputs": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "metadata": {}, "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "versionedPrompt": { "aiModelId": "<string>", "agentType": "STANDARD", "name": "<string>", "prompt": "<string>", "flowDefinition": { "nodes": [ { "id": "<string>", "name": "<string>", "type": "<string>", "transitionRules": [ { "conditionType": "always", "transitionNodeId": "<string>", "arrayConditionType": "any", "field": "<string>", "value": "<string>", "values": [ "<string>" ] } ], "nodeData": {} } ], "globalContext": "<string>", "aiOpen": true, "openingLineType": "INBOUND_ONLY" }, "modelOptionValues": [ { "optionId": "<string>", "value": "<string>" } ] }, "aiVoiceId": "<string>", "taggingText": "<string>" }, "language": "<string>", "fillEmptyStringVariables": true }, "keywords": [ "<string>" ] } '`
```

200

400

422

Copy

```
`{ "dialToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZXN0IjoidGVzdCJ9.9EQaLsDRKDVXLUVLR9JgDTjEULaT2-OMbHayQAzgZH8", "sessionId": "61ccefdf-ea02-4f49-811b-1241f8e20d26", "dialId": "57555c5e-5a56-49ca-8fe8-24946d2fbc3e" }`
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

Create a new dial

[​](#body-call-agent-id)

callAgentId

string

required

Required. The ID of the agent.

Example:

`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`

[​](#body-webhook-url-one-of-0)

webhookUrl

string | null

Optional. The URL for the webhook for this dial session.

Example:

`"https://test.com/webhook"`

[​](#body-browser-call-one-of-0)

browserCall

boolean | null

Set to true if this is a browser call.

Example:

`false`

[​](#body-to-number-one-of-0)

toNumber

string | null

Required if this is a phone dial, in E.164 format.

Example:

`"+11234567890"`

[​](#body-from-number-id-one-of-0)

fromNumberId

string | null

The ID for the phone number to use to start the call. Required if this is a phone dial.

Example:

`"1caec78c-4bba-477d-82cf-bcfce2b73856"`

[​](#body-from-number-pool-id-one-of-0)

fromNumberPoolId

string | null

The ID of a phone number pool to use when starting the call.

Example:

`"1caec78c-4bba-477d-82cf-bcfce2b73856"`

[​](#body-ai-voice-id-one-of-0)

aiVoiceId

string | null

The ID for the voice on the call. If not specified, the default voice for the agent will be used.

Example:

`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`

[​](#body-voice-option-values)

voiceOptionValues

object[]

An optional configuration for the voice being used.

Show child attributes

[​](#body-voice-option-values-items-option-id)

voiceOptionValues.optionId

string

required

The ID of option.

[​](#body-voice-option-values-items-value)

voiceOptionValues.value

string

required

[​](#body-voice-volume-level)

voiceVolumeLevel

integer

The volume level for the voice on the call, from -300 (quiet) to 300 (loud).

Example:

`-100`

[​](#body-versioned-model-id)

versionedModelId

string

The prompt/model version to use for this call, if not specified, the default on the agent is used.

Example:

`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`

[​](#body-ivr-versioned-prompt-id)

ivrVersionedPromptId

string

The prompt/model version to use for the IVR portion of this call, if ivr nav is enabled on the agent.

Example:

`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`

[​](#body-override-transcriber-final-duration-ms)

overrideTranscriberFinalDurationMs

integer

How long in ms after an utterance is complete to ignore the final/non-final status of the transcript and run inference.

Example:

`500`

[​](#body-timeout-minutes)

timeoutMinutes

integer

The number of minutes before the call will be timed out. If not specified, there will be no limit on the calls, it's recommended to provide something here.

Example:

`10`

[​](#body-call-agent-extractor-id)

callAgentExtractorId

string

The ID of the extractor to use for this call, if not specified, the default on the agent is used.

Example:

`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`

[​](#body-call-agent-input-one-of-0)

callAgentInput

object

Any macros in the call agent prompt.

Show child attributes

[​](#body-call-agent-input-one-of-0-additional-properties)

callAgentInput.{key}

any

[​](#body-agent-overrides-one-of-0)

agentOverrides

object

(Alpha) This feature is in Alpha testing, schemas may change slightly before GA. Please notify the Vogent team if there are any issues when using this field. Optional overrides for the call agent used for this dial.

Show child attributes

[​](#body-agent-overrides-one-of-0-default-voice-id)

agentOverrides.defaultVoiceId

string

The ID of the voice to use.

[​](#body-agent-overrides-one-of-0-default-versioned-prompt)

agentOverrides.defaultVersionedPrompt

object

The default versioned prompt to use.

Show child attributes

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-ai-model-id)

agentOverrides.defaultVersionedPrompt.aiModelId

string

required

The ID of the model to use.

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-agent-type)

agentOverrides.defaultVersionedPrompt.agentType

enum<string>

required

The type of agent that this prompt represents.

Available options: 

`STANDARD`, 

`CUSTOM_FLOW`

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-name)

agentOverrides.defaultVersionedPrompt.name

string

required

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-prompt-one-of-0)

agentOverrides.defaultVersionedPrompt.prompt

string | null

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition)

agentOverrides.defaultVersionedPrompt.flowDefinition

object

For agents with agentType CUSTOM_FLOW, the flow definition that you want to use.

Show child attributes

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes

object[]

Show child attributes

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes-items-id)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes.id

string

required

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes-items-name)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes.name

string

required

One of the allowed flow node types. View the available types at <https://docs.vogent.ai/flow>.

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes-items-type)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes.type

string

required

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes-items-transition-rules)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes.transitionRules

object[]

required

Show child attributes

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-condition-type)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes.transitionRules.conditionType

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

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-transition-node-id)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes.transitionRules.transitionNodeId

string

required

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-array-condition-type-one-of-0)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes.transitionRules.arrayConditionType

enum<string> | null

The type of array condition to apply. 'any' means at least one element must match, 'all' means all elements must match.

Available options: 

`any`, 

`all`

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-field-one-of-0)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes.transitionRules.field

string | null

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-value-one-of-0)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes.transitionRules.value

string | null

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes-items-transition-rules-items-values-one-of-0)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes.transitionRules.values

string[] | null

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-nodes-items-node-data)

agentOverrides.defaultVersionedPrompt.flowDefinition.nodes.nodeData

object

required

The node-specific configuration. View the configurations by node type at <https://docs.vogent.ai/flow>.

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-global-context-one-of-0)

agentOverrides.defaultVersionedPrompt.flowDefinition.globalContext

string | null

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-ai-open)

agentOverrides.defaultVersionedPrompt.flowDefinition.aiOpen

boolean

Deprecated, use openingLineType instead.

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-flow-definition-opening-line-type)

agentOverrides.defaultVersionedPrompt.flowDefinition.openingLineType

enum<string>

Available options: 

`INBOUND_ONLY`, 

`INBOUND_OUTBOUND`, 

`NONE`

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-model-option-values)

agentOverrides.defaultVersionedPrompt.modelOptionValues

object[]

Show child attributes

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-model-option-values-items-option-id)

agentOverrides.defaultVersionedPrompt.modelOptionValues.optionId

string

required

The ID of option.

[​](#body-agent-overrides-one-of-0-default-versioned-prompt-model-option-values-items-value)

agentOverrides.defaultVersionedPrompt.modelOptionValues.value

string

required

[​](#body-agent-overrides-one-of-0-inbound-webhook-response)

agentOverrides.inboundWebhookResponse

boolean

[​](#body-agent-overrides-one-of-0-inbound-webhook-url)

agentOverrides.inboundWebhookUrl

string

[​](#body-agent-overrides-one-of-0-max-duration-seconds)

agentOverrides.maxDurationSeconds

integer

The maximum duration of the call in seconds.

[​](#body-agent-overrides-one-of-0-opening-line)

agentOverrides.openingLine

object

Details about the Agent's opening line. If unspecified, or null no opening line will be created.

Show child attributes

[​](#body-agent-overrides-one-of-0-opening-line-line-type)

agentOverrides.openingLine.lineType

enum<string>

required

An indication of when the opening line should be used.

Available options: 

`INBOUND_ONLY`, 

`INBOUND_OUTBOUND`, 

`NONE`

[​](#body-agent-overrides-one-of-0-opening-line-content)

agentOverrides.openingLine.content

string

required

The content of the opening line.

[​](#body-agent-overrides-one-of-0-voice-volume-level)

agentOverrides.voiceVolumeLevel

integer

A value, generally between -300 and 300, indicating the volume level to use for the voice. The default is -100.

[​](#body-agent-overrides-one-of-0-background-noise-type)

agentOverrides.backgroundNoiseType

enum<string>

The background audio that's used by the agent.

Available options: 

`noise`, 

`office`, 

`silence`

[​](#body-agent-overrides-one-of-0-linked-function-definition-ids)

agentOverrides.linkedFunctionDefinitionIds

string[]

The function definitions that should be available to this agent (deprecated, use linkedFunctionDefinitionInputs instead)

[​](#body-agent-overrides-one-of-0-linked-function-definition-inputs)

agentOverrides.linkedFunctionDefinitionInputs

object[]

The function definitions that should be available to this agent with optional lifecycle message overrides

Show child attributes

[​](#body-agent-overrides-one-of-0-linked-function-definition-inputs-items-function-definition-id)

agentOverrides.linkedFunctionDefinitionInputs.functionDefinitionId

string

required

The ID of the function definition to link.

[​](#body-agent-overrides-one-of-0-linked-function-definition-inputs-items-lifecycle-messages-override)

agentOverrides.linkedFunctionDefinitionInputs.lifecycleMessagesOverride

object

Lifecycle messages to override the defaults for this function link, or null to not override.

Show child attributes

[​](#body-agent-overrides-one-of-0-linked-function-definition-inputs-items-lifecycle-messages-override-started)

agentOverrides.linkedFunctionDefinitionInputs.lifecycleMessagesOverride.started

string[]

required

Messages to display when the function starts executing. One will be chosen at random.

[​](#body-agent-overrides-one-of-0-metadata)

agentOverrides.metadata

object

Show child attributes

[​](#body-agent-overrides-one-of-0-metadata-additional-properties)

agentOverrides.metadata.{key}

any

[​](#body-agent-overrides-one-of-0-transcriber-params)

agentOverrides.transcriberParams

object

Show child attributes

[​](#body-agent-overrides-one-of-0-transcriber-params-type)

agentOverrides.transcriberParams.type

enum<string>

required

Available options: 

`deepgram`, 

`openai`

[​](#body-agent-overrides-one-of-0-transcriber-params-keywords)

agentOverrides.transcriberParams.keywords

string[]

Keywords to be used for transcription.

[​](#body-agent-overrides-one-of-0-idle-message-config)

agentOverrides.idleMessageConfig

object

Show child attributes

[​](#body-agent-overrides-one-of-0-idle-message-config-enabled)

agentOverrides.idleMessageConfig.enabled

boolean

required

Whether idle messages are enabled for this agent.

[​](#body-agent-overrides-one-of-0-idle-message-config-messages)

agentOverrides.idleMessageConfig.messages

string[]

The list of idle messages that the agent can say when the user is silent.

[​](#body-agent-overrides-one-of-0-idle-message-config-idle-duration-milliseconds)

agentOverrides.idleMessageConfig.idleDurationMilliseconds

integer

The duration in milliseconds that the user must be silent before an idle message is triggered.

Required range: `x >= 5000`

[​](#body-agent-overrides-one-of-0-idle-message-config-max-idle-messages)

agentOverrides.idleMessageConfig.maxIdleMessages

integer

The maximum number of idle messages that can be said during a call.

Required range: `x >= 1`

[​](#body-agent-overrides-one-of-0-utterance-detector-config)

agentOverrides.utteranceDetectorConfig

object

Show child attributes

[​](#body-agent-overrides-one-of-0-utterance-detector-config-sensitivity)

agentOverrides.utteranceDetectorConfig.sensitivity

enum<string>

required

Available options: 

`ULTRA_FAST`, 

`FAST`, 

`MEDIUM`, 

`SLOW`

[​](#body-agent-overrides-one-of-0-endpoint-detector-config)

agentOverrides.endpointDetectorConfig

object

Configuration for endpoint detection to determine when a user has finished speaking. If not specified, will default to a semantic detector in the default mode.

Show child attributes

[​](#body-agent-overrides-one-of-0-endpoint-detector-config-type)

agentOverrides.endpointDetectorConfig.type

enum<string>

required

The type of endpoint detector to use.

Available options: 

`SIMPLE`, 

`SEMANTIC`

[​](#body-agent-overrides-one-of-0-endpoint-detector-config-mode-one-of-0)

agentOverrides.endpointDetectorConfig.mode

enum<string> | null

The mode for the endpoint detector (only applicable for SEMANTIC type).

Available options: 

`CONSERVATIVE`, 

`DEFAULT`, 

`AGGRESSIVE`

[​](#body-agent-overrides-one-of-0-ivr-configuration)

agentOverrides.ivrConfiguration

object

The configuration for IVR detection and navigation including detection type, prompt, voice, and tagging settings.

Show child attributes

[​](#body-agent-overrides-one-of-0-ivr-configuration-detection-type)

agentOverrides.ivrConfiguration.detectionType

enum<string>

required

The type of IVR detection to use.

Available options: 

`NONE`, 

`STANDARD`

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-id-one-of-0)

agentOverrides.ivrConfiguration.versionedPromptId

string | null

The versioned prompt ID to use for IVR detection.

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt)

agentOverrides.ivrConfiguration.versionedPrompt

object

The default versioned prompt to use for IVR navigation.

Show child attributes

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-ai-model-id)

agentOverrides.ivrConfiguration.versionedPrompt.aiModelId

string

required

The ID of the model to use.

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-agent-type)

agentOverrides.ivrConfiguration.versionedPrompt.agentType

enum<string>

required

The type of agent that this prompt represents.

Available options: 

`STANDARD`, 

`CUSTOM_FLOW`

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-name)

agentOverrides.ivrConfiguration.versionedPrompt.name

string

required

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-prompt-one-of-0)

agentOverrides.ivrConfiguration.versionedPrompt.prompt

string | null

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition

object

For agents with agentType CUSTOM_FLOW, the flow definition that you want to use.

Show child attributes

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes

object[]

Show child attributes

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes-items-id)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes.id

string

required

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes-items-name)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes.name

string

required

One of the allowed flow node types. View the available types at <https://docs.vogent.ai/flow>.

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes-items-type)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes.type

string

required

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes-items-transition-rules)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes.transitionRules

object[]

required

Show child attributes

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes-items-transition-rules-items-condition-type)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes.transitionRules.conditionType

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

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes-items-transition-rules-items-transition-node-id)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes.transitionRules.transitionNodeId

string

required

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes-items-transition-rules-items-array-condition-type-one-of-0)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes.transitionRules.arrayConditionType

enum<string> | null

The type of array condition to apply. 'any' means at least one element must match, 'all' means all elements must match.

Available options: 

`any`, 

`all`

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes-items-transition-rules-items-field-one-of-0)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes.transitionRules.field

string | null

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes-items-transition-rules-items-value-one-of-0)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes.transitionRules.value

string | null

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes-items-transition-rules-items-values-one-of-0)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes.transitionRules.values

string[] | null

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-nodes-items-node-data)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.nodes.nodeData

object

required

The node-specific configuration. View the configurations by node type at <https://docs.vogent.ai/flow>.

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-global-context-one-of-0)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.globalContext

string | null

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-ai-open)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.aiOpen

boolean

Deprecated, use openingLineType instead.

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-flow-definition-opening-line-type)

agentOverrides.ivrConfiguration.versionedPrompt.flowDefinition.openingLineType

enum<string>

Available options: 

`INBOUND_ONLY`, 

`INBOUND_OUTBOUND`, 

`NONE`

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-model-option-values)

agentOverrides.ivrConfiguration.versionedPrompt.modelOptionValues

object[]

Show child attributes

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-model-option-values-items-option-id)

agentOverrides.ivrConfiguration.versionedPrompt.modelOptionValues.optionId

string

required

The ID of option.

[​](#body-agent-overrides-one-of-0-ivr-configuration-versioned-prompt-model-option-values-items-value)

agentOverrides.ivrConfiguration.versionedPrompt.modelOptionValues.value

string

required

[​](#body-agent-overrides-one-of-0-ivr-configuration-ai-voice-id-one-of-0)

agentOverrides.ivrConfiguration.aiVoiceId

string | null

The AI voice ID to use for IVR detection.

[​](#body-agent-overrides-one-of-0-ivr-configuration-tagging-text-one-of-0)

agentOverrides.ivrConfiguration.taggingText

string | null

The tagging text for IVR detection.

[​](#body-agent-overrides-one-of-0-language)

agentOverrides.language

string

The language to use for the agent.

[​](#body-agent-overrides-one-of-0-fill-empty-string-variables)

agentOverrides.fillEmptyStringVariables

boolean

If true, variables that are not specified will be filled with empty strings instead of being left as template placeholders.

[​](#body-keywords-one-of-0)

keywords

string[] | null

A list of keywords to be used in the call.

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

[​](#response-session-id)

sessionId

string

required

Example:

`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`

[​](#response-dial-id)

dialId

string

required

Example:

`"57555c5e-5a56-49ca-8fe8-24946d2fbc3e"`

[Introduction](/api-reference/introduction)[Hangup Dial.](/api-reference/hangup-dial)