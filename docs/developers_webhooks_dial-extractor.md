Webhooks

Dial Extractor Complete



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

# Dial Extractor Complete

This webhook is triggered when the extractor finishes running after a dial.

## 

[​](#event-type)

Event Type

`dial.extractor`

## 

[​](#payload)

Payload

Name| Type| Description  
---|---|---  
`dial_id`| string| The ID of the dial.  
`ai_result`| object| The extractor result.  
  
## 

[​](#example-message)

Example Message

Copy

```
`{ "event": "dial.extractor", "payload": { "ai_result": { "summary": "This call was successful in getting the information." }, "dial_id": "5a6c6190-db20-4d8e-86a9-79a6af292dea" } } `
```

[Dial Recording Complete](/developers/webhooks/dial-recording)[Dial Transcript Finalized](/developers/webhooks/dial-transcript)