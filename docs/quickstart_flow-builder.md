[Skip to main content](http://docs.vogent.ai/quickstart/flow-builder#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Quickstart
Flow Builder Agent Quickstart
[Guides](http://docs.vogent.ai/introduction)[API Reference](http://docs.vogent.ai/api-reference/introduction)[SDK](http://docs.vogent.ai/sdk/web-sdk)[Voicelab](http://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](http://docs.vogent.ai/introduction)
  * Quickstart
    * [Overview](http://docs.vogent.ai/quickstart/overview)
    * [Inbound Agent Quickstart](http://docs.vogent.ai/quickstart/inbound)
    * [Outbound Agent Quickstart](http://docs.vogent.ai/quickstart/outbound)
    * [Flow Builder Agent Quickstart](http://docs.vogent.ai/quickstart/flow-builder)


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
  * [Dials and Dial Sessions](http://docs.vogent.ai/developers/dials-dialsessions)
  * [Dials Statuses](http://docs.vogent.ai/developers/dial-statuses)
  * [Flow Builder Schemas](http://docs.vogent.ai/developers/schemas)


On this page
  * [The agent](http://docs.vogent.ai/quickstart/flow-builder#the-agent)
  * [Creating a new agent](http://docs.vogent.ai/quickstart/flow-builder#creating-a-new-agent)
  * [Configuring the agent](http://docs.vogent.ai/quickstart/flow-builder#configuring-the-agent)
  * [Building the agent’s conversational logic](http://docs.vogent.ai/quickstart/flow-builder#building-the-agent%E2%80%99s-conversational-logic)
  * [Question node](http://docs.vogent.ai/quickstart/flow-builder#question-node)
  * [Freeform node](http://docs.vogent.ai/quickstart/flow-builder#freeform-node)
  * [Function node](http://docs.vogent.ai/quickstart/flow-builder#function-node)
  * [Retrieving details post-call](http://docs.vogent.ai/quickstart/flow-builder#retrieving-details-post-call)
  * [Making a call](http://docs.vogent.ai/quickstart/flow-builder#making-a-call)
  * [Phone call](http://docs.vogent.ai/quickstart/flow-builder#phone-call)
  * [Web call](http://docs.vogent.ai/quickstart/flow-builder#web-call)
  * [Viewing past calls](http://docs.vogent.ai/quickstart/flow-builder#viewing-past-calls)
  * [Testing new version on past calls](http://docs.vogent.ai/quickstart/flow-builder#testing-new-version-on-past-calls)
  * [Conclusion](http://docs.vogent.ai/quickstart/flow-builder#conclusion)


Quickstart
# Flow Builder Agent Quickstart
Create an inbound voice agent that can schedule an appointment.
In this quickstart, we’ll use Vogent’s Flow Builder to build an inbound voice agent that can schedule an appointment for a clinic. Vogent’s Flow Builder is a visual interface for building voice agents. It allows you to create a flow of prompts and functions that can be used to build complex voice agents. The Flow Builder is a powerful tool that allows you to build performant agents without writing code. For more information on the Flow Builder, see the [Flow Builder](http://docs.vogent.ai/platform-overview/agents/flow-builder) guide.
## 
[​](http://docs.vogent.ai/quickstart/flow-builder#the-agent)
The agent
Our inbound Flow Builder agent will act as a scheduling line for a fictional dental clinic called _Shiny Smiles_. It will take down names, check for insurance, and hit external APIs to get appointment availability, before scheduling with the patient.
## 
[​](http://docs.vogent.ai/quickstart/flow-builder#creating-a-new-agent)
Creating a new agent
To create a new agent, navigate to the **Agents** tab on the left sidebar and click the **New Agent** button on the top right. For this quickstart, we’ll walk through the pre-built agent together. You can clone this agent to your workspace by following the instructions [here](http://docs.vogent.ai/quickstart/flow-builder).
## 
[​](http://docs.vogent.ai/quickstart/flow-builder#configuring-the-agent)
Configuring the agent
Once you click into your cloned agent, you’ll see the agent’s configuration page. This is mission control for your agent, where you can configure the agent’s behavior and settings, go through past dials and run evaluations, and more.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/takeout-agent-config-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=c4a82030df8c46eeac6a0a725008f895)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/takeout-agent-config-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=416754ae86cbc3c1c01d9ec15b718db0)
## 
[​](http://docs.vogent.ai/quickstart/flow-builder#building-the-agent’s-conversational-logic)
Building the agent’s conversational logic
Click on the **Model** tab to see the language model configuration for this agent. This specific agent is a **Flow Builder** agent on top of Vogent’s Base Survey model, which is a custom model from Vogent that interprets Flow Builder configurations. To view the full flow, click on the **Edit** button on the bottom right of the **Flow** window. To look through the different questions and transitions, try clicking on different nodes and edges. Diving through a few examples:
### 
[​](http://docs.vogent.ai/quickstart/flow-builder#question-node)
Question node
A question node is used to ask a question to the respondent. You can indicate the question text, the answer type (e.g. Freeform, Multiple Choice, Multiple Select, etc.), and the answer options. Note that the provided answer does not have to verbatim match the answer choices; the model will match the provided answer to the closest choice.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/question-node-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=0eeed6bb3ebff0c966d6187c652fada2)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/question-node-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=852b1899260b9d7abeb3731328715e45)
### 
[​](http://docs.vogent.ai/quickstart/flow-builder#freeform-node)
Freeform node
A freeform node is a node in which the agent is prompted to engage in some sort of exchange with the respondent. It can be useful for inserting a remark, or having the agent offer some pleasantries at the end of a call. Note that a freeform node will only progress if it’s prompted to do so given some condition; otherwise, it is a terminal node.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/freeform-node-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=619d92b59619a4ffe972df155088113c)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/freeform-node-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=2a9765e1a98edd6cb8cc47a13fef15f5)
### 
[​](http://docs.vogent.ai/quickstart/flow-builder#function-node)
Function node
A function node is used to call an external function. For more information on how to add tools (like functions) to your agent, check out the [tools](http://docs.vogent.ai/guides/tools) guide. In this particular agent, we’ve defined a function called `get_availability` that hits an external API to get appointment availability.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/function_node_light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=bbb1441980326e86a27e9decb3cc0092)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/function-node-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=e35124a9a96d2b8f07c0dffb53c6a211)
## 
[​](http://docs.vogent.ai/quickstart/flow-builder#retrieving-details-post-call)
Retrieving details post-call
After the call is completed, you can retrieve the appointment details from the call using the [Dial Extractor webhook](http://docs.vogent.ai/webhooks/dial-extractor). The webhook will return the extracted appointment details in the format defined within the agent’s **Extractor** tab. For this particular agent, we’ve defined a few relevant fields that could help a provider enter a patient’s appointment into their systems.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/flow-extractor-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=7557176a6c6e8591f461fdf737f03301)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/flow-extractor-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=21a3a9814289b09b32636dce10240656)
For more information on how to define extractors, see the [extractors](http://docs.vogent.ai/guides/extractors) guide.
## 
[​](http://docs.vogent.ai/quickstart/flow-builder#making-a-call)
Making a call
### 
[​](http://docs.vogent.ai/quickstart/flow-builder#phone-call)
Phone call
To make a phone call to an inbound agent, you’ll first need to create a phone number; see the [getting started](http://docs.vogent.ai/quickstart/overview) guide for more information. Once you’ve created a phone number, you can attach it to the agent by going to the agent’s **Config** tab, clicking **Link Number** , and selecting the chosen phone number. You can then make a call to the agent by dialing the phone number you’ve attached to the agent.
### 
[​](http://docs.vogent.ai/quickstart/flow-builder#web-call)
Web call
To make a web call to the inbound agent, you can just click on the **Make Call** button on the top-right of the agent’s page, toggle to **Web** , then click **Talk**.
## 
[​](http://docs.vogent.ai/quickstart/flow-builder#viewing-past-calls)
Viewing past calls
To view past calls to the agent, you can go to the agent’s **Dials** tab. This will show you a list of all past calls to the agent as well as the extractor results. You can click into any dial to listen to the recording and see the full transcript of the call, among other things. You can also filter calls by date range, call type, and more, or view dials across agents in the **Dial History** tab on the left sidebar.
### 
[​](http://docs.vogent.ai/quickstart/flow-builder#testing-new-version-on-past-calls)
Testing new version on past calls
If you’ve made changes to your agent, you can test the new version on past calls by clicking the **Run Counterfactual** button when you’ve clicked into a dial. This will run the new agent on the same call transcript and show you the results.
Counterfactuals will feed call history up to the current line to generate each response, so they won’t be _perfect_ reconstructions of how the conversation would have gone. LLM-as-judge functionality is coming soon to enable more dynamic agent testing. See the [counterfactuals](http://docs.vogent.ai/guides/counterfactuals) guide for more information.
## 
[​](http://docs.vogent.ai/quickstart/flow-builder#conclusion)
Conclusion
In this quickstart, we’ve walked through the creation of a Flow Builder agent that can schedule an appointment for a dental clinic. We’ve also covered how to define functions, use them in prompts, and retrieve the appointment details post-call. This was a cursory overview of the different components of Vogent that can be used to create a Flow Builder agent. To go further in depth on any of these features, or to understand functionality not covered here, see the [platform overview](http://docs.vogent.ai/overview) guide. You can also check out some of our other quickstart guides for different agent types:
  * [Outbound Agent Quickstart](http://docs.vogent.ai/quickstart/outbound)
  * [Inbound Agent Quickstart](http://docs.vogent.ai/quickstart/inbound)


[Outbound Agent Quickstart](http://docs.vogent.ai/quickstart/outbound)[Introduction](http://docs.vogent.ai/platform-overview/introduction)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
