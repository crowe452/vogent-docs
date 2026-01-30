[Skip to main content](https://docs.vogent.ai/api-reference/run-multispeaker-tts-model#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Voicelab
Run Multispeaker TTS Model
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


Run Multispeaker TTS Model
cURL
Copy
```
curl --request POST \
 --url https://api.vogent.ai/api/tts/multispeaker \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: application/json' \
 --data '
{
 "lines": [
  {
   "text": "<string>",
   "voiceId": "<string>"
  }
 ],
 "voiceOptionValues": [
  {
   "optionId": "<string>",
   "value": "<string>"
  }
 ],
 "format": {
  "outputType": "WAV_PCM16",
  "sampleRate": 24000
 }
}
'
```

200
Copy
```
"<string>"
```

Voicelab
# Run Multispeaker TTS Model
Runs a multispeaker (conversational) text to speech model and generates audio. Bytes will be streamed to the client as they are generated.
POST
/
tts
/
multispeaker
Try it
Run Multispeaker TTS Model
cURL
Copy
```
curl --request POST \
 --url https://api.vogent.ai/api/tts/multispeaker \
 --header 'Authorization: Bearer <token>' \
 --header 'Content-Type: application/json' \
 --data '
{
 "lines": [
  {
   "text": "<string>",
   "voiceId": "<string>"
  }
 ],
 "voiceOptionValues": [
  {
   "optionId": "<string>",
   "value": "<string>"
  }
 ],
 "format": {
  "outputType": "WAV_PCM16",
  "sampleRate": 24000
 }
}
'
```

200
Copy
```
"<string>"
```

#### Authorizations
[​](https://docs.vogent.ai/api-reference/run-multispeaker-tts-model#authorization-authorization)
Authorization
string
header
required
In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.
#### Body
application/json
[​](https://docs.vogent.ai/api-reference/run-multispeaker-tts-model#body-lines)
lines
object[]
required
The lines that need to be generated.
Show child attributes
[​](https://docs.vogent.ai/api-reference/run-multispeaker-tts-model#body-voice-option-values)
voiceOptionValues
object[]
An optional configuration for the voices being used.
Show child attributes
[​](https://docs.vogent.ai/api-reference/run-multispeaker-tts-model#body-format)
format
object
The output format for the generated audio. Defaults to WAV_PCM16 at 24000 Hz.
Show child attributes
#### Response
200
application/octet-stream
Returns a file with the audio.
The response is of type `file`.
[Run TTS Model](https://docs.vogent.ai/api-reference/run-tts-model)[Websocket TTS](https://docs.vogent.ai/api-reference/voicelab-websocket-tts)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
