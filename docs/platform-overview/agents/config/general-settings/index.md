[Skip to main content](https://docs.vogent.ai/platform-overview/agents/config/general-settings#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Configuration
General Settings
[Guides](https://docs.vogent.ai/introduction)[API Reference](https://docs.vogent.ai/api-reference/introduction)[SDK](https://docs.vogent.ai/sdk/web-sdk)[Voicelab](https://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](https://docs.vogent.ai/introduction)
  * Quickstart


##### Platform Overview
  * [Introduction](https://docs.vogent.ai/platform-overview/introduction)
  * Agents
    * [Overview](https://docs.vogent.ai/platform-overview/agents/overview)
    * Configuration
      * [Overview](https://docs.vogent.ai/platform-overview/agents/config/overview)
      * [General Settings](https://docs.vogent.ai/platform-overview/agents/config/general-settings)
      * [Voice Settings](https://docs.vogent.ai/platform-overview/agents/config/voice-settings)
      * [Linked Numbers](https://docs.vogent.ai/platform-overview/agents/config/linked-numbers)
      * [IVR Settings](https://docs.vogent.ai/platform-overview/agents/config/ivr-settings)
    * Model
    * Post-Call Analysis
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
  * [Dials and Dial Sessions](https://docs.vogent.ai/developers/dials-dialsessions)
  * [Dials Statuses](https://docs.vogent.ai/developers/dial-statuses)
  * [Flow Builder Schemas](https://docs.vogent.ai/developers/schemas)


On this page
  * [Opening Line](https://docs.vogent.ai/platform-overview/agents/config/general-settings#opening-line)
  * [Call Transfers](https://docs.vogent.ai/platform-overview/agents/config/general-settings#call-transfers)
  * [Background Noise](https://docs.vogent.ai/platform-overview/agents/config/general-settings#background-noise)
  * [Utterance Detector Sensitivity](https://docs.vogent.ai/platform-overview/agents/config/general-settings#utterance-detector-sensitivity)
  * [Inbound Webhook Responses](https://docs.vogent.ai/platform-overview/agents/config/general-settings#inbound-webhook-responses)


Configuration
# General Settings
Configure Basic Behavior of Your Voice Agent
General settings control the fundamental behavior of your voice agent during calls, from how it initiates conversations to how it handles interruptions.
## 
[​](https://docs.vogent.ai/platform-overview/agents/config/general-settings#opening-line)
Opening Line
Configure what your agent says when first connecting to a call. This feature can be set differently for:
  * Inbound calls
  * Outbound calls
  * Both call types


If you want your agent to wait for the user to speak first, you can disable this feature entirely. This can be useful for scenarios where the caller should initiate the conversation.
## 
[​](https://docs.vogent.ai/platform-overview/agents/config/general-settings#call-transfers)
Call Transfers
Enable your agent to transfer calls to specific phone numbers. When enabled, the agent can transfer calls by outputting a special `<|transfer|>` tag in their response.
Make sure your agent’s prompt includes logic for when and how to handle transfers appropriately.
## 
[​](https://docs.vogent.ai/platform-overview/agents/config/general-settings#background-noise)
Background Noise
Add ambient sound to make conversations feel more natural. Available options include:
  * Office
  * Other environmental sounds

This feature helps create a more realistic conversation environment and can make the interaction feel more authentic.
## 
[​](https://docs.vogent.ai/platform-overview/agents/config/general-settings#utterance-detector-sensitivity)
Utterance Detector Sensitivity
Control how quickly your agent recognizes and responds to user interruptions. Sensitivity levels:
  * Low
  * Medium (recommended)
  * High


Higher sensitivity means faster interruption detection but may result in more false positives. Medium provides a good balance for most use cases.
## 
[​](https://docs.vogent.ai/platform-overview/agents/config/general-settings#inbound-webhook-responses)
Inbound Webhook Responses
Enable dynamic prompt customization based on webhook responses for inbound calls. When enabled, you can:
  * Inject variables into your agent’s prompt
  * Customize responses based on caller data
  * Adapt agent behavior using external information


This feature requires proper webhook configuration and handling on your server to provide the necessary information during inbound calls.
[Overview](https://docs.vogent.ai/platform-overview/agents/config/overview)[Voice Settings](https://docs.vogent.ai/platform-overview/agents/config/voice-settings)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
