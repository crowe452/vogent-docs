Webhooks

Create Dial



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

# Create Dial

This webhook is triggered when a dial is created under a dial session.

## 

[​](#event-type)

Event Type

`dial.created`

## 

[​](#payload)

Payload

Name| Type| Description  
---|---|---  
`dial_session_id`| string| The ID of the dial session.  
`dial_id`| string| The ID of the created dial.  
  
## 

[​](#example-message)

Example Message

Copy

```
`{ "event": "dial.created", "payload": { "dial_session_id": "de3ee23e-ce58-4e05-9e7b-fcb96ba440a6", "dial_id": "5a6c6190-db20-4d8e-86a9-79a6af292dea" } } `
```

[Optimize Agents](/platform-overview/self-learning/optimize)[Inbound Dial](/developers/webhooks/dial-inbound)