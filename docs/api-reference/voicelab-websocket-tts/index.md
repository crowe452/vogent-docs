[Skip to main content](https://docs.vogent.ai/api-reference/voicelab-websocket-tts#content-area)
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
Websocket TTS
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
[Run Multispeaker TTS Model](https://docs.vogent.ai/api-reference/run-multispeaker-tts-model)[List Batch Jobs](https://docs.vogent.ai/api-reference/list-batch-dial-jobs)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
