Webhooks

Dial Transcript Finalized



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

                                  



  * [Event Type](#event-type)
  * [Payload](#payload)
  * [Example Message](#example-message)



Webhooks

# Dial Transcript Finalized

This webhook is triggered when a dial transcript is finalized.

## 

[​](#event-type)

Event Type

`dial.transcript`

## 

[​](#payload)

Payload

Name| Type| Description  
---|---|---  
`dial_id`| string| The ID of the created dial.  
`transcript`| `{text: string, speaker: ‘AI’ | ‘HUMAN’, detailType?: string}[]` | The finalized transcript.  
  
## 

[​](#example-message)

Example Message

Copy

```
`{ "event": "dial.transcript", "payload": { "dial_id": "5a6c6190-db20-4d8e-86a9-79a6af292dea", "transcript": [{ "text": "Hello?", "speaker": "HUMAN" }] } } `
```

[Dial Extractor Complete](/developers/webhooks/dial-extractor)[Function Call](/developers/webhooks/function-call)