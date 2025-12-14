Voicelab

Run TTS Model



  



        



        



    



        



        



              



        



  



      



              


Run TTS Model

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/tts \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "text": "<string>", "voiceId": "<string>", "voiceOptionValues": [ { "optionId": "<string>", "value": "<string>" } ], "format": { "outputType": "WAV_PCM16", "sampleRate": 24000 } } '`
```

200

400

422

Copy

```
`"<string>"`
```

Voicelab

# Run TTS Model

Runs a text to speech model and generates audio. Bytes will be streamed to the client as they are generated.

POST

/

tts

Try it

Run TTS Model

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/tts \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "text": "<string>", "voiceId": "<string>", "voiceOptionValues": [ { "optionId": "<string>", "value": "<string>" } ], "format": { "outputType": "WAV_PCM16", "sampleRate": 24000 } } '`
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

[​](#body-text)

text

string

required

The text to generate.

[​](#body-voice-id)

voiceId

string

required

The voice ID to use to generate the text.

[​](#body-voice-option-values)

voiceOptionValues

object[]

An optional configuration for the voice being used.

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

[List Models](/api-reference/list-models)[Run Multispeaker TTS Model](/api-reference/run-multispeaker-tts-model)