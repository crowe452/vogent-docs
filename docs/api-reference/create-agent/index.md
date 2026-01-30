[Skip to main content](https://docs.vogent.ai/api-reference/create-agent#content-area)
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
Create Agent
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


Create Agent
cURL
Copy
```
curl --request POST \
 --url https://api.vogent.ai/api/agents \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: application/json' \
 --data '
{
 "name": "<string>",
 "defaultVoiceId": "<string>",
 "defaultVersionedPrompt": {
  "aiModelId": "<string>",
  "agentType": "STANDARD",
  "name": "<string>",
  "prompt": "<string>",
  "flowDefinition": {
   "nodes": [
    {
     "id": "<string>",
     "name": "<string>",
     "type": "<string>",
     "transitionRules": [
      {
       "conditionType": "always",
       "transitionNodeId": "<string>",
       "arrayConditionType": "any",
       "field": "<string>",
       "value": "<string>",
       "values": [
        "<string>"
       ]
      }
     ],
     "nodeData": {}
    }
   ],
   "globalContext": "<string>",
   "aiOpen": true,
   "openingLineType": "INBOUND_ONLY"
  },
  "modelOptionValues": [
   {
    "optionId": "<string>",
    "value": "<string>"
   }
  ]
 },
 "defaultExtractor": {
  "name": "<string>",
  "extractorFieldsJsonSchema": "<string>"
 },
 "inboundWebhookResponse": true,
 "inboundWebhookUrl": "<string>",
 "maxDurationSeconds": 10800,
 "openingLine": {
  "lineType": "INBOUND_ONLY",
  "content": "<string>"
 },
 "voiceVolumeLevel": -100,
 "backgroundNoiseType": "office",
 "linkedFunctionDefinitionIds": [
  "<string>"
 ],
 "linkedFunctionDefinitionInputs": [
  {
   "functionDefinitionId": "<string>",
   "lifecycleMessagesOverride": {
    "started": [
     "<string>"
    ]
   }
  }
 ],
 "metadata": {},
 "transcriberParams": {
  "type": "deepgram",
  "keywords": [
   "<string>"
  ]
 },
 "idleMessageConfig": {
  "enabled": true,
  "messages": [
   "<string>"
  ],
  "idleDurationMilliseconds": 5001,
  "maxIdleMessages": 2
 },
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
 "language": "en",
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
'
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
curl --request POST \
 --url https://api.vogent.ai/api/agents \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: application/json' \
 --data '
{
 "name": "<string>",
 "defaultVoiceId": "<string>",
 "defaultVersionedPrompt": {
  "aiModelId": "<string>",
  "agentType": "STANDARD",
  "name": "<string>",
  "prompt": "<string>",
  "flowDefinition": {
   "nodes": [
    {
     "id": "<string>",
     "name": "<string>",
     "type": "<string>",
     "transitionRules": [
      {
       "conditionType": "always",
       "transitionNodeId": "<string>",
       "arrayConditionType": "any",
       "field": "<string>",
       "value": "<string>",
       "values": [
        "<string>"
       ]
      }
     ],
     "nodeData": {}
    }
   ],
   "globalContext": "<string>",
   "aiOpen": true,
   "openingLineType": "INBOUND_ONLY"
  },
  "modelOptionValues": [
   {
    "optionId": "<string>",
    "value": "<string>"
   }
  ]
 },
 "defaultExtractor": {
  "name": "<string>",
  "extractorFieldsJsonSchema": "<string>"
 },
 "inboundWebhookResponse": true,
 "inboundWebhookUrl": "<string>",
 "maxDurationSeconds": 10800,
 "openingLine": {
  "lineType": "INBOUND_ONLY",
  "content": "<string>"
 },
 "voiceVolumeLevel": -100,
 "backgroundNoiseType": "office",
 "linkedFunctionDefinitionIds": [
  "<string>"
 ],
 "linkedFunctionDefinitionInputs": [
  {
   "functionDefinitionId": "<string>",
   "lifecycleMessagesOverride": {
    "started": [
     "<string>"
    ]
   }
  }
 ],
 "metadata": {},
 "transcriberParams": {
  "type": "deepgram",
  "keywords": [
   "<string>"
  ]
 },
 "idleMessageConfig": {
  "enabled": true,
  "messages": [
   "<string>"
  ],
  "idleDurationMilliseconds": 5001,
  "maxIdleMessages": 2
 },
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
 "language": "en",
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
'
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
[​](https://docs.vogent.ai/api-reference/create-agent#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Body
application/json
Create a new agent
[​](https://docs.vogent.ai/api-reference/create-agent#body-name)
name
string
required
The name of the agent.
[​](https://docs.vogent.ai/api-reference/create-agent#body-default-voice-id)
defaultVoiceId
string
required
The ID of the voice to use.
[​](https://docs.vogent.ai/api-reference/create-agent#body-default-versioned-prompt)
defaultVersionedPrompt
object
required
The default versioned prompt to use for this agent.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#body-default-extractor-one-of-0)
defaultExtractor
object
The default extractor to use for this agent.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#body-inbound-webhook-response)
inboundWebhookResponse
boolean
[​](https://docs.vogent.ai/api-reference/create-agent#body-inbound-webhook-url)
inboundWebhookUrl
string
[​](https://docs.vogent.ai/api-reference/create-agent#body-max-duration-seconds)
maxDurationSeconds
integer
default:10800
The maximum duration of the call in seconds.
[​](https://docs.vogent.ai/api-reference/create-agent#body-opening-line-one-of-0)
openingLine
object
Details about the Agent's opening line. If unspecified, or null no opening line will be created.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#body-voice-volume-level-one-of-0)
voiceVolumeLevel
integer | null
default:-100
A value, generally between -300 and 300, indicating the volume level to use for the voice. The default is -100.
[​](https://docs.vogent.ai/api-reference/create-agent#body-background-noise-type)
backgroundNoiseType
enum<string>
default:office
The background audio that's used by the agent.
Available options: 
`noise`, 
`office`, 
`silence`
[​](https://docs.vogent.ai/api-reference/create-agent#body-linked-function-definition-ids)
linkedFunctionDefinitionIds
string[]
The function definitions that should be available to this agent (deprecated, use linkedFunctionDefinitionInputs instead)
[​](https://docs.vogent.ai/api-reference/create-agent#body-linked-function-definition-inputs)
linkedFunctionDefinitionInputs
object[]
The function definitions that should be available to this agent with optional lifecycle message overrides
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#body-metadata)
metadata
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#body-transcriber-params-one-of-0)
transcriberParams
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#body-idle-message-config)
idleMessageConfig
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#body-utterance-detector-config)
utteranceDetectorConfig
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#body-endpoint-detector-config-one-of-0)
endpointDetectorConfig
object
Configuration for endpoint detection to determine when a user has finished speaking. If not specified, will default to a semantic detector in the default mode.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#body-ivr-configuration-one-of-0)
ivrConfiguration
object
The configuration for IVR detection and navigation including detection type, prompt, voice, and tagging settings.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#body-language)
language
string
default:en
The language to use for the agent.
[​](https://docs.vogent.ai/api-reference/create-agent#body-fill-empty-string-variables-one-of-0)
fillEmptyStringVariables
boolean | null
If true, variables that are not specified will be filled with empty strings instead of being left as template placeholders.
[​](https://docs.vogent.ai/api-reference/create-agent#body-silence-hangup-configuration-one-of-0)
silenceHangupConfiguration
object
Configuration for automatically hanging up the call after a period of silence.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#body-voice-option-values)
voiceOptionValues
object[]
An optional configuration for the voice being used.
Show child attributes
#### Response
200
application/json
Successful operation
[​](https://docs.vogent.ai/api-reference/create-agent#response-id)
id
string
required
[​](https://docs.vogent.ai/api-reference/create-agent#response-name)
name
string
required
[​](https://docs.vogent.ai/api-reference/create-agent#response-language)
language
string
required
The language to use for the agent.
[​](https://docs.vogent.ai/api-reference/create-agent#response-transcriber-params-one-of-0)
transcriberParams
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#response-metadata)
metadata
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#response-utterance-detector-config)
utteranceDetectorConfig
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#response-endpoint-detector-config-one-of-0)
endpointDetectorConfig
object
Configuration for endpoint detection to determine when a user has finished speaking.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#response-ivr-configuration-one-of-0)
ivrConfiguration
object
The configuration for IVR detection and navigation including detection type, prompt, voice, and tagging settings.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#response-idle-message-config-one-of-0)
idleMessageConfig
object
Configuration for idle messages that the agent can say when the user is silent.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#response-max-duration-seconds)
maxDurationSeconds
integer
default:10800
The maximum duration of the call in seconds.
[​](https://docs.vogent.ai/api-reference/create-agent#response-default-voice-id)
defaultVoiceId
string
The default voice ID to use for the agent.
[​](https://docs.vogent.ai/api-reference/create-agent#response-default-versioned-prompt-id)
defaultVersionedPromptId
string
The default versioned prompt ID to use for the agent.
[​](https://docs.vogent.ai/api-reference/create-agent#response-default-extractor-id-one-of-0)
defaultExtractorId
string | null
The default extractor ID to use for the agent.
[​](https://docs.vogent.ai/api-reference/create-agent#response-linked-function-definitions)
linkedFunctionDefinitions
object[]
The function definitions that should be available to this agent.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#response-fill-empty-string-variables)
fillEmptyStringVariables
boolean
If true, variables that are not specified will be filled with empty strings instead of being left as template placeholders.
[​](https://docs.vogent.ai/api-reference/create-agent#response-silence-hangup-configuration-one-of-0)
silenceHangupConfiguration
object
Configuration for automatically hanging up the call after a period of silence.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-agent#response-voice-option-values)
voiceOptionValues
object[]
The configuration values for the voice being used by the agent.
Show child attributes
[List Agents](https://docs.vogent.ai/api-reference/list-agents)[Update Agent](https://docs.vogent.ai/api-reference/update-agent)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
