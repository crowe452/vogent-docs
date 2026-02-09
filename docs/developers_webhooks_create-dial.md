[Skip to main content](http://docs.vogent.ai/developers/webhooks/create-dial#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Webhooks
Create Dial
[Guides](http://docs.vogent.ai/introduction)[API Reference](http://docs.vogent.ai/api-reference/introduction)[SDK](http://docs.vogent.ai/sdk/web-sdk)[Voicelab](http://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](http://docs.vogent.ai/introduction)
  * Quickstart


##### Platform Overview
  * [Introduction](http://docs.vogent.ai/platform-overview/introduction)
  * Agents
  * Voices
  * Tools
  * [Live Dials](http://docs.vogent.ai/platform-overview/live-dials)
  * [Batch Dial Jobs](http://docs.vogent.ai/platform-overview/batch-dial-jobs)
  * [API Settings](http://docs.vogent.ai/platform-overview/api-settings)
  * [Team](http://docs.vogent.ai/platform-overview/team)
  * [Billing](http://docs.vogent.ai/platform-overview/billing)
  * [Prompting Guide](http://docs.vogent.ai/platform-overview/prompting-guide)


##### Phone Numbers
  * [Overview](http://docs.vogent.ai/telephony/overview)
  * Importing via SIP
  * [Using a SIP Domain](http://docs.vogent.ai/telephony/sip-domain/overview)


##### Self Learning
  * [Self Learning Overview](http://docs.vogent.ai/platform-overview/self-learning/overview)
  * [Auto-Create Agents](http://docs.vogent.ai/platform-overview/self-learning/create)
  * [Optimize Agents](http://docs.vogent.ai/platform-overview/self-learning/optimize)


##### For Developers
  * Webhooks
    * [Create Dial](http://docs.vogent.ai/developers/webhooks/create-dial)
    * [Inbound Dial](http://docs.vogent.ai/developers/webhooks/dial-inbound)
    * [Dial Status Updated](http://docs.vogent.ai/developers/webhooks/dial-status-updated)
    * [Dial Recording Complete](http://docs.vogent.ai/developers/webhooks/dial-recording)
    * [Dial Extractor Complete](http://docs.vogent.ai/developers/webhooks/dial-extractor)
    * [Dial Transcript Finalized](http://docs.vogent.ai/developers/webhooks/dial-transcript)
    * [Function Call](http://docs.vogent.ai/developers/webhooks/function-call)
  * [Dials and Dial Sessions](http://docs.vogent.ai/developers/dials-dialsessions)
  * [Dials Statuses](http://docs.vogent.ai/developers/dial-statuses)
  * [Flow Builder Schemas](http://docs.vogent.ai/developers/schemas)


On this page
  * [Event Type](http://docs.vogent.ai/developers/webhooks/create-dial#event-type)
  * [Payload](http://docs.vogent.ai/developers/webhooks/create-dial#payload)
  * [Example Message](http://docs.vogent.ai/developers/webhooks/create-dial#example-message)


Webhooks
# Create Dial
This webhook is triggered when a dial is created under a dial session.
## 
[​](http://docs.vogent.ai/developers/webhooks/create-dial#event-type)
Event Type
`dial.created`
## 
[​](http://docs.vogent.ai/developers/webhooks/create-dial#payload)
Payload
Name| Type| Description  
---|---|---  
`dial_session_id`| string| The ID of the dial session.  
`dial_id`| string| The ID of the created dial.  
## 
[​](http://docs.vogent.ai/developers/webhooks/create-dial#example-message)
Example Message
Copy
```
{
  "event": "dial.created",
  "payload": {
    "dial_session_id": "de3ee23e-ce58-4e05-9e7b-fcb96ba440a6",
    "dial_id": "5a6c6190-db20-4d8e-86a9-79a6af292dea"
  }
}

```

[Optimize Agents](http://docs.vogent.ai/platform-overview/self-learning/optimize)[Inbound Dial](http://docs.vogent.ai/developers/webhooks/dial-inbound)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
