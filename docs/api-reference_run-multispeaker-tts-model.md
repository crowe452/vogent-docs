Voicelab

Run Multispeaker TTS Model



  



        



        



    



        



        



              



        



  



      



              


Run Multispeaker TTS Model

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/tts/multispeaker \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "lines": [ { "text": "<string>", "voiceId": "<string>" } ], "voiceOptionValues": [ { "optionId": "<string>", "value": "<string>" } ], "format": { "outputType": "WAV_PCM16", "sampleRate": 24000 } } '`
```

200

400

422

Copy

```
`"<string>"`
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
`curl --request POST \ --url https://api.vogent.ai/api/tts/multispeaker \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "lines": [ { "text": "<string>", "voiceId": "<string>" } ], "voiceOptionValues": [ { "optionId": "<string>", "value": "<string>" } ], "format": { "outputType": "WAV_PCM16", "sampleRate": 24000 } } '`
```

200

400

422

Copy

```
`"<string>"`
```

#### Authorizations

[​](#authorization-authorization)

Authorization

string

header

required

In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.

#### Body

application/json

[​](#body-lines)

lines

object[]

required

The lines that need to be generated.

Show child attributes

[​](#body-lines-items-text)

lines.text

string

required

The text to generate.

[​](#body-lines-items-voice-id)

lines.voiceId

string

required

The voice ID to use to generate the text.

[​](#body-voice-option-values)

voiceOptionValues

object[]

An optional configuration for the voices being used.

Show child attributes

[​](#body-voice-option-values-items-option-id)

voiceOptionValues.optionId

string

required

The ID of option.

[​](#body-voice-option-values-items-value)

voiceOptionValues.value

string

required

[​](#body-format)

format

object

The output format for the generated audio. Defaults to WAV_PCM16 at 24000 Hz.

Show child attributes

[​](#body-format-output-type)

format.outputType

enum<string>

required

The type of output format.

Available options: 

`RAW_PCM16`, 

`WAV_PCM16`, 

`MP3`

[​](#body-format-sample-rate)

format.sampleRate

integer

required

The sample rate for the audio output. Must be one of 8000, 16000, 22050, 24000, 41500, or 48000

#### Response

200

application/octet-stream

Returns a file with the audio.

The response is of type `file`.

[Run TTS Model](/api-reference/run-tts-model)[Websocket TTS](/api-reference/voicelab-websocket-tts)