[Skip to main content](http://docs.vogent.ai/quickstart/outbound#content-area)
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
Outbound Agent Quickstart
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
  * [The agent](http://docs.vogent.ai/quickstart/outbound#the-agent)
  * [Creating a new agent](http://docs.vogent.ai/quickstart/outbound#creating-a-new-agent)
  * [Configuring the agent](http://docs.vogent.ai/quickstart/outbound#configuring-the-agent)
  * [Prompting the agent](http://docs.vogent.ai/quickstart/outbound#prompting-the-agent)
  * [The IVR Model](http://docs.vogent.ai/quickstart/outbound#the-ivr-model)
  * [The Conversational Model](http://docs.vogent.ai/quickstart/outbound#the-conversational-model)
  * [Retrieving the hours post-call](http://docs.vogent.ai/quickstart/outbound#retrieving-the-hours-post-call)
  * [Making a call](http://docs.vogent.ai/quickstart/outbound#making-a-call)
  * [Phone call](http://docs.vogent.ai/quickstart/outbound#phone-call)
  * [Web call](http://docs.vogent.ai/quickstart/outbound#web-call)
  * [Viewing past calls](http://docs.vogent.ai/quickstart/outbound#viewing-past-calls)
  * [Testing new version on past calls](http://docs.vogent.ai/quickstart/outbound#testing-new-version-on-past-calls)
  * [Conclusion](http://docs.vogent.ai/quickstart/outbound#conclusion)


Quickstart
# Outbound Agent Quickstart
Create an outbound voice agent that can navigate an IVR and get a restaurant’s hours.
In this quickstart, we’ll create an outbound voice agent that can navigate an IVR and get a restaurant’s hours. This guide will provide an overview of the platform by walking through the creation of a sample agent; for a more in-depth guide to using Vogent, see the [platform overview](http://docs.vogent.ai/overview) guide.
Before you go through this guide, make sure to [create an account](http://docs.vogent.ai/quickstart/overview).
## 
[​](http://docs.vogent.ai/quickstart/outbound#the-agent)
The agent
Our outbound agent navigates an IVR and gets a restaurant’s hours.
## 
[​](http://docs.vogent.ai/quickstart/outbound#creating-a-new-agent)
Creating a new agent
To create a new agent, navigate to the **Agents** tab on the left sidebar and click the **New Agent** button on the top right. For this quickstart, we’ll walk through the pre-built agent together. You can clone this agent to your workspace by following the instructions [here](http://docs.vogent.ai/quickstart/outbound).
## 
[​](http://docs.vogent.ai/quickstart/outbound#configuring-the-agent)
Configuring the agent
Once you click into your cloned agent, you’ll see the agent’s configuration page. This is mission control for your agent, where you can configure the agent’s behavior and settings, go through past dials and run evaluations, and more.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/hours-agent-config-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=b3f291a6692d72ea37852e9a5219cb31)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/hours-agent-config-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=0c56dd9d7e85f6a1d80098573e8eb927)
## 
[​](http://docs.vogent.ai/quickstart/outbound#prompting-the-agent)
Prompting the agent
Click on the **Model** tab to see the language model configuration for this agent. This specific agent comprises both an IVR navigation model and a conversational model. The IVR model triggers when Vogent detects that a line is from an IVR; once it detects a human line, it switches irreversibly to the conversational model. See the [IVR Settings](http://docs.vogent.ai/platform-overview/agents/config/ivr-settings) section for more information. You can view each model by going to the **Version** dropdown and selecting `ivr-version` or `conversational-version`.
### 
[​](http://docs.vogent.ai/quickstart/outbound#the-ivr-model)
The IVR Model
The IVR model is a prompted agent on top of GPT-4o. The prompt is as follows:
IVR Model Prompt
Ignore previous instructions. You are calling a restaurant, and I need you to navigate the IVR to find the hours (or, if the IVR does not give you the option to find the hours, I need you to navigate to reach a human).To press a button, output `<|press:n|>`, where `n` is the button you want to press (so e.g. `<|press:1|>` to press 1). If you need to speak, just output the line that you want to say.If you do not want to do anything, please output `<|silence|>`. Unless you need to press or say something, you should output `<|silence|>`.If you have found the restaurant hours through their IVR, or if you reach a voicemail inbox or are asked to leave a message, output `<|hangup|>` to end the call.If the IVR does not include the hours, then navigate to reach a human.Do not output anything else.
### 
[​](http://docs.vogent.ai/quickstart/outbound#the-conversational-model)
The Conversational Model
The conversational model is a prompted agent on top of Vogent’s Base Conversations model. This is a custom model that we offer that has been fine-tuned to perform well on the phone with minimal prompting. The prompt is as follows:
Conversational Model Prompt
Ignore previous instructions. You are calling a restaurant, `{{restaurant_name}}`, to find out today’s hours.When the receptionist picks up, greet them and ask them what `{{restaurant_name}}`’s hours are today. If they only offer the closing time, make sure to ask them for the opening time too.Once they answer, thank them and end the call by outputting `<|hangup|>`.Do not ask any other questions. If asked, your name is Jay. You may be asked to be put on hold; if so, simply output `<|silence|>` until the hold is over.
For more information on prompting agents and choosing a base model, see the [prompting agents](http://docs.vogent.ai/guides/prompting-agents) guide.
## 
[​](http://docs.vogent.ai/quickstart/outbound#retrieving-the-hours-post-call)
Retrieving the hours post-call
After the call is completed, you can retrieve the hours from the call using the [Dial Extractor webhook](http://docs.vogent.ai/webhooks/dial-extractor). The webhook will return the extracted hours in the format defined within the agent’s **Extractor** tab. You can also view the extracted hours by clicking on the dial in the agent’s **Dials** tab, or in the **Dial History** tab in the left sidebar. For this particular agent, we’ve defined the following extractor fields:
Field Name| Type| Description| Nullable  
---|---|---|---  
`opening_time`| `string`| The opening time, in military time, in the format HH:MM| `false`  
`closing_time`| `string`| The closing time, in military time, in the format HH:MM| `false`  
Thus, after every call, Vogent’s extractor model will parse the transcript for the `opening_time` and `closing_time` fields, and store them in the dial. For more information on how to define extractors and use them effectively, see the [extractors](http://docs.vogent.ai/guides/extractors) guide.
## 
[​](http://docs.vogent.ai/quickstart/outbound#making-a-call)
Making a call
### 
[​](http://docs.vogent.ai/quickstart/outbound#phone-call)
Phone call
To make a phone call from an outbound agent, you’ll first need to create a phone number; see the [getting started](http://docs.vogent.ai/quickstart/overview) guide for more information. You can then follow these steps:
1
[](http://docs.vogent.ai/quickstart/outbound)
Open the call modal
Click on the **Make Call** button on the top-right of the agent’s page.
2
[](http://docs.vogent.ai/quickstart/outbound)
Populate fields
In the **Configure** section, click on **Find From Prompt** to extract all of the variables from the prompt. Then, for each variable (in this case, just `{{restaurant_name}}`), enter a value.
3
[](http://docs.vogent.ai/quickstart/outbound)
Select an outbound phone number
Below the **Configure** section, toggle to **Phone** and select the phone number you want to call from.
4
[](http://docs.vogent.ai/quickstart/outbound)
Make the call
Enter the phone number that you’d like to dial, then click **Dial**.
### 
[​](http://docs.vogent.ai/quickstart/outbound#web-call)
Web call
To make a web call, you can follow the steps above; just toggle to **Web** instead of **Phone**.
## 
[​](http://docs.vogent.ai/quickstart/outbound#viewing-past-calls)
Viewing past calls
To view past calls to the agent, you can go to the agent’s **Dials** tab. This will show you a list of all past calls to the agent as well as the extractor results. You can click into any dial to listen to the recording and see the full transcript of the call, among other things. You can also filter calls by date range, call type, and more, or view dials across agents in the **Dial History** tab on the left sidebar.
### 
[​](http://docs.vogent.ai/quickstart/outbound#testing-new-version-on-past-calls)
Testing new version on past calls
If you’ve made changes to your agent, you can test the new version on past calls by clicking the **Run Counterfactual** button when you’ve clicked into a dial. This will run the new agent on the same call transcript and show you the results.
Counterfactuals will feed call history up to the current line to generate each response, so they won’t be _perfect_ reconstructions of how the conversation would have gone. LLM-as-judge functionality is coming soon to enable more dynamic agent testing. See the [counterfactuals](http://docs.vogent.ai/guides/counterfactuals) guide for more information.
## 
[​](http://docs.vogent.ai/quickstart/outbound#conclusion)
Conclusion
In this quickstart, we’ve walked through the creation of an outbound agent that can navigate an IVR and get a restaurant’s hours. We’ve also covered how to define extractors and use them effectively. This was a cursory overview of the different components of Vogent that can be used to create an outbound agent. To go further in depth on any of these features, or to understand functionality not covered here, see the [platform overview](http://docs.vogent.ai/overview) guide. You can also check out some of our other quickstart guides for different agent types:
  * [Inbound Agent Quickstart](http://docs.vogent.ai/quickstart/inbound)
  * [Survey Agent Quickstart](http://docs.vogent.ai/quickstart/survey)


[Inbound Agent Quickstart](http://docs.vogent.ai/quickstart/inbound)[Flow Builder Agent Quickstart](http://docs.vogent.ai/quickstart/flow-builder)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
