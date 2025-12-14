Webhooks

Inbound Dial



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

                                  



  * [Event Type](#event-type)
  * [Payload](#payload)
  * [Example Message](#example-message)
  * [Example Response (with inbound webhook response)](#example-response-with-inbound-webhook-response)



Webhooks

# Inbound Dial

This webhook is triggered when an inbound dial is made to a phone number linked to an agent. Elto will automatically run the agent after this webhook is triggered. If the agent is configured with the inbound webhook response option, you may return a JSON object to fill in any parameters in the agent’s prompt with the following typescript schema:

Copy

```
`{ call_agent_input: { [key: string]: string; }; keywords: string[]; } `
```

However, in this case you’ll only have 3 seconds to respond before the call proceeds without the parameters filled in.

## 

[​](#event-type)

Event Type

`dial.inbound`

## 

[​](#payload)

Payload

Name| Type| Description  
---|---|---  
`dial_session_id`| string| The ID of the dial session.  
`dial_id`| string| The ID of the inbound dial.  
`dest_number_id`| string| The Elto ID of the called phone number.  
`call_agent_id`| string| The associated agent that was triggered by the call.  
`source_number`| string| The E.164 formatted phone number that is making the call.  
  
## 

[​](#example-message)

Example Message

Copy

```
`{ "event": "dial.inbound", "payload": { "dial_session_id": "de3ee23e-ce58-4e05-9e7b-fcb96ba440a6", "dial_id": "5a6c6190-db20-4d8e-86a9-79a6af292dea", "dest_number_id": "2310e824-a2cb-4b0c-88cf-8f8b745bf6ae", "call_agent_id": "32e4be84-0803-4c41-af70-5a87a2dc0a4e", "source_number": "+18001234567" } } `
```

## 

[​](#example-response-with-inbound-webhook-response)

Example Response (with inbound webhook response)

Copy

```
`{ "call_agent_input": { "name": "John Doe" }, "keywords": ["John", "Doe"] } `
```

[Create Dial](/developers/webhooks/create-dial)[Dial Status Updated](/developers/webhooks/dial-status-updated)