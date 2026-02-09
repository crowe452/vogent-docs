[Skip to main content](http://docs.vogent.ai/api-reference/update-extractor#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Extractors
Update extractor
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


Update extractor
cURL
Copy
```
curl --request PUT \
 --url https://api.vogent.ai/api/agents/{agentId}/extractors/{extractorId} \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: application/json' \
 --data '
{
 "name": "<string>",
 "extractorFieldsJsonSchema": "<string>"
}
'
```

200
Copy
```
{
 "id": "<string>",
 "name": "<string>",
 "extractorFieldsJsonSchema": "<string>"
}
```

Extractors
# Update extractor
Update an extractor for a given agent.
PUT
/
agents
/
{agentId}
/
extractors
/
{extractorId}
Try it
Update extractor
cURL
Copy
```
curl --request PUT \
 --url https://api.vogent.ai/api/agents/{agentId}/extractors/{extractorId} \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: application/json' \
 --data '
{
 "name": "<string>",
 "extractorFieldsJsonSchema": "<string>"
}
'
```

200
Copy
```
{
 "id": "<string>",
 "name": "<string>",
 "extractorFieldsJsonSchema": "<string>"
}
```

#### Authorizations
[​](http://docs.vogent.ai/api-reference/update-extractor#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Path Parameters
[​](http://docs.vogent.ai/api-reference/update-extractor#parameter-agent-id)
agentId
string
required
ID of the agent.
[​](http://docs.vogent.ai/api-reference/update-extractor#parameter-extractor-id)
extractorId
string
required
ID of the extractor.
#### Body
application/json
Update an extractor
[​](http://docs.vogent.ai/api-reference/update-extractor#body-name)
name
string
[​](http://docs.vogent.ai/api-reference/update-extractor#body-extractor-fields-json-schema)
extractorFieldsJsonSchema
string
#### Response
200
application/json
Successful operation
[​](http://docs.vogent.ai/api-reference/update-extractor#response-id)
id
string
required
[​](http://docs.vogent.ai/api-reference/update-extractor#response-name)
name
string
required
[​](http://docs.vogent.ai/api-reference/update-extractor#response-extractor-fields-json-schema)
extractorFieldsJsonSchema
string
required
[Create extractor](http://docs.vogent.ai/api-reference/create-extractor)[List phone numbers](http://docs.vogent.ai/api-reference/list-phone-numbers)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
