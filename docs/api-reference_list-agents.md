Agents

List Agents



  



        



        



    



        



        



              



        



  



      



              


List Agents

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/agents \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "name": "<string>", "language": "<string>", "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "metadata": {}, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "aiVoiceId": "<string>", "taggingText": "<string>" }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "maxDurationSeconds": 10800, "defaultVoiceId": "<string>", "defaultVersionedPromptId": "<string>", "defaultExtractorId": "<string>", "linkedFunctionDefinitions": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "fillEmptyStringVariables": true } ], "cursor": "<string>" }`
```

Agents

# List Agents

List the agents on your account.

GET

/

agents

Try it

List Agents

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/agents \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "name": "<string>", "language": "<string>", "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "metadata": {}, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "aiVoiceId": "<string>", "taggingText": "<string>" }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "maxDurationSeconds": 10800, "defaultVoiceId": "<string>", "defaultVersionedPromptId": "<string>", "defaultExtractorId": "<string>", "linkedFunctionDefinitions": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "fillEmptyStringVariables": true } ], "cursor": "<string>" }`
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

[​](#response-data-items-language)

data.language

string

required

The language to use for the agent.

[​](#response-data-items-transcriber-params-one-of-0)

data.transcriberParams

object

Show child attributes

[​](#response-data-items-transcriber-params-one-of-0-type)

data.transcriberParams.type

enum<string>

required

Available options: 

`deepgram`, 

`openai`

[​](#response-data-items-transcriber-params-one-of-0-keywords)

data.transcriberParams.keywords

string[]

Keywords to be used for transcription.

[​](#response-data-items-metadata)

data.metadata

object

Show child attributes

[​](#response-data-items-metadata-additional-properties)

data.metadata.{key}

any

[​](#response-data-items-utterance-detector-config)

data.utteranceDetectorConfig

object

Show child attributes

[​](#response-data-items-utterance-detector-config-sensitivity)

data.utteranceDetectorConfig.sensitivity

enum<string>

required

Available options: 

`ULTRA_FAST`, 

`FAST`, 

`MEDIUM`, 

`SLOW`

[​](#response-data-items-endpoint-detector-config-one-of-0)

data.endpointDetectorConfig

object

Configuration for endpoint detection to determine when a user has finished speaking.

Show child attributes

[​](#response-data-items-endpoint-detector-config-one-of-0-type)

data.endpointDetectorConfig.type

enum<string>

required

The type of endpoint detector to use.

Available options: 

`SIMPLE`, 

`SEMANTIC`

[​](#response-data-items-endpoint-detector-config-one-of-0-mode-one-of-0)

data.endpointDetectorConfig.mode

enum<string> | null

The mode for the endpoint detector (only applicable for SEMANTIC type).

Available options: 

`CONSERVATIVE`, 

`DEFAULT`, 

`AGGRESSIVE`

[​](#response-data-items-ivr-configuration-one-of-0)

data.ivrConfiguration

object

The configuration for IVR detection and navigation including detection type, prompt, voice, and tagging settings.

Show child attributes

[​](#response-data-items-ivr-configuration-one-of-0-detection-type)

data.ivrConfiguration.detectionType

enum<string>

required

The type of IVR detection to use.

Available options: 

`NONE`, 

`STANDARD`

[​](#response-data-items-ivr-configuration-one-of-0-versioned-prompt-id-one-of-0)

data.ivrConfiguration.versionedPromptId

string | null

The versioned prompt ID to use for IVR detection.

[​](#response-data-items-ivr-configuration-one-of-0-ai-voice-id-one-of-0)

data.ivrConfiguration.aiVoiceId

string | null

The AI voice ID to use for IVR detection.

[​](#response-data-items-ivr-configuration-one-of-0-tagging-text-one-of-0)

data.ivrConfiguration.taggingText

string | null

The tagging text for IVR detection.

[​](#response-data-items-idle-message-config-one-of-0)

data.idleMessageConfig

object

Configuration for idle messages that the agent can say when the user is silent.

Show child attributes

[​](#response-data-items-idle-message-config-one-of-0-enabled)

data.idleMessageConfig.enabled

boolean

required

Whether idle messages are enabled for this agent.

[​](#response-data-items-idle-message-config-one-of-0-messages)

data.idleMessageConfig.messages

string[]

The list of idle messages that the agent can say when the user is silent.

[​](#response-data-items-idle-message-config-one-of-0-idle-duration-milliseconds)

data.idleMessageConfig.idleDurationMilliseconds

integer

The duration in milliseconds that the user must be silent before an idle message is triggered.

Required range: `x >= 5000`

[​](#response-data-items-idle-message-config-one-of-0-max-idle-messages)

data.idleMessageConfig.maxIdleMessages

integer

The maximum number of idle messages that can be said during a call.

Required range: `x >= 1`

[​](#response-data-items-max-duration-seconds)

data.maxDurationSeconds

integer

default:10800

The maximum duration of the call in seconds.

[​](#response-data-items-default-voice-id)

data.defaultVoiceId

string

The default voice ID to use for the agent.

[​](#response-data-items-default-versioned-prompt-id)

data.defaultVersionedPromptId

string

The default versioned prompt ID to use for the agent.

[​](#response-data-items-default-extractor-id-one-of-0)

data.defaultExtractorId

string | null

The default extractor ID to use for the agent.

[​](#response-data-items-linked-function-definitions)

data.linkedFunctionDefinitions

object[]

The function definitions that should be available to this agent.

Show child attributes

[​](#response-data-items-linked-function-definitions-items-function-definition-id)

data.linkedFunctionDefinitions.functionDefinitionId

string

required

The ID of the function definition to link.

[​](#response-data-items-linked-function-definitions-items-lifecycle-messages-override)

data.linkedFunctionDefinitions.lifecycleMessagesOverride

object

Lifecycle messages to override the defaults for this function link, or null to not override.

Show child attributes

[​](#response-data-items-linked-function-definitions-items-lifecycle-messages-override-started)

data.linkedFunctionDefinitions.lifecycleMessagesOverride.started

string[]

required

Messages to display when the function starts executing. One will be chosen at random.

[​](#response-data-items-fill-empty-string-variables)

data.fillEmptyStringVariables

boolean

If true, variables that are not specified will be filled with empty strings instead of being left as template placeholders.

[​](#response-cursor-one-of-0)

cursor

string | null

required

A cursor you can pass to /agents to fetch the next page. If no next page exists, the cursor will be null.

[Get Dial Token](/api-reference/get-dial-token)[Create Agent](/api-reference/create-agent)