[Skip to main content](https://docs.vogent.ai/api-reference/get-function#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Functions
Get function
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


Get function
cURL
Copy
```
curl --request GET \
 --url https://api.vogent.ai/api/functions/{id} \
 --header 'Authorization: Bearer <token>'
```

200
Copy
```
{
 "id": "<string>",
 "name": "<string>",
 "description": "<string>",
 "type": "transfer",
 "allowedNumbers": [
  {
   "number": "<string>"
  }
 ],
 "allowAnyNumber": true,
 "lifecycleMessages": {
  "started": [
   "<string>"
  ]
 }
}
```

Functions
# Get function
Gets a specific function.
GET
/
functions
/
{id}
Try it
Get function
cURL
Copy
```
curl --request GET \
 --url https://api.vogent.ai/api/functions/{id} \
 --header 'Authorization: Bearer <token>'
```

200
Copy
```
{
 "id": "<string>",
 "name": "<string>",
 "description": "<string>",
 "type": "transfer",
 "allowedNumbers": [
  {
   "number": "<string>"
  }
 ],
 "allowAnyNumber": true,
 "lifecycleMessages": {
  "started": [
   "<string>"
  ]
 }
}
```

#### Authorizations
[​](https://docs.vogent.ai/api-reference/get-function#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Path Parameters
[​](https://docs.vogent.ai/api-reference/get-function#parameter-id)
id
string
required
ID of the function.
#### Response
200
application/json
Successful operation
  * Transfer
  * API


[​](https://docs.vogent.ai/api-reference/get-function#response-one-of-0-id)
id
string
required
[​](https://docs.vogent.ai/api-reference/get-function#response-one-of-0-name)
name
string
required
The name of the function.
[​](https://docs.vogent.ai/api-reference/get-function#response-one-of-0-description)
description
string
required
A description of what the function does.
[​](https://docs.vogent.ai/api-reference/get-function#response-one-of-0-type)
type
enum<string>
required
Available options: 
`transfer`, 
`api`
[​](https://docs.vogent.ai/api-reference/get-function#response-one-of-0-allowed-numbers)
allowedNumbers
object[]
required
The numbers that the agent is allowed to transfer to.
Show child attributes
[​](https://docs.vogent.ai/api-reference/get-function#response-one-of-0-allow-any-number)
allowAnyNumber
boolean
required
Instead of using a fixed list of allowed numbers, allow the agent to transfer to any number (not recommended).
[​](https://docs.vogent.ai/api-reference/get-function#response-one-of-0-lifecycle-messages)
lifecycleMessages
object
Messages to display during function execution lifecycle events.
Show child attributes
[Create a function](https://docs.vogent.ai/api-reference/create-a-function)[Update function](https://docs.vogent.ai/api-reference/update-function)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
