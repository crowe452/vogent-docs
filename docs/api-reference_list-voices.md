Voices

List Voices



  



        



        



    



        



        



              



        



  



      



              


List Voices

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/voices \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "voices": [ { "id": "<string>", "name": "<string>", "voiceType": "<string>", "voiceTier": "STANDARD", "description": "<string>" } ], "cursor": "<string>" }`
```

Voices

# List Voices

Lists the AI voices available to the workspace.

GET

/

voices

Try it

List Voices

cURL

Copy

```
`curl --request GET \ --url https://api.vogent.ai/api/voices \ --header 'Authorization: Bearer <token>'`
```

200

400

422

Copy

```
`{ "voices": [ { "id": "<string>", "name": "<string>", "voiceType": "<string>", "voiceTier": "STANDARD", "description": "<string>" } ], "cursor": "<string>" }`
```

#### Authorizations

[​](#authorization-authorization)

Authorization

string

header

required

In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.

#### Query Parameters

[​](#parameter-name)

name

string

Filter voices by name.

[​](#parameter-voice-type)

voiceType

string

The provider (for third party voices), or model type (for Vogent hosted voices).

[​](#parameter-limit)

limit

integer

The maximum number of voices to return.

[​](#parameter-cursor)

cursor

string

The pagination cursor returned by the previous request. Feed the result provided by vogent verbatim.

#### Response

200

application/json

Successful operation

[​](#response-voices)

voices

object[]

required

Show child attributes

[​](#response-voices-items-id)

voices.id

string

required

[​](#response-voices-items-name)

voices.name

string

required

[​](#response-voices-items-voice-type)

voices.voiceType

string

required

[​](#response-voices-items-voice-tier)

voices.voiceTier

enum<string>

required

Available options: 

`STANDARD`, 

`PREMIUM`

[​](#response-voices-items-description)

voices.description

string

required

[​](#response-cursor-one-of-0)

cursor

string | null

required

A cursor you can pass to /voices to fetch the next page. If no next page exists, the cursor will be null.

[Clone Voice](/api-reference/clone-voice)[List versioned prompts](/api-reference/list-versioned-prompts)