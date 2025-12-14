Voices

Clone Voice



  



        



        



    



        



        



              



        



  



      



              


Clone Voice

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/voices/clone \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: multipart/form-data' \ --form 'name=<string>' \ --form clip='@example-file' \ --form model=CARTESIA \ --form 'transcription=<string>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "voiceType": "<string>", "voiceTier": "STANDARD", "description": "<string>" }`
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
`curl --request POST \ --url https://api.vogent.ai/api/voices/clone \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: multipart/form-data' \ --form 'name=<string>' \ --form clip='@example-file' \ --form model=CARTESIA \ --form 'transcription=<string>'`
```

200

400

422

Copy

```
`{ "id": "<string>", "name": "<string>", "voiceType": "<string>", "voiceTier": "STANDARD", "description": "<string>" }`
```

#### Authorizations

[​](#authorization-authorization)

Authorization

string

header

required

In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.

#### Body

multipart/form-data

[​](#body-name)

name

string

required

The name of the cloned voice.

[​](#body-clip)

clip

file

required

The audio clip to use for cloning.

[​](#body-model)

model

enum<string>

required

Available options: 

`CARTESIA`, 

`CSM`

[​](#body-transcription)

transcription

string

Optional transcription of the audio clip.

#### Response

200

application/json

Successful operation

[​](#response-id)

id

string

required

[​](#response-name)

name

string

required

[​](#response-voice-type)

voiceType

string

required

[​](#response-voice-tier)

voiceTier

enum<string>

required

Available options: 

`STANDARD`, 

`PREMIUM`

[​](#response-description)

description

string

required

[Delete Agent](/api-reference/delete-agent)[List Voices](/api-reference/list-voices)