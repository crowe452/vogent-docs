[Skip to main content](http://docs.vogent.ai/api-reference/voicelab-websocket-tts#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Voicelab
Websocket TTS
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


Messages
Websocket Input
```
{ "generationId": "<string>", "contextId": "<string>", "items": "<string>", "description": "<string>", "voiceId": "<string>", "text": "<string>", "finalText": true, "cancel": true, "sampleRate": 123, "addWordTimestamps": true}
```

Finished Message
```
{ "type": "<string>", "generationId": "<string>"}
```

Error Message
```
{ "type": "<string>", "generationId": "<string>", "error": "<string>"}
```

Chunk Message
```
{ "type": "<string>", "generationId": "<string>", "audio": "<string>"}
```

Timestamp Message
```
No examples found
```

Voicelab
# Websocket TTS
Real-time text-to-speech streaming over websockets. Send text incrementally and receive audio chunks as they are generated. To authenticate, you must include an `Authorization` header, with the value `Bearer {API_TOKEN}`. You can also include an `apiKey` query param with the value being your API key. Websockets can run multiple TTS streams concurrently. If you’re using the `contextId` feature, make sure all generations for the context are on the same websocket.
WSS
wss://api.vogent.ai/api/tts/websocket
Connect
Messages
Websocket Input
```
{ "generationId": "<string>", "contextId": "<string>", "items": "<string>", "description": "<string>", "voiceId": "<string>", "text": "<string>", "finalText": true, "cancel": true, "sampleRate": 123, "addWordTimestamps": true}
```

Finished Message
```
{ "type": "<string>", "generationId": "<string>"}
```

Error Message
```
{ "type": "<string>", "generationId": "<string>", "error": "<string>"}
```

Chunk Message
```
{ "type": "<string>", "generationId": "<string>", "audio": "<string>"}
```

Timestamp Message
```
No examples found
```

Send
Websocket Input
type:object
show 10 properties
Input message for text-to-speech generation
Receive
Finished Message
type:object
show 2 properties
Message sent when text-to-speech generation is complete
Error Message
type:object
show 3 properties
Message sent when text-to-speech generation encounters an error
Chunk Message
type:object
show 3 properties
Message sent with audio data chunks during text-to-speech generation
Timestamp Message
type:object
show 3 properties
Message sent with timestamps during text-to-speech generation, only when add word timestamps is true
[Run Multispeaker TTS Model](http://docs.vogent.ai/api-reference/run-multispeaker-tts-model)[List Batch Jobs](http://docs.vogent.ai/api-reference/list-batch-dial-jobs)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
