Webhooks

Function Call



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

                                  



  * [Payload](#payload)
  * [Example Message](#example-message)



Webhooks

# Function Call

This webhook is triggered when an agent makes a function call.

## 

[​](#payload)

Payload

Name| Type| Description  
---|---|---  
`dial_id`| string| The ID of the dial this function call is associated with.  
`params`| object| Object containing the function call parameters.  
`dial`| Dial| The dial that triggered the function call.  
  
## 

[​](#example-message)

Example Message

Copy

```
`{ "dial_id": "f47ac10b-58cc-4372-a567-0e02b2c3d479", "dial": { ... }, "params": { "name": "John Doe" } } `
```

[Dial Transcript Finalized](/developers/webhooks/dial-transcript)[Dials and Dial Sessions](/developers/dials-dialsessions)