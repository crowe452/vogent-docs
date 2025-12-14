Batch Dials

List Batch Dials



  



        



        



    



        



        



              



        



  



      



              


List Batch Dials

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/batch_dial_jobs/{id}/dials \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "toNumber": "<string>", "agent": { "id": "<string>", "name": "<string>", "language": "<string>", "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "metadata": {}, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "aiVoiceId": "<string>", "taggingText": "<string>" }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "maxDurationSeconds": 10800, "defaultVoiceId": "<string>", "defaultVersionedPromptId": "<string>", "defaultExtractorId": "<string>", "linkedFunctionDefinitions": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "fillEmptyStringVariables": true }, "recordings": [ { "url": "<string>" } ], "transcript": [ { "text": "<string>", "speaker": "<string>", "detailType": "<string>", "functionCallId": "<string>", "startTimeMs": 123, "endTimeMs": 123, "functionCalls": [ { "name": "<string>", "args": "<string>", "functionCallId": "<string>" } ], "nodeTransition": { "toNodeId": "<string>", "transitionData": {} } } ], "durationSeconds": 123, "aiResult": {}, "inputs": {}, "status": "<string>", "dialTaskId": "<string>", "fromNumberId": "<string>", "startedAt": "2023-11-07T05:31:56Z", "endedAt": "2023-11-07T05:31:56Z", "createdAt": "2023-11-07T05:31:56Z", "updatedAt": "2023-11-07T05:31:56Z", "systemResultType": "BUSY", "voiceId": "<string>", "versionedPromptId": "<string>" } ], "cursor": "<string>" }`
```

Batch Dials

# List Batch Dials

Lists completed dials that are associated with the batch job.

GET

/

batch_dial_jobs

/

{id}

/

dials

Try it

List Batch Dials

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/batch_dial_jobs/{id}/dials \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "data": [ { "id": "<string>", "toNumber": "<string>", "agent": { "id": "<string>", "name": "<string>", "language": "<string>", "transcriberParams": { "type": "deepgram", "keywords": [ "<string>" ] }, "metadata": {}, "utteranceDetectorConfig": { "sensitivity": "ULTRA_FAST" }, "endpointDetectorConfig": { "type": "SIMPLE", "mode": "CONSERVATIVE" }, "ivrConfiguration": { "detectionType": "NONE", "versionedPromptId": "<string>", "aiVoiceId": "<string>", "taggingText": "<string>" }, "idleMessageConfig": { "enabled": true, "messages": [ "<string>" ], "idleDurationMilliseconds": 5001, "maxIdleMessages": 2 }, "maxDurationSeconds": 10800, "defaultVoiceId": "<string>", "defaultVersionedPromptId": "<string>", "defaultExtractorId": "<string>", "linkedFunctionDefinitions": [ { "functionDefinitionId": "<string>", "lifecycleMessagesOverride": { "started": [ "<string>" ] } } ], "fillEmptyStringVariables": true }, "recordings": [ { "url": "<string>" } ], "transcript": [ { "text": "<string>", "speaker": "<string>", "detailType": "<string>", "functionCallId": "<string>", "startTimeMs": 123, "endTimeMs": 123, "functionCalls": [ { "name": "<string>", "args": "<string>", "functionCallId": "<string>" } ], "nodeTransition": { "toNodeId": "<string>", "transitionData": {} } } ], "durationSeconds": 123, "aiResult": {}, "inputs": {}, "status": "<string>", "dialTaskId": "<string>", "fromNumberId": "<string>", "startedAt": "2023-11-07T05:31:56Z", "endedAt": "2023-11-07T05:31:56Z", "createdAt": "2023-11-07T05:31:56Z", "updatedAt": "2023-11-07T05:31:56Z", "systemResultType": "BUSY", "voiceId": "<string>", "versionedPromptId": "<string>" } ], "cursor": "<string>" }`
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

ID of the batch dial job.

#### Query Parameters

[​](#parameter-limit)

limit

integer

The number of dials to return.

[​](#parameter-cursor)

cursor

string

The cursor for pagination.

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

[​](#response-data-items-to-number)

data.toNumber

string

[​](#response-data-items-agent)

data.agent

object

Show child attributes

[​](#response-data-items-agent-id)

data.agent.id

string

required

[​](#response-data-items-agent-name)

data.agent.name

string

required

[​](#response-data-items-agent-language)

data.agent.language

string

required

The language to use for the agent.

[​](#response-data-items-agent-transcriber-params-one-of-0)

data.agent.transcriberParams

object

Show child attributes

[​](#response-data-items-agent-transcriber-params-one-of-0-type)

data.agent.transcriberParams.type

enum<string>

required

Available options: 

`deepgram`, 

`openai`

[​](#response-data-items-agent-transcriber-params-one-of-0-keywords)

data.agent.transcriberParams.keywords

string[]

Keywords to be used for transcription.

[​](#response-data-items-agent-metadata)

data.agent.metadata

object

Show child attributes

[​](#response-data-items-agent-metadata-additional-properties)

data.agent.metadata.{key}

any

[​](#response-data-items-agent-utterance-detector-config)

data.agent.utteranceDetectorConfig

object

Show child attributes

[​](#response-data-items-agent-utterance-detector-config-sensitivity)

data.agent.utteranceDetectorConfig.sensitivity

enum<string>

required

Available options: 

`ULTRA_FAST`, 

`FAST`, 

`MEDIUM`, 

`SLOW`

[​](#response-data-items-agent-endpoint-detector-config-one-of-0)

data.agent.endpointDetectorConfig

object

Configuration for endpoint detection to determine when a user has finished speaking.

Show child attributes

[​](#response-data-items-agent-endpoint-detector-config-one-of-0-type)

data.agent.endpointDetectorConfig.type

enum<string>

required

The type of endpoint detector to use.

Available options: 

`SIMPLE`, 

`SEMANTIC`

[​](#response-data-items-agent-endpoint-detector-config-one-of-0-mode-one-of-0)

data.agent.endpointDetectorConfig.mode

enum<string> | null

The mode for the endpoint detector (only applicable for SEMANTIC type).

Available options: 

`CONSERVATIVE`, 

`DEFAULT`, 

`AGGRESSIVE`

[​](#response-data-items-agent-ivr-configuration-one-of-0)

data.agent.ivrConfiguration

object

The configuration for IVR detection and navigation including detection type, prompt, voice, and tagging settings.

Show child attributes

[​](#response-data-items-agent-ivr-configuration-one-of-0-detection-type)

data.agent.ivrConfiguration.detectionType

enum<string>

required

The type of IVR detection to use.

Available options: 

`NONE`, 

`STANDARD`

[​](#response-data-items-agent-ivr-configuration-one-of-0-versioned-prompt-id-one-of-0)

data.agent.ivrConfiguration.versionedPromptId

string | null

The versioned prompt ID to use for IVR detection.

[​](#response-data-items-agent-ivr-configuration-one-of-0-ai-voice-id-one-of-0)

data.agent.ivrConfiguration.aiVoiceId

string | null

The AI voice ID to use for IVR detection.

[​](#response-data-items-agent-ivr-configuration-one-of-0-tagging-text-one-of-0)

data.agent.ivrConfiguration.taggingText

string | null

The tagging text for IVR detection.

[​](#response-data-items-agent-idle-message-config-one-of-0)

data.agent.idleMessageConfig

object

Configuration for idle messages that the agent can say when the user is silent.

Show child attributes

[​](#response-data-items-agent-idle-message-config-one-of-0-enabled)

data.agent.idleMessageConfig.enabled

boolean

required

Whether idle messages are enabled for this agent.

[​](#response-data-items-agent-idle-message-config-one-of-0-messages)

data.agent.idleMessageConfig.messages

string[]

The list of idle messages that the agent can say when the user is silent.

[​](#response-data-items-agent-idle-message-config-one-of-0-idle-duration-milliseconds)

data.agent.idleMessageConfig.idleDurationMilliseconds

integer

The duration in milliseconds that the user must be silent before an idle message is triggered.

Required range: `x >= 5000`

[​](#response-data-items-agent-idle-message-config-one-of-0-max-idle-messages)

data.agent.idleMessageConfig.maxIdleMessages

integer

The maximum number of idle messages that can be said during a call.

Required range: `x >= 1`

[​](#response-data-items-agent-max-duration-seconds)

data.agent.maxDurationSeconds

integer

default:10800

The maximum duration of the call in seconds.

[​](#response-data-items-agent-default-voice-id)

data.agent.defaultVoiceId

string

The default voice ID to use for the agent.

[​](#response-data-items-agent-default-versioned-prompt-id)

data.agent.defaultVersionedPromptId

string

The default versioned prompt ID to use for the agent.

[​](#response-data-items-agent-default-extractor-id-one-of-0)

data.agent.defaultExtractorId

string | null

The default extractor ID to use for the agent.

[​](#response-data-items-agent-linked-function-definitions)

data.agent.linkedFunctionDefinitions

object[]

The function definitions that should be available to this agent.

Show child attributes

[​](#response-data-items-agent-linked-function-definitions-items-function-definition-id)

data.agent.linkedFunctionDefinitions.functionDefinitionId

string

required

The ID of the function definition to link.

[​](#response-data-items-agent-linked-function-definitions-items-lifecycle-messages-override)

data.agent.linkedFunctionDefinitions.lifecycleMessagesOverride

object

Lifecycle messages to override the defaults for this function link, or null to not override.

Show child attributes

[​](#response-data-items-agent-linked-function-definitions-items-lifecycle-messages-override-started)

data.agent.linkedFunctionDefinitions.lifecycleMessagesOverride.started

string[]

required

Messages to display when the function starts executing. One will be chosen at random.

[​](#response-data-items-agent-fill-empty-string-variables)

data.agent.fillEmptyStringVariables

boolean

If true, variables that are not specified will be filled with empty strings instead of being left as template placeholders.

[​](#response-data-items-recordings)

data.recordings

object[]

Show child attributes

[​](#response-data-items-recordings-items-url)

data.recordings.url

string

required

A URL that can be used to download the recording of the call. Be sure to include an API key in the header to access the recording.

[​](#response-data-items-transcript)

data.transcript

object[]

Show child attributes

[​](#response-data-items-transcript-items-text)

data.transcript.text

string

required

[​](#response-data-items-transcript-items-speaker)

data.transcript.speaker

string

required

Either `HUMAN` or `AI`, indicating the speaker type. If this is a function call result the speaker will be `AI`, while the `detailType` will be `function`.

[​](#response-data-items-transcript-items-detail-type-one-of-0)

data.transcript.detailType

string | null

Will be `function` if this is a function result, otherwise `null`.

[​](#response-data-items-transcript-items-function-call-id)

data.transcript.functionCallId

string

The function call ID if this is a tool call result.

[​](#response-data-items-transcript-items-start-time-ms)

data.transcript.startTimeMs

integer

[​](#response-data-items-transcript-items-end-time-ms)

data.transcript.endTimeMs

integer

[​](#response-data-items-transcript-items-function-calls)

data.transcript.functionCalls

object[]

Show child attributes

[​](#response-data-items-transcript-items-function-calls-items-name)

data.transcript.functionCalls.name

string

required

[​](#response-data-items-transcript-items-function-calls-items-args)

data.transcript.functionCalls.args

string

required

The arguments to the function call, JSON encoded if it is an object.

[​](#response-data-items-transcript-items-function-calls-items-function-call-id)

data.transcript.functionCalls.functionCallId

string

[​](#response-data-items-transcript-items-node-transition)

data.transcript.nodeTransition

object

Show child attributes

[​](#response-data-items-transcript-items-node-transition-to-node-id)

data.transcript.nodeTransition.toNodeId

string

required

[​](#response-data-items-transcript-items-node-transition-transition-data-one-of-0)

data.transcript.nodeTransition.transitionData

object

required

Show child attributes

[​](#response-data-items-transcript-items-node-transition-transition-data-one-of-0-additional-properties)

data.transcript.nodeTransition.transitionData.{key}

any

[​](#response-data-items-duration-seconds)

data.durationSeconds

integer

[​](#response-data-items-ai-result)

data.aiResult

object

Show child attributes

[​](#response-data-items-ai-result-additional-properties)

data.aiResult.{key}

any

[​](#response-data-items-inputs)

data.inputs

object

Show child attributes

[​](#response-data-items-inputs-additional-properties)

data.inputs.{key}

any

[​](#response-data-items-status)

data.status

string

[​](#response-data-items-dial-task-id)

data.dialTaskId

string

[​](#response-data-items-from-number-id)

data.fromNumberId

string

[​](#response-data-items-started-at)

data.startedAt

string<date-time>

[​](#response-data-items-ended-at)

data.endedAt

string<date-time>

[​](#response-data-items-created-at)

data.createdAt

string<date-time>

[​](#response-data-items-updated-at)

data.updatedAt

string<date-time>

[​](#response-data-items-system-result-type-one-of-0)

data.systemResultType

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

[​](#response-data-items-voice-id)

data.voiceId

string

[​](#response-data-items-versioned-prompt-id)

data.versionedPromptId

string

[​](#response-cursor-one-of-0)

cursor

string | null

required

[Pause/Resume Batch Job](/api-reference/set-batch-dial-job-paused)