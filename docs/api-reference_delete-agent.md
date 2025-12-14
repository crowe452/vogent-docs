Agents

Delete Agent



  



        



        



    



        



        



              



        



  



      



              


Delete Agent

cURL

Copy

```
`curl --request DELETE \ --url https://api.vogent.ai/api/agents/{id} \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "language": "<string>", "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "metadata": {}, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "aiVoiceId": "<string>", "taggingText": "<string>" }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "maxDurationSeconds": 10800, "defaultVoiceId": "<string>", "defaultVersionedPromptId": "<string>", "defaultExtractorId": "<string>", "linkedFunctionDefinitions": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "fillEmptyStringVariables": true }`
```

Agents

# Delete Agent

Delete an agent. This action is irreversible, so be careful when using it. Returns the deleted agent.

DELETE

/

agents

/

{id}

Try it

Delete Agent

cURL

Copy

```
`curl --request DELETE \ --url https://api.vogent.ai/api/agents/{id} \ --header 'Authorization: Bearer <token>'`
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

#### Path Parameters

[​](#parameter-id)

id

string

required

ID of the agent.

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

[Update Agent](/api-reference/update-agent)[Clone Voice](/api-reference/clone-voice)