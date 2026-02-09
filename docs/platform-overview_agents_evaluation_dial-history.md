[Skip to main content](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Post-Call Analysis
Dial History
[Guides](http://docs.vogent.ai/introduction)[API Reference](http://docs.vogent.ai/api-reference/introduction)[SDK](http://docs.vogent.ai/sdk/web-sdk)[Voicelab](http://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](http://docs.vogent.ai/introduction)
  * Quickstart


##### Platform Overview
  * [Introduction](http://docs.vogent.ai/platform-overview/introduction)
  * Agents
    * [Overview](http://docs.vogent.ai/platform-overview/agents/overview)
    * Configuration
    * Model
    * Post-Call Analysis
      * [Overview](http://docs.vogent.ai/platform-overview/agents/evaluation/overview)
      * [Extractors](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
      * [Dial History](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history)
      * [Versioning and Evaluation](http://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation)
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
  * [Viewing Dial History](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#viewing-dial-history)
  * [Analyzing Individual Dials](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#analyzing-individual-dials)
  * [Transcript](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#transcript)
  * [Results](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#results)
  * [Invocation](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#invocation)
  * [Counterfactuals](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#counterfactuals)
  * [Filtering and Navigation](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#filtering-and-navigation)
  * [Exporting Data](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#exporting-data)


Post-Call Analysis
# Dial History
View and analyze past dials
The Dial History page allows you to review all past calls made to and from your agent. You can access detailed information about each call, including recordings, transcripts, and extracted results. You can also use the Counterfactuals feature to test how different versions of your agent would have handled past conversations.
## 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#viewing-dial-history)
Viewing Dial History
There are two ways to view dial history:
  1. Navigate to your agent’s **Dials** tab to view all calls to/from the agent.
  2. Click the **Dial History** button on the left sidebar to view dial history across agents.


## 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#analyzing-individual-dials)
Analyzing Individual Dials
Click on any dial to view its detailed information.
### 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#transcript)
Transcript
The transcript tab shows the complete conversation between the user and your AI agent. Each message is labeled with the speaker (Human/AI) and displayed chronologically. You can click on any Human line to jump to the corresponding timestamp in the recording.
### 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#results)
Results
The **Results** tab provides:
  * Completion reason (e.g., “User Hung Up”)
  * Extractor results (if any extractors were configured)
  * Option to add comments for team collaboration


### 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#invocation)
Invocation
The **Invocation** tab displays:
  * Agent information
  * Agent version used for the call
  * The inputs provided for this call’s invocation


## 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#counterfactuals)
Counterfactuals
The **Run Counterfactual** feature lets you test how different versions of your agent would handle past conversations:
1
[](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history)
Select Version
Choose the prompt version you want to test from the dropdown menu
2
[](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history)
Run Test
Click the “Run” button to simulate how that version would have responded
3
[](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history)
Review Results
Compare the counterfactual responses with the original conversation
This feature is particularly useful when:
  * Evaluating new agent versions before deployment
  * Debugging conversation flows
  * Training and improving your agent’s responses


The **Run Counterfactual** feature runs by passing your model version the dial transcript up to the point of the counterfactual and outputting the response at that point. This isn’t a fully accurate simulation of the conversation (as we can’t simulate the counterparty’s response to your tested model’s output), but it can still be useful for testing your model against specific problematic scenarios.
## 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#filtering-and-navigation)
Filtering and Navigation
Use the Filters menu to:
  * Search for specific dials
  * Filter by date range
  * Filter by call outcome
  * Filter by phone number or connection type


## 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#exporting-data)
Exporting Data
Click the **Export** button to download dial history.
[Extractors](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)[Versioning and Evaluation](http://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
