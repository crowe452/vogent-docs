[Skip to main content](https://docs.vogent.ai/api-reference/get-batch-dial-job#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Batch Dials
Get Batch Job
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


Get Batch Job
cURL
Copy
```
curl --request GET \
 --url https://api.vogent.ai/api/batch_dial_jobs/{id} \
 --header 'Authorization: Bearer <token>'
```

200
Copy
```
{
 "id": "<string>",
 "maxConcurrentDials": 123,
 "name": "<string>",
 "status": "INIT",
 "callAgentId": "<string>",
 "createdAt": "2023-11-07T05:31:56Z",
 "fromPhoneNumberIds": [
  "<string>"
 ],
 "schedule": {
  "days": [
   {
    "dayOfWeek": 123,
    "timeSlots": [
     {
      "startTime": "<string>",
      "endTime": "<string>"
     }
    ]
   }
  ],
  "timezone": "<string>"
 }
}
```

Batch Dials
# Get Batch Job
Get metadata for a batch dial job.
GET
/
batch_dial_jobs
/
{id}
Try it
Get Batch Job
cURL
Copy
```
curl --request GET \
 --url https://api.vogent.ai/api/batch_dial_jobs/{id} \
 --header 'Authorization: Bearer <token>'
```

200
Copy
```
{
 "id": "<string>",
 "maxConcurrentDials": 123,
 "name": "<string>",
 "status": "INIT",
 "callAgentId": "<string>",
 "createdAt": "2023-11-07T05:31:56Z",
 "fromPhoneNumberIds": [
  "<string>"
 ],
 "schedule": {
  "days": [
   {
    "dayOfWeek": 123,
    "timeSlots": [
     {
      "startTime": "<string>",
      "endTime": "<string>"
     }
    ]
   }
  ],
  "timezone": "<string>"
 }
}
```

#### Authorizations
[​](https://docs.vogent.ai/api-reference/get-batch-dial-job#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Path Parameters
[​](https://docs.vogent.ai/api-reference/get-batch-dial-job#parameter-id)
id
string
required
ID of the batch dial job.
#### Response
200
application/json
Successful operation
[​](https://docs.vogent.ai/api-reference/get-batch-dial-job#response-id)
id
string
required
[​](https://docs.vogent.ai/api-reference/get-batch-dial-job#response-max-concurrent-dials)
maxConcurrentDials
integer
required
[​](https://docs.vogent.ai/api-reference/get-batch-dial-job#response-name)
name
string
required
[​](https://docs.vogent.ai/api-reference/get-batch-dial-job#response-status)
status
enum<string>
required
Available options: 
`INIT`, 
`ACTIVE`, 
`PAUSED`, 
`COMPLETE`, 
`CANCELLED`
[​](https://docs.vogent.ai/api-reference/get-batch-dial-job#response-call-agent-id)
callAgentId
string
required
[​](https://docs.vogent.ai/api-reference/get-batch-dial-job#response-created-at)
createdAt
string<date-time>
required
[​](https://docs.vogent.ai/api-reference/get-batch-dial-job#response-from-phone-number-ids)
fromPhoneNumberIds
string[]
[​](https://docs.vogent.ai/api-reference/get-batch-dial-job#response-schedule-one-of-0)
schedule
object
Show child attributes
[Create Batch Job](https://docs.vogent.ai/api-reference/create-a-new-batch-dial-job)[Update Batch Job](https://docs.vogent.ai/api-reference/update-batch-dial-job)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
