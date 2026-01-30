[Skip to main content](https://docs.vogent.ai/api-reference/delete-agent#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Agents
Delete Agent
[Guides](https://docs.vogent.ai/introduction)[API Reference](https://docs.vogent.ai/api-reference/introduction)[SDK](https://docs.vogent.ai/sdk/web-sdk)[Voicelab](https://docs.vogent.ai/voicelab/introduction)
##### API Documentation
  * [Introduction](https://docs.vogent.ai/api-reference/introduction)


##### Dials
  * [POSTCreate a new dial](https://docs.vogent.ai/api-reference/create-a-new-dial)
  * [POSTHangup Dial.](https://docs.vogent.ai/api-reference/hangup-dial)
  * [GETGet Dial](https://docs.vogent.ai/api-reference/get-dial)
  * [POSTGet Dial Token](https://docs.vogent.ai/api-reference/get-dial-token)


##### Agents
  * [GETList Agents](https://docs.vogent.ai/api-reference/list-agents)
  * [POSTCreate Agent](https://docs.vogent.ai/api-reference/create-agent)
  * [PUTUpdate Agent](https://docs.vogent.ai/api-reference/update-agent)
  * [DELDelete Agent](https://docs.vogent.ai/api-reference/delete-agent)


##### Voices
  * [POSTClone Voice](https://docs.vogent.ai/api-reference/clone-voice)
  * [GETList Voices](https://docs.vogent.ai/api-reference/list-voices)


##### Versioned Prompts
  * [GETList versioned prompts](https://docs.vogent.ai/api-reference/list-versioned-prompts)
  * [GETGet versioned prompt](https://docs.vogent.ai/api-reference/get-versioned-prompt)
  * [PUTUpdate versioned prompt](https://docs.vogent.ai/api-reference/update-versioned-prompt)
  * [POSTCreate versioned prompt](https://docs.vogent.ai/api-reference/create-versioned-prompt)


##### Extractors
  * [GETGet extractor](https://docs.vogent.ai/api-reference/get-extractor)
  * [GETList extractors](https://docs.vogent.ai/api-reference/list-extractors)
  * [POSTCreate extractor](https://docs.vogent.ai/api-reference/create-extractor)
  * [PUTUpdate extractor](https://docs.vogent.ai/api-reference/update-extractor)


##### Phone Numbers
  * [GETList phone numbers](https://docs.vogent.ai/api-reference/list-phone-numbers)
  * [GETGet Phone Number](https://docs.vogent.ai/api-reference/get-phone-number)
  * [PUTUpdate Phone Number](https://docs.vogent.ai/api-reference/update-phone-number)
  * [POSTCreate a phone number](https://docs.vogent.ai/api-reference/create-number)
  * [POSTSearch for available numbers](https://docs.vogent.ai/api-reference/search-for-available-numbers)
  * [POSTPurchase available number (deprecated, use /phone_numbers instead)](https://docs.vogent.ai/api-reference/purchase-available-number)
  * [DELDelete Phone Number](https://docs.vogent.ai/api-reference/delete-phone-number)


##### Functions
  * [POSTCreate a function](https://docs.vogent.ai/api-reference/create-a-function)
  * [GETGet function](https://docs.vogent.ai/api-reference/get-function)
  * [PUTUpdate function](https://docs.vogent.ai/api-reference/update-function)
  * [DELDelete function](https://docs.vogent.ai/api-reference/delete-function)


##### Models
  * [GETList Models](https://docs.vogent.ai/api-reference/list-models)


##### Voicelab
  * [POSTRun TTS Model](https://docs.vogent.ai/api-reference/run-tts-model)
  * [POSTRun Multispeaker TTS Model](https://docs.vogent.ai/api-reference/run-multispeaker-tts-model)
  * [WSSWebsocket TTS](https://docs.vogent.ai/api-reference/voicelab-websocket-tts)


##### Batch Dials
  * [GETList Batch Jobs](https://docs.vogent.ai/api-reference/list-batch-dial-jobs)
  * [POSTCreate Batch Job](https://docs.vogent.ai/api-reference/create-a-new-batch-dial-job)
  * [GETGet Batch Job](https://docs.vogent.ai/api-reference/get-batch-dial-job)
  * [PUTUpdate Batch Job](https://docs.vogent.ai/api-reference/update-batch-dial-job)
  * [GETList Queued Batch Dials](https://docs.vogent.ai/api-reference/list-queued-dials-for-batch-dial-job)
  * [POSTPause/Resume Batch Job](https://docs.vogent.ai/api-reference/set-batch-dial-job-paused)
  * [GETList Batch Dials](https://docs.vogent.ai/api-reference/list-batch-dials)


Delete Agent
cURL
Copy
```
curl --request DELETE \
 --url https://api.vogent.ai/api/agents/{id} \
 --header 'Authorization: Bearer <token>'
```

200
Copy
```
{
 "id": "<string>",
 "name": "<string>",
 "language": "<string>",
 "transcriberParams": {
  "type": "deepgram",
  "keywords": [
   "<string>"
  ]
 },
 "metadata": {},
 "utteranceDetectorConfig": {
  "sensitivity": "ULTRA_FAST",
  "interruptionPlayTimeMs": 123
 },
 "endpointDetectorConfig": {
  "type": "SIMPLE",
  "mode": "CONSERVATIVE"
 },
 "ivrConfiguration": {
  "detectionType": "NONE",
  "versionedPromptId": "<string>",
  "aiVoiceId": "<string>",
  "taggingText": "<string>"
 },
 "idleMessageConfig": {
  "enabled": true,
  "messages": [
   "<string>"
  ],
  "idleDurationMilliseconds": 5001,
  "maxIdleMessages": 2
 },
 "maxDurationSeconds": 10800,
 "defaultVoiceId": "<string>",
 "defaultVersionedPromptId": "<string>",
 "defaultExtractorId": "<string>",
 "linkedFunctionDefinitions": [
  {
   "functionDefinitionId": "<string>",
   "lifecycleMessagesOverride": {
    "started": [
     "<string>"
    ]
   }
  }
 ],
 "fillEmptyStringVariables": true,
 "silenceHangupConfiguration": {
  "type": "DISABLED",
  "silenceDurationSeconds": 123
 },
 "voiceOptionValues": [
  {
   "optionId": "<string>",
   "value": "<string>"
  }
 ]
}
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
curl --request DELETE \
 --url https://api.vogent.ai/api/agents/{id} \
 --header 'Authorization: Bearer <token>'
```

200
Copy
```
{
 "id": "<string>",
 "name": "<string>",
 "language": "<string>",
 "transcriberParams": {
  "type": "deepgram",
  "keywords": [
   "<string>"
  ]
 },
 "metadata": {},
 "utteranceDetectorConfig": {
  "sensitivity": "ULTRA_FAST",
  "interruptionPlayTimeMs": 123
 },
 "endpointDetectorConfig": {
  "type": "SIMPLE",
  "mode": "CONSERVATIVE"
 },
 "ivrConfiguration": {
  "detectionType": "NONE",
  "versionedPromptId": "<string>",
  "aiVoiceId": "<string>",
  "taggingText": "<string>"
 },
 "idleMessageConfig": {
  "enabled": true,
  "messages": [
   "<string>"
  ],
  "idleDurationMilliseconds": 5001,
  "maxIdleMessages": 2
 },
 "maxDurationSeconds": 10800,
 "defaultVoiceId": "<string>",
 "defaultVersionedPromptId": "<string>",
 "defaultExtractorId": "<string>",
 "linkedFunctionDefinitions": [
  {
   "functionDefinitionId": "<string>",
   "lifecycleMessagesOverride": {
    "started": [
     "<string>"
    ]
   }
  }
 ],
 "fillEmptyStringVariables": true,
 "silenceHangupConfiguration": {
  "type": "DISABLED",
  "silenceDurationSeconds": 123
 },
 "voiceOptionValues": [
  {
   "optionId": "<string>",
   "value": "<string>"
  }
 ]
}
```

#### Authorizations
[​](https://docs.vogent.ai/api-reference/delete-agent#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Path Parameters
[​](https://docs.vogent.ai/api-reference/delete-agent#parameter-id)
id
string
required
ID of the agent.
#### Response
200
application/json
Successful operation
[​](https://docs.vogent.ai/api-reference/delete-agent#response-id)
id
string
required
[​](https://docs.vogent.ai/api-reference/delete-agent#response-name)
name
string
required
[​](https://docs.vogent.ai/api-reference/delete-agent#response-language)
language
string
required
The language to use for the agent.
[​](https://docs.vogent.ai/api-reference/delete-agent#response-transcriber-params-one-of-0)
transcriberParams
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/delete-agent#response-metadata)
metadata
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/delete-agent#response-utterance-detector-config)
utteranceDetectorConfig
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/delete-agent#response-endpoint-detector-config-one-of-0)
endpointDetectorConfig
object
Configuration for endpoint detection to determine when a user has finished speaking.
Show child attributes
[​](https://docs.vogent.ai/api-reference/delete-agent#response-ivr-configuration-one-of-0)
ivrConfiguration
object
The configuration for IVR detection and navigation including detection type, prompt, voice, and tagging settings.
Show child attributes
[​](https://docs.vogent.ai/api-reference/delete-agent#response-idle-message-config-one-of-0)
idleMessageConfig
object
Configuration for idle messages that the agent can say when the user is silent.
Show child attributes
[​](https://docs.vogent.ai/api-reference/delete-agent#response-max-duration-seconds)
maxDurationSeconds
integer
default:10800
The maximum duration of the call in seconds.
[​](https://docs.vogent.ai/api-reference/delete-agent#response-default-voice-id)
defaultVoiceId
string
The default voice ID to use for the agent.
[​](https://docs.vogent.ai/api-reference/delete-agent#response-default-versioned-prompt-id)
defaultVersionedPromptId
string
The default versioned prompt ID to use for the agent.
[​](https://docs.vogent.ai/api-reference/delete-agent#response-default-extractor-id-one-of-0)
defaultExtractorId
string | null
The default extractor ID to use for the agent.
[​](https://docs.vogent.ai/api-reference/delete-agent#response-linked-function-definitions)
linkedFunctionDefinitions
object[]
The function definitions that should be available to this agent.
Show child attributes
[​](https://docs.vogent.ai/api-reference/delete-agent#response-fill-empty-string-variables)
fillEmptyStringVariables
boolean
If true, variables that are not specified will be filled with empty strings instead of being left as template placeholders.
[​](https://docs.vogent.ai/api-reference/delete-agent#response-silence-hangup-configuration-one-of-0)
silenceHangupConfiguration
object
Configuration for automatically hanging up the call after a period of silence.
Show child attributes
[​](https://docs.vogent.ai/api-reference/delete-agent#response-voice-option-values)
voiceOptionValues
object[]
The configuration values for the voice being used by the agent.
Show child attributes
[Update Agent](https://docs.vogent.ai/api-reference/update-agent)[Clone Voice](https://docs.vogent.ai/api-reference/clone-voice)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
