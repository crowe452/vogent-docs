Webhooks

Dial Recording Complete



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

# Dial Recording Complete

This webhook is triggered when a recording is attached to a dial.

## 

[​](#event-type)

Event Type

`dial.recording_created`

## 

[​](#payload)

Payload

Name| Type| Description  
---|---|---  
`dial_id`| string| The ID of the dial.  
`recording_url`| string| The URL to the recording.  
  
## 

[​](#example-message)

Example Message

Copy

```
`{ "event": "dial.recording_created", "payload": { "recording_url": "https://api.getelto.com/api/recordings/de3ee23e-ce58-4e05-9e7b-fcb96ba440a6", "dial_id": "5a6c6190-db20-4d8e-86a9-79a6af292dea" } } `
```

[Dial Status Updated](/developers/webhooks/dial-status-updated)[Dial Extractor Complete](/developers/webhooks/dial-extractor)