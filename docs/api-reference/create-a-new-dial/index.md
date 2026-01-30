[Skip to main content](https://docs.vogent.ai/api-reference/create-a-new-dial#content-area)
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
Create a new dial
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


Create a new dial
cURL
Copy
```
curl --request POST \
 --url https://api.vogent.ai/api/dials \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: application/json' \
 --data '
{
 "callAgentId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "webhookUrl": "https://test.com/webhook",
 "browserCall": false,
 "toNumber": "+11234567890",
 "fromNumberId": "1caec78c-4bba-477d-82cf-bcfce2b73856",
 "fromNumberPoolId": "1caec78c-4bba-477d-82cf-bcfce2b73856",
 "aiVoiceId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "voiceOptionValues": [
  {
   "optionId": "<string>",
   "value": "<string>"
  }
 ],
 "voiceVolumeLevel": -100,
 "versionedModelId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "ivrVersionedPromptId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "overrideTranscriberFinalDurationMs": 500,
 "timeoutMinutes": 10,
 "callAgentExtractorId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "callAgentInput": {},
 "agentOverrides": {
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
  "inboundWebhookResponse": true,
  "inboundWebhookUrl": "<string>",
  "maxDurationSeconds": 123,
  "openingLine": {
   "lineType": "INBOUND_ONLY",
   "content": "<string>"
  },
  "voiceVolumeLevel": 123,
  "backgroundNoiseType": "noise",
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
   "versionedPrompt": {
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
   "aiVoiceId": "<string>",
   "taggingText": "<string>"
  },
  "language": "<string>",
  "fillEmptyStringVariables": true,
  "silenceHangupConfiguration": {
   "type": "DISABLED",
   "silenceDurationSeconds": 123
  }
 },
 "keywords": [
  "<string>"
 ],
 "advancedBrowserInteraction": true
}
'
```

200
Copy
```
{
 "dialToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZXN0IjoidGVzdCJ9.9EQaLsDRKDVXLUVLR9JgDTjEULaT2-OMbHayQAzgZH8",
 "sessionId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "dialId": "57555c5e-5a56-49ca-8fe8-24946d2fbc3e"
}
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
curl --request POST \
 --url https://api.vogent.ai/api/dials \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: application/json' \
 --data '
{
 "callAgentId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "webhookUrl": "https://test.com/webhook",
 "browserCall": false,
 "toNumber": "+11234567890",
 "fromNumberId": "1caec78c-4bba-477d-82cf-bcfce2b73856",
 "fromNumberPoolId": "1caec78c-4bba-477d-82cf-bcfce2b73856",
 "aiVoiceId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "voiceOptionValues": [
  {
   "optionId": "<string>",
   "value": "<string>"
  }
 ],
 "voiceVolumeLevel": -100,
 "versionedModelId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "ivrVersionedPromptId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "overrideTranscriberFinalDurationMs": 500,
 "timeoutMinutes": 10,
 "callAgentExtractorId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "callAgentInput": {},
 "agentOverrides": {
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
  "inboundWebhookResponse": true,
  "inboundWebhookUrl": "<string>",
  "maxDurationSeconds": 123,
  "openingLine": {
   "lineType": "INBOUND_ONLY",
   "content": "<string>"
  },
  "voiceVolumeLevel": 123,
  "backgroundNoiseType": "noise",
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
   "versionedPrompt": {
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
   "aiVoiceId": "<string>",
   "taggingText": "<string>"
  },
  "language": "<string>",
  "fillEmptyStringVariables": true,
  "silenceHangupConfiguration": {
   "type": "DISABLED",
   "silenceDurationSeconds": 123
  }
 },
 "keywords": [
  "<string>"
 ],
 "advancedBrowserInteraction": true
}
'
```

200
Copy
```
{
 "dialToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZXN0IjoidGVzdCJ9.9EQaLsDRKDVXLUVLR9JgDTjEULaT2-OMbHayQAzgZH8",
 "sessionId": "61ccefdf-ea02-4f49-811b-1241f8e20d26",
 "dialId": "57555c5e-5a56-49ca-8fe8-24946d2fbc3e"
}
```

#### Authorizations
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Body
application/json
Create a new dial
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-call-agent-id)
callAgentId
string
required
Required. The ID of the agent.
Example:
`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-webhook-url-one-of-0)
webhookUrl
string | null
Optional. The URL for the webhook for this dial session.
Example:
`"https://test.com/webhook"`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-browser-call-one-of-0)
browserCall
boolean | null
Set to true if this is a browser call.
Example:
`false`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-to-number-one-of-0)
toNumber
string | null
Required if this is a phone dial, in E.164 format.
Example:
`"+11234567890"`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-from-number-id-one-of-0)
fromNumberId
string | null
The ID for the phone number to use to start the call. Required if this is a phone dial.
Example:
`"1caec78c-4bba-477d-82cf-bcfce2b73856"`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-from-number-pool-id-one-of-0)
fromNumberPoolId
string | null
The ID of a phone number pool to use when starting the call.
Example:
`"1caec78c-4bba-477d-82cf-bcfce2b73856"`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-ai-voice-id-one-of-0)
aiVoiceId
string | null
The ID for the voice on the call. If not specified, the default voice for the agent will be used.
Example:
`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-voice-option-values)
voiceOptionValues
object[]
An optional configuration for the voice being used.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-voice-volume-level)
voiceVolumeLevel
integer
The volume level for the voice on the call, from -300 (quiet) to 300 (loud).
Example:
`-100`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-versioned-model-id)
versionedModelId
string
The prompt/model version to use for this call, if not specified, the default on the agent is used.
Example:
`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-ivr-versioned-prompt-id)
ivrVersionedPromptId
string
The prompt/model version to use for the IVR portion of this call, if ivr nav is enabled on the agent.
Example:
`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-override-transcriber-final-duration-ms)
overrideTranscriberFinalDurationMs
integer
How long in ms after an utterance is complete to ignore the final/non-final status of the transcript and run inference.
Example:
`500`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-timeout-minutes)
timeoutMinutes
integer
The number of minutes before the call will be timed out. If not specified, there will be no limit on the calls, it's recommended to provide something here.
Example:
`10`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-call-agent-extractor-id)
callAgentExtractorId
string
The ID of the extractor to use for this call, if not specified, the default on the agent is used.
Example:
`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-call-agent-input-one-of-0)
callAgentInput
object
Any macros in the call agent prompt.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-agent-overrides-one-of-0)
agentOverrides
object
(Alpha) This feature is in Alpha testing, schemas may change slightly before GA. Please notify the Vogent team if there are any issues when using this field. Optional overrides for the call agent used for this dial.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-keywords-one-of-0)
keywords
string[] | null
A list of keywords to be used in the call.
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#body-advanced-browser-interaction)
advancedBrowserInteraction
boolean
If browserCall is false, and you want to have a more complex flow, allowing the web SDK to have transcribed barge-in lines, you should set this to true. Contact the vogent team to enable this feature.
#### Response
200
application/json
Successful operation
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#response-dial-token)
dialToken
string
required
You can pass this dial token to Elto's web UI, or use this token to authorize any requests for this dial. It's safe to pass this token to a client -- it only allows users to run requests against the dial associated with this session.
Example:
`"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0ZXN0IjoidGVzdCJ9.9EQaLsDRKDVXLUVLR9JgDTjEULaT2-OMbHayQAzgZH8"`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#response-session-id)
sessionId
string
required
Example:
`"61ccefdf-ea02-4f49-811b-1241f8e20d26"`
[​](https://docs.vogent.ai/api-reference/create-a-new-dial#response-dial-id)
dialId
string
required
Example:
`"57555c5e-5a56-49ca-8fe8-24946d2fbc3e"`
[Introduction](https://docs.vogent.ai/api-reference/introduction)[Hangup Dial.](https://docs.vogent.ai/api-reference/hangup-dial)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
