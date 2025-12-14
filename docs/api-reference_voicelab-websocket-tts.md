Voicelab

Websocket TTS



  



        



        



    



        



        



              



        



  



      



              


Messages

Websocket Input

```
`{ "generationId": "<string>", "contextId": "<string>", "items": "<string>", "description": "<string>", "voiceId": "<string>", "text": "<string>", "finalText": true, "cancel": true, "sampleRate": 123, "addWordTimestamps": true}`
```

Finished Message

```
`{ "type": "<string>", "generationId": "<string>"}`
```

Error Message

```
`{ "type": "<string>", "generationId": "<string>", "error": "<string>"}`
```

Chunk Message

```
`{ "type": "<string>", "generationId": "<string>", "audio": "<string>"}`
```

Timestamp Message

```
`No examples found`
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
`{ "generationId": "<string>", "contextId": "<string>", "items": "<string>", "description": "<string>", "voiceId": "<string>", "text": "<string>", "finalText": true, "cancel": true, "sampleRate": 123, "addWordTimestamps": true}`
```

Finished Message

```
`{ "type": "<string>", "generationId": "<string>"}`
```

Error Message

```
`{ "type": "<string>", "generationId": "<string>", "error": "<string>"}`
```

Chunk Message

```
`{ "type": "<string>", "generationId": "<string>", "audio": "<string>"}`
```

Timestamp Message

```
`No examples found`
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

[Run Multispeaker TTS Model](/api-reference/run-multispeaker-tts-model)[List Batch Jobs](/api-reference/list-batch-dial-jobs)