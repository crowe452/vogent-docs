Dials

Get Dial



  



        



        



    



        



        



              



        



  



      



              


Get Dial

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/dials/{id} \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "toNumber": "<string>", "agent": { "id": "<string>", "name": "<string>", "language": "<string>", "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "metadata": {}, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "aiVoiceId": "<string>", "taggingText": "<string>" }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "maxDurationSeconds": 10800, "defaultVoiceId": "<string>", "defaultVersionedPromptId": "<string>", "defaultExtractorId": "<string>", "linkedFunctionDefinitions": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "fillEmptyStringVariables": true }, "recordings": [ { "url": "<string>" } ], "transcript": [ { "text": "<string>", "speaker": "<string>", "detailType": "<string>", "functionCallId": "<string>", "startTimeMs": 123, "endTimeMs": 123, "functionCalls": [ { "name": "<string>", "args": "<string>", "functionCallId": "<string>" } ], "nodeTransition": { "toNodeId": "<string>", "transitionData": {} } } ], "durationSeconds": 123, "aiResult": {}, "inputs": {}, "status": "<string>", "dialTaskId": "<string>", "fromNumberId": "<string>", "startedAt": "2023-11-07T05:31:56Z", "endedAt": "2023-11-07T05:31:56Z", "createdAt": "2023-11-07T05:31:56Z", "updatedAt": "2023-11-07T05:31:56Z", "systemResultType": "BUSY", "voiceId": "<string>", "versionedPromptId": "<string>" }`
```

Dials

# Get Dial

Gets the details of a dial.

GET

/

dials

/

{id}

Try it

Get Dial

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/dials/{id} \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "toNumber": "<string>", "agent": { "id": "<string>", "name": "<string>", "language": "<string>", "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "metadata": {}, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "aiVoiceId": "<string>", "taggingText": "<string>" }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "maxDurationSeconds": 10800, "defaultVoiceId": "<string>", "defaultVersionedPromptId": "<string>", "defaultExtractorId": "<string>", "linkedFunctionDefinitions": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "fillEmptyStringVariables": true }, "recordings": [ { "url": "<string>" } ], "transcript": [ { "text": "<string>", "speaker": "<string>", "detailType": "<string>", "functionCallId": "<string>", "startTimeMs": 123, "endTimeMs": 123, "functionCalls": [ { "name": "<string>", "args": "<string>", "functionCallId": "<string>" } ], "nodeTransition": { "toNodeId": "<string>", "transitionData": {} } } ], "durationSeconds": 123, "aiResult": {}, "inputs": {}, "status": "<string>", "dialTaskId": "<string>", "fromNumberId": "<string>", "startedAt": "2023-11-07T05:31:56Z", "endedAt": "2023-11-07T05:31:56Z", "createdAt": "2023-11-07T05:31:56Z", "updatedAt": "2023-11-07T05:31:56Z", "systemResultType": "BUSY", "voiceId": "<string>", "versionedPromptId": "<string>" }`
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

ID of the dial.

#### Response

200

application/json

Successful operation

[​](#response-id)

id

string

required

[​](#response-to-number)

toNumber

string

[​](#response-agent)

agent

object

Show child attributes

[​](#response-agent-id)

agent.id

string

required

[​](#response-agent-name)

agent.name

string

required

[​](#response-agent-language)

agent.language

string

required

The language to use for the agent.

[​](#response-agent-transcriber-params-one-of-0)

agent.transcriberParams

object

Show child attributes

[​](#response-agent-transcriber-params-one-of-0-type)

agent.transcriberParams.type

enum<string>

required

Available options: 

`deepgram`, 

`openai`

[​](#response-agent-transcriber-params-one-of-0-keywords)

agent.transcriberParams.keywords

string[]

Keywords to be used for transcription.

[​](#response-agent-metadata)

agent.metadata

object

Show child attributes

[​](#response-agent-metadata-additional-properties)

agent.metadata.{key}

any

[​](#response-agent-utterance-detector-config)

agent.utteranceDetectorConfig

object

Show child attributes

[​](#response-agent-utterance-detector-config-sensitivity)

agent.utteranceDetectorConfig.sensitivity

enum<string>

required

Available options: 

`ULTRA_FAST`, 

`FAST`, 

`MEDIUM`, 

`SLOW`

[​](#response-agent-endpoint-detector-config-one-of-0)

agent.endpointDetectorConfig

object

Configuration for endpoint detection to determine when a user has finished speaking.

Show child attributes

[​](#response-agent-endpoint-detector-config-one-of-0-type)

agent.endpointDetectorConfig.type

enum<string>

required

The type of endpoint detector to use.

Available options: 

`SIMPLE`, 

`SEMANTIC`

[​](#response-agent-endpoint-detector-config-one-of-0-mode-one-of-0)

agent.endpointDetectorConfig.mode

enum<string> | null

The mode for the endpoint detector (only applicable for SEMANTIC type).

Available options: 

`CONSERVATIVE`, 

`DEFAULT`, 

`AGGRESSIVE`

[​](#response-agent-ivr-configuration-one-of-0)

agent.ivrConfiguration

object

The configuration for IVR detection and navigation including detection type, prompt, voice, and tagging settings.

Show child attributes

[​](#response-agent-ivr-configuration-one-of-0-detection-type)

agent.ivrConfiguration.detectionType

enum<string>

required

The type of IVR detection to use.

Available options: 

`NONE`, 

`STANDARD`

[​](#response-agent-ivr-configuration-one-of-0-versioned-prompt-id-one-of-0)

agent.ivrConfiguration.versionedPromptId

string | null

The versioned prompt ID to use for IVR detection.

[​](#response-agent-ivr-configuration-one-of-0-ai-voice-id-one-of-0)

agent.ivrConfiguration.aiVoiceId

string | null

The AI voice ID to use for IVR detection.

[​](#response-agent-ivr-configuration-one-of-0-tagging-text-one-of-0)

agent.ivrConfiguration.taggingText

string | null

The tagging text for IVR detection.

[​](#response-agent-idle-message-config-one-of-0)

agent.idleMessageConfig

object

Configuration for idle messages that the agent can say when the user is silent.

Show child attributes

[​](#response-agent-idle-message-config-one-of-0-enabled)

agent.idleMessageConfig.enabled

boolean

required

Whether idle messages are enabled for this agent.

[​](#response-agent-idle-message-config-one-of-0-messages)

agent.idleMessageConfig.messages

string[]

The list of idle messages that the agent can say when the user is silent.

[​](#response-agent-idle-message-config-one-of-0-idle-duration-milliseconds)

agent.idleMessageConfig.idleDurationMilliseconds

integer

The duration in milliseconds that the user must be silent before an idle message is triggered.

Required range: `x >= 5000`

[​](#response-agent-idle-message-config-one-of-0-max-idle-messages)

agent.idleMessageConfig.maxIdleMessages

integer

The maximum number of idle messages that can be said during a call.

Required range: `x >= 1`

[​](#response-agent-max-duration-seconds)

agent.maxDurationSeconds

integer

default:10800

The maximum duration of the call in seconds.

[​](#response-agent-default-voice-id)

agent.defaultVoiceId

string

The default voice ID to use for the agent.

[​](#response-agent-default-versioned-prompt-id)

agent.defaultVersionedPromptId

string

The default versioned prompt ID to use for the agent.

[​](#response-agent-default-extractor-id-one-of-0)

agent.defaultExtractorId

string | null

The default extractor ID to use for the agent.

[​](#response-agent-linked-function-definitions)

agent.linkedFunctionDefinitions

object[]

The function definitions that should be available to this agent.

Show child attributes

[​](#response-agent-linked-function-definitions-items-function-definition-id)

agent.linkedFunctionDefinitions.functionDefinitionId

string

required

The ID of the function definition to link.

[​](#response-agent-linked-function-definitions-items-lifecycle-messages-override)

agent.linkedFunctionDefinitions.lifecycleMessagesOverride

object

Lifecycle messages to override the defaults for this function link, or null to not override.

Show child attributes

[​](#response-agent-linked-function-definitions-items-lifecycle-messages-override-started)

agent.linkedFunctionDefinitions.lifecycleMessagesOverride.started

string[]

required

Messages to display when the function starts executing. One will be chosen at random.

[​](#response-agent-fill-empty-string-variables)

agent.fillEmptyStringVariables

boolean

If true, variables that are not specified will be filled with empty strings instead of being left as template placeholders.

[​](#response-recordings)

recordings

object[]

Show child attributes

[​](#response-recordings-items-url)

recordings.url

string

required

A URL that can be used to download the recording of the call. Be sure to include an API key in the header to access the recording.

[​](#response-transcript)

transcript

object[]

Show child attributes

[​](#response-transcript-items-text)

transcript.text

string

required

[​](#response-transcript-items-speaker)

transcript.speaker

string

required

Either `HUMAN` or `AI`, indicating the speaker type. If this is a function call result the speaker will be `AI`, while the `detailType` will be `function`.

[​](#response-transcript-items-detail-type-one-of-0)

transcript.detailType

string | null

Will be `function` if this is a function result, otherwise `null`.

[​](#response-transcript-items-function-call-id)

transcript.functionCallId

string

The function call ID if this is a tool call result.

[​](#response-transcript-items-start-time-ms)

transcript.startTimeMs

integer

[​](#response-transcript-items-end-time-ms)

transcript.endTimeMs

integer

[​](#response-transcript-items-function-calls)

transcript.functionCalls

object[]

Show child attributes

[​](#response-transcript-items-function-calls-items-name)

transcript.functionCalls.name

string

required

[​](#response-transcript-items-function-calls-items-args)

transcript.functionCalls.args

string

required

The arguments to the function call, JSON encoded if it is an object.

[​](#response-transcript-items-function-calls-items-function-call-id)

transcript.functionCalls.functionCallId

string

[​](#response-transcript-items-node-transition)

transcript.nodeTransition

object

Show child attributes

[​](#response-transcript-items-node-transition-to-node-id)

transcript.nodeTransition.toNodeId

string

required

[​](#response-transcript-items-node-transition-transition-data-one-of-0)

transcript.nodeTransition.transitionData

object

required

Show child attributes

[​](#response-transcript-items-node-transition-transition-data-one-of-0-additional-properties)

transcript.nodeTransition.transitionData.{key}

any

[​](#response-duration-seconds)

durationSeconds

integer

[​](#response-ai-result)

aiResult

object

Show child attributes

[​](#response-ai-result-additional-properties)

aiResult.{key}

any

[​](#response-inputs)

inputs

object

Show child attributes

[​](#response-inputs-additional-properties)

inputs.{key}

any

[​](#response-status)

status

string

[​](#response-dial-task-id)

dialTaskId

string

[​](#response-from-number-id)

fromNumberId

string

[​](#response-started-at)

startedAt

string<date-time>

[​](#response-ended-at)

endedAt

string<date-time>

[​](#response-created-at)

createdAt

string<date-time>

[​](#response-updated-at)

updatedAt

string<date-time>

[​](#response-system-result-type-one-of-0)

systemResultType

enum<string> | null

The type of system result for this dial, if applicable.

Available options: 

`BUSY`, 

`FAILED`, 

`NO_ANSWER`, 

`CANCELLED`, 

`USER_HANGUP`, 

`COUNTERPARTY_HANGUP`, 

`TIMEOUT`, 

`RATE_LIMITED`, 

`TRANSFERRED`, 

`AGENT_HANGUP`, 

`VOICEMAIL_DETECTED_HANGUP`, 

`LONG_SILENCE_HANGUP`

[​](#response-voice-id)

voiceId

string

[​](#response-versioned-prompt-id)

versionedPromptId

string

[Hangup Dial.](/api-reference/hangup-dial)[Get Dial Token](/api-reference/get-dial-token)