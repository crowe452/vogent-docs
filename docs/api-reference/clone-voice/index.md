[Skip to main content](https://docs.vogent.ai/api-reference/clone-voice#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Voices
Clone Voice
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


Clone Voice
cURL
Copy
```
curl --request POST \
 --url https://api.vogent.ai/api/voices/clone \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: multipart/form-data' \
 --form 'name=<string>' \
 --form clip='@example-file' \
 --form model=CARTESIA \
 --form 'transcription=<string>'
```

200
Copy
```
{
 "id": "<string>",
 "name": "<string>",
 "voiceType": "<string>",
 "voiceTier": "STANDARD",
 "description": "<string>"
}
```

Voices
# Clone Voice
Clones a new voice for the workspace.
POST
/
voices
/
clone
Try it
Clone Voice
cURL
Copy
```
curl --request POST \
 --url https://api.vogent.ai/api/voices/clone \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: multipart/form-data' \
 --form 'name=<string>' \
 --form clip='@example-file' \
 --form model=CARTESIA \
 --form 'transcription=<string>'
```

200
Copy
```
{
 "id": "<string>",
 "name": "<string>",
 "voiceType": "<string>",
 "voiceTier": "STANDARD",
 "description": "<string>"
}
```

#### Authorizations
[​](https://docs.vogent.ai/api-reference/clone-voice#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Body
multipart/form-data
[​](https://docs.vogent.ai/api-reference/clone-voice#body-name)
name
string
required
The name of the cloned voice.
[​](https://docs.vogent.ai/api-reference/clone-voice#body-clip)
clip
file
required
The audio clip to use for cloning.
[​](https://docs.vogent.ai/api-reference/clone-voice#body-model)
model
enum<string>
required
Available options: 
`CARTESIA`, 
`CSM`
[​](https://docs.vogent.ai/api-reference/clone-voice#body-transcription)
transcription
string
Optional transcription of the audio clip.
#### Response
200
application/json
Successful operation
[​](https://docs.vogent.ai/api-reference/clone-voice#response-id)
id
string
required
[​](https://docs.vogent.ai/api-reference/clone-voice#response-name)
name
string
required
[​](https://docs.vogent.ai/api-reference/clone-voice#response-voice-type)
voiceType
string
required
[​](https://docs.vogent.ai/api-reference/clone-voice#response-voice-tier)
voiceTier
enum<string>
required
Available options: 
`STANDARD`, 
`PREMIUM`
[​](https://docs.vogent.ai/api-reference/clone-voice#response-description)
description
string
required
[Delete Agent](https://docs.vogent.ai/api-reference/delete-agent)[List Voices](https://docs.vogent.ai/api-reference/list-voices)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
