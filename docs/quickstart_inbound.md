[Skip to main content](http://docs.vogent.ai/quickstart/inbound#content-area)
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
Inbound Agent Quickstart
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
  * [The agent](http://docs.vogent.ai/quickstart/inbound#the-agent)
  * [Creating a new agent](http://docs.vogent.ai/quickstart/inbound#creating-a-new-agent)
  * [Configuring the agent](http://docs.vogent.ai/quickstart/inbound#configuring-the-agent)
  * [Prompting the agent](http://docs.vogent.ai/quickstart/inbound#prompting-the-agent)
  * [Calculating the total using function-calling](http://docs.vogent.ai/quickstart/inbound#calculating-the-total-using-function-calling)
  * [Retrieving the order post-call](http://docs.vogent.ai/quickstart/inbound#retrieving-the-order-post-call)
  * [Making a call](http://docs.vogent.ai/quickstart/inbound#making-a-call)
  * [Phone call](http://docs.vogent.ai/quickstart/inbound#phone-call)
  * [Web call](http://docs.vogent.ai/quickstart/inbound#web-call)
  * [Viewing past calls](http://docs.vogent.ai/quickstart/inbound#viewing-past-calls)
  * [Testing new version on past calls](http://docs.vogent.ai/quickstart/inbound#testing-new-version-on-past-calls)
  * [Conclusion](http://docs.vogent.ai/quickstart/inbound#conclusion)


Quickstart
# Inbound Agent Quickstart
Create an inbound voice agent that can take orders for a restaurant.
In this quickstart, we’ll create an inbound voice agent that can take orders for a restaurant and calculate the total cost of the order. This guide will provide an overview of the platform by walking through the creation of a sample agent; for a more in-depth guide to using Vogent, see the [platform overview](http://docs.vogent.ai/platform-overview/introduction) guide.
Before you go through this guide, make sure to [create an account](http://docs.vogent.ai/quickstart/overview).
## 
[​](http://docs.vogent.ai/quickstart/inbound#the-agent)
The agent
Our inbound agent takes orders and answers basic questions for a fictional restaurant called Bamboo Express.
![Bamboo Express Menu](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/oriental-express.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=c72c39244d86a217a0a8188bd5174996)
## 
[​](http://docs.vogent.ai/quickstart/inbound#creating-a-new-agent)
Creating a new agent
To create a new agent, navigate to the **Agents** tab on the left sidebar and click the **New Agent** button on the top right. For this quickstart, we’ll walk through the pre-built agent together. You can clone this agent to your workspace by following the instructions [here](http://docs.vogent.ai/quickstart/inbound).
## 
[​](http://docs.vogent.ai/quickstart/inbound#configuring-the-agent)
Configuring the agent
Once you click into your cloned agent, you’ll see the agent’s configuration page. This is mission control for your agent, where you can configure the agent’s behavior and settings, go through past dials and run evaluations, and more.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/takeout-agent-config-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=c4a82030df8c46eeac6a0a725008f895)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/takeout-agent-config-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=416754ae86cbc3c1c01d9ec15b718db0)
## 
[​](http://docs.vogent.ai/quickstart/inbound#prompting-the-agent)
Prompting the agent
Click on the **Model** tab to see the language model configuration for this agent. This specific agent is a prompted agent on top of GPT-4o. For more information on prompting agents and choosing a base model, see the [prompting agents](http://docs.vogent.ai/platform-overview/prompting-guide) guide.
Prompt
Ignore previous instructions. You are answering the phones as a representative of the following restaurant:Bamboo Express 140 McConnell Boulevard Denton, Texas 76203When you pick up, open with the following line:Hi, thank you for calling Bamboo Express, this is Kyle, how can I help you?The person on the other end will then say how they want to be helped.For any questions about the store (operating hours, address, phone number, etc.), use the following information to respond:Name: Bamboo Express Address: 140 McConnell Boulevard, Denton, Texas 76203 Phone Number: 800-806-6453 Hours: 9 AM to 11 PM, 7 days a week Open right now: TrueYour main purpose is to accept orders. If the customer would like to place an order, ask them what they would like.These are the possible menu items:Orange Chicken Eggplant Tofu Broccoli Beef White Rice Brown RiceAs the customer requests items, ask if they would like anything else, until they confirm that they’re done ordering. If they ask for any items that are not on the above menu, let them know that you don’t have that item. Entrees do not come with rice.The customer may provide special instructions; acknowledge these instructions.Once the customer has completed their order, tell them you’ll ring it up, and determine the total for the order. The total can be calculated using the `get_total` function. This function will return a number with a decimal, which is the cost in dollars of the meal; tell the customer the cost by saying the number of dollars and cents that it is.Once you have the total, let them know the price and ask for their name.Finally, let them know that the order will be ready for pickup in 20 minutes.If you receive any requests that you cannot answer or if the caller needs assistance beyond what is outlined here, apologize and let them know that this line only handles orders.
## 
[​](http://docs.vogent.ai/quickstart/inbound#calculating-the-total-using-function-calling)
Calculating the total using function-calling
The prompt above references a function called `get_total`.
> Once the customer has completed their order, tell them you’ll ring it up, and determine the total for the order. The total can be calculated using the `get_total` function. This function will return a number with a decimal, which is the cost in dollars of the meal; tell the customer the cost by saying the number of dollars and cents that it is.
Vogent supports leveraging function-calling within agents to perform actions and retrieve information live. To include a function in your agent, you’ll need to:
  1. Define the function in the **Functions** tab on the left sidebar.
  2. Include the function as one of the agent’s functions in the Agent’s **Functions** tab.
  3. Reference the function in your prompt.

The `get_total` function hits an external API with the counts for each item in the order, and receives the total cost of the order (The API simply sums the cost of each ordered item). To see how we’ve defined the function, head to the **Functions** tab, and select the `get_total` function.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/get-total-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=ffccf8c9a1cea01d85f72e79dfe9e5fd)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/get-total-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=bc029179703c0d8fad49baf2f995145e)
For more information on how to define functions and use them effectively, see the [functions](http://docs.vogent.ai/guides/functions) guide.
## 
[​](http://docs.vogent.ai/quickstart/inbound#retrieving-the-order-post-call)
Retrieving the order post-call
After the call is completed, you can retrieve the order information from the call using the [Dial Extractor webhook](http://docs.vogent.ai/webhooks/dial-extractor). The webhook will return the extracted order information in the format defined within the agent’s **Extractor** tab. For this particular agent, we’ve defined a single extractor field as a JSON object with the following schema using the _Custom_ type:
Extractor Schema
Copy
```
{
 "$schema": "http://json-schema.org/draft-07/schema#",
 "type": "object",
 "properties": {
  "items": {
   "type": "object",
   "properties": {
    "orange_chicken": {
     "type": "integer",
     "description": "Number of Orange Chicken orders",
     "minimum": 0
    },
    "eggplant_tofu": {
     "type": "integer", 
     "description": "Number of Eggplant Tofu orders",
     "minimum": 0
    },
    "broccoli_beef": {
     "type": "integer",
     "description": "Number of Broccoli Beef orders",
     "minimum": 0
    },
    "white_rice": {
     "type": "integer",
     "description": "Number of White Rice orders",
     "minimum": 0
    },
    "brown_rice": {
     "type": "integer",
     "description": "Number of Brown Rice orders",
     "minimum": 0
    }
   },
   "additionalProperties": false
  },
  "subtotal": {
   "type": "number",
   "description": "Total cost of the order in dollars",
   "minimum": 0
  },
  "special_instructions": {
   "type": "string",
   "description": "Any special instructions for the order"
  },
  "customer_name": {
   "type": "string",
   "description": "Name of the customer placing the order"
  },
  "completed_order": {
   "type": "boolean",
   "description": "Whether this order should be submitted (e.g. if the customer says they want to cancel the order, or if no order was placed, this should be false)"
  }
 },
 "required": ["items", "subtotal", "customer_name", "completed_order"],
 "additionalProperties": false
}

```

Alternatively, you can define your extractor output field-by-field. For more information on how to define extractors, see the [extractors](http://docs.vogent.ai/guides/extractors) guide.
## 
[​](http://docs.vogent.ai/quickstart/inbound#making-a-call)
Making a call
### 
[​](http://docs.vogent.ai/quickstart/inbound#phone-call)
Phone call
To make a phone call to an inbound agent, you’ll first need to create a phone number; see the [getting started](http://docs.vogent.ai/quickstart/overview) guide for more information. Once you’ve created a phone number, you can attach it to the agent by going to the agent’s **Config** tab, clicking **Link Number** , and selecting the chosen phone number. You can then make a call to the agent by dialing the phone number you’ve attached to the agent.
### 
[​](http://docs.vogent.ai/quickstart/inbound#web-call)
Web call
To make a web call to the inbound agent, you can just click on the **Make Call** button on the top-right of the agent’s page, toggle to **Web** , then click **Talk**.
## 
[​](http://docs.vogent.ai/quickstart/inbound#viewing-past-calls)
Viewing past calls
To view past calls to the agent, you can go to the agent’s **Dials** tab. This will show you a list of all past calls to the agent as well as the extractor results. You can click into any dial to listen to the recording and see the full transcript of the call, among other things. You can also filter calls by date range, call type, and more, or view dials across agents in the **Dial History** tab on the left sidebar.
### 
[​](http://docs.vogent.ai/quickstart/inbound#testing-new-version-on-past-calls)
Testing new version on past calls
If you’ve made changes to your agent, you can test the new version on past calls by clicking the **Run Counterfactual** button when you’ve clicked into a dial. This will run the new agent on the same call transcript and show you the results.
Counterfactuals will feed call history up to the current line to generate each response, so they won’t be _perfect_ reconstructions of how the conversation would have gone. LLM-as-judge functionality is coming soon to enable more dynamic agent testing. See the [counterfactuals](http://docs.vogent.ai/guides/counterfactuals) guide for more information.
## 
[​](http://docs.vogent.ai/quickstart/inbound#conclusion)
Conclusion
In this quickstart, we’ve walked through the creation of an inbound agent that can take orders for a restaurant and calculate the total cost of the order. We’ve also covered how to define functions, use them in prompts, and retrieve the order information post-call. This was a cursory overview of the different components of Vogent that can be used to create an inbound agent. To go further in depth on any of these features, or to understand functionality not covered here, see the [platform overview](http://docs.vogent.ai/quickstart/platform-overview/introduction) guide. You can also check out some of our other quickstart guides for different agent types:
  * [Outbound Agent Quickstart](http://docs.vogent.ai/quickstart/outbound)
  * [Flow Builder Quickstart](http://docs.vogent.ai/quickstart/flow-builder)


[Overview](http://docs.vogent.ai/quickstart/overview)[Outbound Agent Quickstart](http://docs.vogent.ai/quickstart/outbound)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
