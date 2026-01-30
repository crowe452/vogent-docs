[Skip to main content](https://docs.vogent.ai/developers/webhooks/function-call#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Webhooks
Function Call
[Guides](https://docs.vogent.ai/introduction)[API Reference](https://docs.vogent.ai/api-reference/introduction)[SDK](https://docs.vogent.ai/sdk/web-sdk)[Voicelab](https://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](https://docs.vogent.ai/introduction)
  * Quickstart


##### Platform Overview
  * [Introduction](https://docs.vogent.ai/platform-overview/introduction)
  * Agents
  * Voices
  * Tools
  * [Live Dials](https://docs.vogent.ai/platform-overview/live-dials)
  * [Batch Dial Jobs](https://docs.vogent.ai/platform-overview/batch-dial-jobs)
  * [API Settings](https://docs.vogent.ai/platform-overview/api-settings)
  * [Team](https://docs.vogent.ai/platform-overview/team)
  * [Billing](https://docs.vogent.ai/platform-overview/billing)
  * [Prompting Guide](https://docs.vogent.ai/platform-overview/prompting-guide)


##### Phone Numbers
  * [Overview](https://docs.vogent.ai/telephony/overview)
  * Importing via SIP
  * [Using a SIP Domain](https://docs.vogent.ai/telephony/sip-domain/overview)


##### Self Learning
  * [Self Learning Overview](https://docs.vogent.ai/platform-overview/self-learning/overview)
  * [Auto-Create Agents](https://docs.vogent.ai/platform-overview/self-learning/create)
  * [Optimize Agents](https://docs.vogent.ai/platform-overview/self-learning/optimize)


##### For Developers
  * Webhooks
    * [Create Dial](https://docs.vogent.ai/developers/webhooks/create-dial)
    * [Inbound Dial](https://docs.vogent.ai/developers/webhooks/dial-inbound)
    * [Dial Status Updated](https://docs.vogent.ai/developers/webhooks/dial-status-updated)
    * [Dial Recording Complete](https://docs.vogent.ai/developers/webhooks/dial-recording)
    * [Dial Extractor Complete](https://docs.vogent.ai/developers/webhooks/dial-extractor)
    * [Dial Transcript Finalized](https://docs.vogent.ai/developers/webhooks/dial-transcript)
    * [Function Call](https://docs.vogent.ai/developers/webhooks/function-call)
  * [Dials and Dial Sessions](https://docs.vogent.ai/developers/dials-dialsessions)
  * [Dials Statuses](https://docs.vogent.ai/developers/dial-statuses)
  * [Flow Builder Schemas](https://docs.vogent.ai/developers/schemas)


On this page
  * [Payload](https://docs.vogent.ai/developers/webhooks/function-call#payload)
  * [Example Message](https://docs.vogent.ai/developers/webhooks/function-call#example-message)


Webhooks
# Function Call
This webhook is triggered when an agent makes a function call.
## 
[​](https://docs.vogent.ai/developers/webhooks/function-call#payload)
Payload
Name| Type| Description  
---|---|---  
`dial_id`| string| The ID of the dial this function call is associated with.  
`params`| object| Object containing the function call parameters.  
`dial`| Dial| The dial that triggered the function call.  
## 
[​](https://docs.vogent.ai/developers/webhooks/function-call#example-message)
Example Message
Copy
```
{
  "dial_id": "f47ac10b-58cc-4372-a567-0e02b2c3d479",
  "dial": {
    ...
  },
  "params": {
    "name": "John Doe"
   }
}

```

[Dial Transcript Finalized](https://docs.vogent.ai/developers/webhooks/dial-transcript)[Dials and Dial Sessions](https://docs.vogent.ai/developers/dials-dialsessions)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
