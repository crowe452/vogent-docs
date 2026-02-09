[Skip to main content](http://docs.vogent.ai/api-reference/list-queued-dials-for-batch-dial-job#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Batch Dials
List Queued Batch Dials
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


List Queued Batch Dials
cURL
Copy
```
curl --request GET \
 --url https://api.vogent.ai/api/batch_dial_jobs/{id}/queue \
 --header 'Authorization: Bearer <token>'
```

200
Copy
```
{
 "data": [
  {
   "id": "<string>",
   "toNumber": "<string>",
   "batchDialJobId": "<string>",
   "createdAt": "2023-11-07T05:31:56Z",
   "inputs": {}
  }
 ],
 "cursor": "<string>"
}
```

Batch Dials
# List Queued Batch Dials
Lists all rows that are queued as part of the batch job.
GET
/
batch_dial_jobs
/
{id}
/
queue
Try it
List Queued Batch Dials
cURL
Copy
```
curl --request GET \
 --url https://api.vogent.ai/api/batch_dial_jobs/{id}/queue \
 --header 'Authorization: Bearer <token>'
```

200
Copy
```
{
 "data": [
  {
   "id": "<string>",
   "toNumber": "<string>",
   "batchDialJobId": "<string>",
   "createdAt": "2023-11-07T05:31:56Z",
   "inputs": {}
  }
 ],
 "cursor": "<string>"
}
```

#### Authorizations
[​](http://docs.vogent.ai/api-reference/list-queued-dials-for-batch-dial-job#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Path Parameters
[​](http://docs.vogent.ai/api-reference/list-queued-dials-for-batch-dial-job#parameter-id)
id
string
required
ID of the batch dial job.
#### Query Parameters
[​](http://docs.vogent.ai/api-reference/list-queued-dials-for-batch-dial-job#parameter-limit)
limit
integer
The number of specs to return.
[​](http://docs.vogent.ai/api-reference/list-queued-dials-for-batch-dial-job#parameter-cursor)
cursor
string
The cursor for pagination.
#### Response
200
application/json
Successful operation
[​](http://docs.vogent.ai/api-reference/list-queued-dials-for-batch-dial-job#response-data)
data
object[]
required
Show child attributes
[​](http://docs.vogent.ai/api-reference/list-queued-dials-for-batch-dial-job#response-cursor-one-of-0)
cursor
string | null
required
[Update Batch Job](http://docs.vogent.ai/api-reference/update-batch-dial-job)[Pause/Resume Batch Job](http://docs.vogent.ai/api-reference/set-batch-dial-job-paused)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
