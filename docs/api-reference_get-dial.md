[Skip to main content](http://docs.vogent.ai/api-reference/get-dial#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
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
[Guides](http://docs.vogent.ai/introduction)[API Reference](http://docs.vogent.ai/api-reference/introduction)[SDK](http://docs.vogent.ai/sdk/web-sdk)[Voicelab](http://docs.vogent.ai/voicelab/introduction)
##### API Documentation
  * [Introduction](http://docs.vogent.ai/api-reference/introduction)


##### Dials
  * [POSTCreate a new dial](http://docs.vogent.ai/api-reference/create-a-new-dial)
  * [POSTHangup Dial.](http://docs.vogent.ai/api-reference/hangup-dial)
  * [GETGet Dial](http://docs.vogent.ai/api-reference/get-dial)
  * [POSTGet Dial Token](http://docs.vogent.ai/api-reference/get-dial-token)


##### Agents
  * [GETList Agents](http://docs.vogent.ai/api-reference/list-agents)
  * [POSTCreate Agent](http://docs.vogent.ai/api-reference/create-agent)
  * [PUTUpdate Agent](http://docs.vogent.ai/api-reference/update-agent)
  * [DELDelete Agent](http://docs.vogent.ai/api-reference/delete-agent)


##### Voices
  * [POSTClone Voice](http://docs.vogent.ai/api-reference/clone-voice)
  * [GETList Voices](http://docs.vogent.ai/api-reference/list-voices)


##### Versioned Prompts
  * [GETList versioned prompts](http://docs.vogent.ai/api-reference/list-versioned-prompts)
  * [GETGet versioned prompt](http://docs.vogent.ai/api-reference/get-versioned-prompt)
  * [PUTUpdate versioned prompt](http://docs.vogent.ai/api-reference/update-versioned-prompt)
  * [POSTCreate versioned prompt](http://docs.vogent.ai/api-reference/create-versioned-prompt)


##### Extractors
  * [GETGet extractor](http://docs.vogent.ai/api-reference/get-extractor)
  * [GETList extractors](http://docs.vogent.ai/api-reference/list-extractors)
  * [POSTCreate extractor](http://docs.vogent.ai/api-reference/create-extractor)
  * [PUTUpdate extractor](http://docs.vogent.ai/api-reference/update-extractor)


##### Phone Numbers
  * [GETList phone numbers](http://docs.vogent.ai/api-reference/list-phone-numbers)
  * [GETGet Phone Number](http://docs.vogent.ai/api-reference/get-phone-number)
  * [PUTUpdate Phone Number](http://docs.vogent.ai/api-reference/update-phone-number)
  * [POSTCreate a phone number](http://docs.vogent.ai/api-reference/create-number)
  * [POSTSearch for available numbers](http://docs.vogent.ai/api-reference/search-for-available-numbers)
  * [POSTPurchase available number (deprecated, use /phone_numbers instead)](http://docs.vogent.ai/api-reference/purchase-available-number)
  * [DELDelete Phone Number](http://docs.vogent.ai/api-reference/delete-phone-number)


##### Functions
  * [POSTCreate a function](http://docs.vogent.ai/api-reference/create-a-function)
  * [GETGet function](http://docs.vogent.ai/api-reference/get-function)
  * [PUTUpdate function](http://docs.vogent.ai/api-reference/update-function)
  * [DELDelete function](http://docs.vogent.ai/api-reference/delete-function)


##### Models
  * [GETList Models](http://docs.vogent.ai/api-reference/list-models)


##### Voicelab
  * [POSTRun TTS Model](http://docs.vogent.ai/api-reference/run-tts-model)
  * [POSTRun Multispeaker TTS Model](http://docs.vogent.ai/api-reference/run-multispeaker-tts-model)
  * [WSSWebsocket TTS](http://docs.vogent.ai/api-reference/voicelab-websocket-tts)


##### Batch Dials
  * [GETList Batch Jobs](http://docs.vogent.ai/api-reference/list-batch-dial-jobs)
  * [POSTCreate Batch Job](http://docs.vogent.ai/api-reference/create-a-new-batch-dial-job)
  * [GETGet Batch Job](http://docs.vogent.ai/api-reference/get-batch-dial-job)
  * [PUTUpdate Batch Job](http://docs.vogent.ai/api-reference/update-batch-dial-job)
  * [GETList Queued Batch Dials](http://docs.vogent.ai/api-reference/list-queued-dials-for-batch-dial-job)
  * [POSTPause/Resume Batch Job](http://docs.vogent.ai/api-reference/set-batch-dial-job-paused)
  * [GETList Batch Dials](http://docs.vogent.ai/api-reference/list-batch-dials)


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
[​](http://docs.vogent.ai/api-reference/get-dial#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Path Parameters
[​](http://docs.vogent.ai/api-reference/get-dial#parameter-id)
id
string
required
ID of the dial.
#### Response
200
application/json
Successful operation
[​](http://docs.vogent.ai/api-reference/get-dial#response-id)
id
string
required
[​](http://docs.vogent.ai/api-reference/get-dial#response-to-number)
toNumber
string
[​](http://docs.vogent.ai/api-reference/get-dial#response-agent)
agent
object
Show child attributes
[​](http://docs.vogent.ai/api-reference/get-dial#response-recordings)
recordings
object[]
Show child attributes
[​](http://docs.vogent.ai/api-reference/get-dial#response-transcript)
transcript
object[]
Show child attributes
[​](http://docs.vogent.ai/api-reference/get-dial#response-duration-seconds)
durationSeconds
integer
[​](http://docs.vogent.ai/api-reference/get-dial#response-ai-result)
aiResult
object
Show child attributes
[​](http://docs.vogent.ai/api-reference/get-dial#response-inputs)
inputs
object
Show child attributes
[​](http://docs.vogent.ai/api-reference/get-dial#response-status)
status
string
[​](http://docs.vogent.ai/api-reference/get-dial#response-dial-task-id)
dialTaskId
string
[​](http://docs.vogent.ai/api-reference/get-dial#response-from-number-id)
fromNumberId
string
[​](http://docs.vogent.ai/api-reference/get-dial#response-started-at)
startedAt
string<date-time>
[​](http://docs.vogent.ai/api-reference/get-dial#response-ended-at)
endedAt
string<date-time>
[​](http://docs.vogent.ai/api-reference/get-dial#response-created-at)
createdAt
string<date-time>
[​](http://docs.vogent.ai/api-reference/get-dial#response-updated-at)
updatedAt
string<date-time>
[​](http://docs.vogent.ai/api-reference/get-dial#response-system-result-type-one-of-0)
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
[​](http://docs.vogent.ai/api-reference/get-dial#response-voice-id)
voiceId
string
[​](http://docs.vogent.ai/api-reference/get-dial#response-versioned-prompt-id)
versionedPromptId
string
[Hangup Dial.](http://docs.vogent.ai/api-reference/hangup-dial)[Get Dial Token](http://docs.vogent.ai/api-reference/get-dial-token)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
