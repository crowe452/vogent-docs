[Skip to main content](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Configuration
IVR Settings
[Guides](http://docs.vogent.ai/introduction)[API Reference](http://docs.vogent.ai/api-reference/introduction)[SDK](http://docs.vogent.ai/sdk/web-sdk)[Voicelab](http://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](http://docs.vogent.ai/introduction)
  * Quickstart


##### Platform Overview
  * [Introduction](http://docs.vogent.ai/platform-overview/introduction)
  * Agents
    * [Overview](http://docs.vogent.ai/platform-overview/agents/overview)
    * Configuration
      * [Overview](http://docs.vogent.ai/platform-overview/agents/config/overview)
      * [General Settings](http://docs.vogent.ai/platform-overview/agents/config/general-settings)
      * [Voice Settings](http://docs.vogent.ai/platform-overview/agents/config/voice-settings)
      * [Linked Numbers](http://docs.vogent.ai/platform-overview/agents/config/linked-numbers)
      * [IVR Settings](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings)
    * Model
    * Post-Call Analysis
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
  * [Dials and Dial Sessions](http://docs.vogent.ai/developers/dials-dialsessions)
  * [Dials Statuses](http://docs.vogent.ai/developers/dial-statuses)
  * [Flow Builder Schemas](http://docs.vogent.ai/developers/schemas)


On this page
  * [IVR Detection](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings#ivr-detection)
  * [Voice Settings](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings#voice-settings)
  * [Model Selection](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings#model-selection)
  * [Tag Text](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings#tag-text)
  * [Best Practices](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings#best-practices)


Configuration
# IVR Settings
Configure How Your Agent Handles Automated Phone Menus
IVR (Interactive Voice Response) settings determine how your agent detects and navigates through automated phone menus. These settings are crucial for scenarios where your agent needs to interact with other phone systems.
## 
[​](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings#ivr-detection)
IVR Detection
Enable automatic detection of automated phone menus during calls. When enabled, the agent uses a specialized model to identify when it’s interacting with an IVR system.
While IVR detection may add a few milliseconds of latency to the call, it significantly improves the agent’s ability to navigate automated systems successfully.
## 
[​](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings#voice-settings)
Voice Settings
Choose a specific voice for IVR interactions that prioritizes clarity and recognition by automated systems. Options include:
  * Use Standard Voice (same as regular conversations)
  * Select a specialized voice optimized for IVR interactions


Using a specialized voice for IVR interactions can improve success rates when dealing with automated systems that may have trouble recognizing more natural-sounding voices.
## 
[​](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings#model-selection)
Model Selection
Configure which language model handles IVR interactions:
  * Use Standard Model (same as regular conversations)
  * Select a specialized model trained for IVR navigation


Specialized IVR models are optimized for shorter, more precise responses that work well with automated systems.
## 
[​](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings#tag-text)
Tag Text
Configure how IVR interactions are marked in transcripts and logs. Options:
  * Don’t tag
  * Tag with `<ivr>` at the start of IVR interactions


Tagging IVR text can be useful for analysis and debugging, but may affect how the transcript appears in your systems if you’re not handling the tags appropriately.
## 
[​](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings#best-practices)
Best Practices
  1. Enable IVR detection when your agent regularly needs to navigate automated menus
  2. Use specialized voices and models for complex IVR systems
  3. Consider enabling text tagging during testing to help debug navigation issues


These settings only affect how your agent handles automated menus - they don’t impact normal human conversations.
[Linked Numbers](http://docs.vogent.ai/platform-overview/agents/config/linked-numbers)[Overview](http://docs.vogent.ai/platform-overview/agents/model/overview)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
