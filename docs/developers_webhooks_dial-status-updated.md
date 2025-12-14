Webhooks

Dial Status Updated



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

# Dial Status Updated

This webhook is triggered when a dial status is updated.

## 

[​](#event-type)

Event Type

`dial.updated`

## 

[​](#payload)

Payload

Name| Type| Description  
---|---|---  
`dial_session_id`| string| The ID of the dial session.  
`dial_id`| string| The ID of the created dial.  
`status`| string| The new dial status  
  
## 

[​](#example-message)

Example Message

Copy

```
`{ "event": "dial.updated", "payload": { "dial_session_id": "de3ee23e-ce58-4e05-9e7b-fcb96ba440a6", "dial_id": "5a6c6190-db20-4d8e-86a9-79a6af292dea", "status": "completed" } } `
```

[Inbound Dial](/developers/webhooks/dial-inbound)[Dial Recording Complete](/developers/webhooks/dial-recording)