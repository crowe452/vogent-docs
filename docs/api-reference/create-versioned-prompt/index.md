[Skip to main content](https://docs.vogent.ai/api-reference/create-versioned-prompt#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Versioned Prompts
Create versioned prompt
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


Create versioned prompt
cURL
Copy
```
curl --request POST \
 --url https://api.vogent.ai/api/agents/{agentId}/versioned_prompts \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: application/json' \
 --data '
{
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
}
'
```

200
Copy
```
{
 "id": "<string>",
 "name": "<string>",
 "agentType": "STANDARD",
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
    "nodeData": {},
    "outputSchema": "<string>"
   }
  ],
  "globalContext": "<string>",
  "aiOpen": true,
  "openingLineType": "INBOUND_ONLY"
 },
 "aiModelId": "<string>",
 "modelOptionValues": [
  {
   "optionId": "<string>",
   "value": "<string>"
  }
 ]
}
```

Versioned Prompts
# Create versioned prompt
Creates a versioned prompt for a given agent.
POST
/
agents
/
{agentId}
/
versioned_prompts
Try it
Create versioned prompt
cURL
Copy
```
curl --request POST \
 --url https://api.vogent.ai/api/agents/{agentId}/versioned_prompts \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: application/json' \
 --data '
{
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
}
'
```

200
Copy
```
{
 "id": "<string>",
 "name": "<string>",
 "agentType": "STANDARD",
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
    "nodeData": {},
    "outputSchema": "<string>"
   }
  ],
  "globalContext": "<string>",
  "aiOpen": true,
  "openingLineType": "INBOUND_ONLY"
 },
 "aiModelId": "<string>",
 "modelOptionValues": [
  {
   "optionId": "<string>",
   "value": "<string>"
  }
 ]
}
```

#### Authorizations
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Path Parameters
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#parameter-agent-id)
agentId
string
required
ID of the agent.
#### Body
application/json
Creates a versioned prompt
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#body-ai-model-id)
aiModelId
string
required
The ID of the model to use.
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#body-agent-type)
agentType
enum<string>
required
The type of agent that this prompt represents.
Available options: 
`STANDARD`, 
`CUSTOM_FLOW`
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#body-name)
name
string
required
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#body-prompt-one-of-0)
prompt
string | null
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#body-flow-definition)
flowDefinition
object
For agents with agentType CUSTOM_FLOW, the flow definition that you want to use.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#body-model-option-values)
modelOptionValues
object[]
Show child attributes
#### Response
200
application/json
Successful operation
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#response-id)
id
string
required
Unique identifier for the versioned prompt
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#response-name)
name
string
required
Human-readable name for the versioned prompt
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#response-agent-type)
agentType
enum<string>
required
The type of agent this prompt is designed for (STANDARD or CUSTOM_FLOW)
Available options: 
`STANDARD`, 
`CUSTOM_FLOW`
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#response-prompt-one-of-0)
prompt
string | null
required
The actual prompt content that will be used by the agent. Can be null for CUSTOM_FLOW agent types
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#response-flow-definition-one-of-0)
flowDefinition
object
The flow definition for the agent. Only defined for CUSTOM_FLOW agent types.
Show child attributes
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#response-ai-model-id)
aiModelId
string
The AI model ID to use for the agent.
[​](https://docs.vogent.ai/api-reference/create-versioned-prompt#response-model-option-values)
modelOptionValues
object[]
Show child attributes
[Update versioned prompt](https://docs.vogent.ai/api-reference/update-versioned-prompt)[Get extractor](https://docs.vogent.ai/api-reference/get-extractor)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
