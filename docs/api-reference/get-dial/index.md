[Skip to main content](https://docs.vogent.ai/api-reference/get-dial#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Dials
Get Dial
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


Get Dial
cURL
Copy
```
curl --request GET \
 --url https://api.vogent.ai/api/dials/{id} \
 --header 'Authorization: Bearer <token>'
```

200
Copy
```
{
 "id": "<string>",
 "toNumber": "<string>",
 "agent": {
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
 },
 "recordings": [
  {
   "url": "<string>"
  }
 ],
 "transcript": [
  {
   "text": "<string>",
   "speaker": "<string>",
   "detailType": "<string>",
   "functionCallId": "<string>",
   "startTimeMs": 123,
   "endTimeMs": 123,
   "functionCalls": [
    {
     "name": "<string>",
     "args": "<string>",
     "functionCallId": "<string>"
    }
   ],
   "nodeTransition": {
    "toNodeId": "<string>",
    "transitionData": {}
   }
  }
 ],
 "durationSeconds": 123,
 "aiResult": {},
 "inputs": {},
 "status": "<string>",
 "dialTaskId": "<string>",
 "fromNumberId": "<string>",
 "startedAt": "2023-11-07T05:31:56Z",
 "endedAt": "2023-11-07T05:31:56Z",
 "createdAt": "2023-11-07T05:31:56Z",
 "updatedAt": "2023-11-07T05:31:56Z",
 "systemResultType": "BUSY",
 "voiceId": "<string>",
 "versionedPromptId": "<string>"
}
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
curl --request GET \
 --url https://api.vogent.ai/api/dials/{id} \
 --header 'Authorization: Bearer <token>'
```

200
Copy
```
{
 "id": "<string>",
 "toNumber": "<string>",
 "agent": {
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
 },
 "recordings": [
  {
   "url": "<string>"
  }
 ],
 "transcript": [
  {
   "text": "<string>",
   "speaker": "<string>",
   "detailType": "<string>",
   "functionCallId": "<string>",
   "startTimeMs": 123,
   "endTimeMs": 123,
   "functionCalls": [
    {
     "name": "<string>",
     "args": "<string>",
     "functionCallId": "<string>"
    }
   ],
   "nodeTransition": {
    "toNodeId": "<string>",
    "transitionData": {}
   }
  }
 ],
 "durationSeconds": 123,
 "aiResult": {},
 "inputs": {},
 "status": "<string>",
 "dialTaskId": "<string>",
 "fromNumberId": "<string>",
 "startedAt": "2023-11-07T05:31:56Z",
 "endedAt": "2023-11-07T05:31:56Z",
 "createdAt": "2023-11-07T05:31:56Z",
 "updatedAt": "2023-11-07T05:31:56Z",
 "systemResultType": "BUSY",
 "voiceId": "<string>",
 "versionedPromptId": "<string>"
}
```

#### Authorizations
[​](https://docs.vogent.ai/api-reference/get-dial#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Path Parameters
[​](https://docs.vogent.ai/api-reference/get-dial#parameter-id)
id
string
required
ID of the dial.
#### Response
200
application/json
Successful operation
[​](https://docs.vogent.ai/api-reference/get-dial#response-id)
id
string
required
[​](https://docs.vogent.ai/api-reference/get-dial#response-to-number)
toNumber
string
[​](https://docs.vogent.ai/api-reference/get-dial#response-agent)
agent
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/get-dial#response-recordings)
recordings
object[]
Show child attributes
[​](https://docs.vogent.ai/api-reference/get-dial#response-transcript)
transcript
object[]
Show child attributes
[​](https://docs.vogent.ai/api-reference/get-dial#response-duration-seconds)
durationSeconds
integer
[​](https://docs.vogent.ai/api-reference/get-dial#response-ai-result)
aiResult
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/get-dial#response-inputs)
inputs
object
Show child attributes
[​](https://docs.vogent.ai/api-reference/get-dial#response-status)
status
string
[​](https://docs.vogent.ai/api-reference/get-dial#response-dial-task-id)
dialTaskId
string
[​](https://docs.vogent.ai/api-reference/get-dial#response-from-number-id)
fromNumberId
string
[​](https://docs.vogent.ai/api-reference/get-dial#response-started-at)
startedAt
string<date-time>
[​](https://docs.vogent.ai/api-reference/get-dial#response-ended-at)
endedAt
string<date-time>
[​](https://docs.vogent.ai/api-reference/get-dial#response-created-at)
createdAt
string<date-time>
[​](https://docs.vogent.ai/api-reference/get-dial#response-updated-at)
updatedAt
string<date-time>
[​](https://docs.vogent.ai/api-reference/get-dial#response-system-result-type-one-of-0)
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
[​](https://docs.vogent.ai/api-reference/get-dial#response-voice-id)
voiceId
string
[​](https://docs.vogent.ai/api-reference/get-dial#response-versioned-prompt-id)
versionedPromptId
string
[Hangup Dial.](https://docs.vogent.ai/api-reference/hangup-dial)[Get Dial Token](https://docs.vogent.ai/api-reference/get-dial-token)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
