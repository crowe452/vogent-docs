[Skip to main content](http://docs.vogent.ai/platform-overview/tools/function-calling#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Tools
Function Calling
[Guides](http://docs.vogent.ai/introduction)[API Reference](http://docs.vogent.ai/api-reference/introduction)[SDK](http://docs.vogent.ai/sdk/web-sdk)[Voicelab](http://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](http://docs.vogent.ai/introduction)
  * Quickstart


##### Platform Overview
  * [Introduction](http://docs.vogent.ai/platform-overview/introduction)
  * Agents
  * Voices
  * Tools
    * [Function Calling](http://docs.vogent.ai/platform-overview/tools/function-calling)
    * [Knowledge Bases](http://docs.vogent.ai/platform-overview/tools/knowledge-bases)
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
  * [Defining a function](http://docs.vogent.ai/platform-overview/tools/function-calling#defining-a-function)
  * [API](http://docs.vogent.ai/platform-overview/tools/function-calling#api)
  * [Configuration](http://docs.vogent.ai/platform-overview/tools/function-calling#configuration)
  * [Knowledge Base](http://docs.vogent.ai/platform-overview/tools/function-calling#knowledge-base)
  * [Configuration](http://docs.vogent.ai/platform-overview/tools/function-calling#configuration-2)
  * [Function Schema](http://docs.vogent.ai/platform-overview/tools/function-calling#function-schema)
  * [Call Transfer](http://docs.vogent.ai/platform-overview/tools/function-calling#call-transfer)
  * [Configuration](http://docs.vogent.ai/platform-overview/tools/function-calling#configuration-3)
  * [Function Schema](http://docs.vogent.ai/platform-overview/tools/function-calling#function-schema-2)
  * [Example Usage](http://docs.vogent.ai/platform-overview/tools/function-calling#example-usage)


Tools
# Function Calling
Connect agents to external data and systems
## 
[​](http://docs.vogent.ai/platform-overview/tools/function-calling#defining-a-function)
Defining a function
When you create a function in the **Functions** tab, you’ll have a few different options for defining it.
### 
[​](http://docs.vogent.ai/platform-overview/tools/function-calling#api)
API
The API function type allows your agent to make external API calls during conversations. This is useful for retrieving real-time data or performing actions in external systems.
#### 
[​](http://docs.vogent.ai/platform-overview/tools/function-calling#configuration)
Configuration
1
[](http://docs.vogent.ai/platform-overview/tools/function-calling)
Select function type
Choose “API” as the Function Type in the dropdown menu.
2
[](http://docs.vogent.ai/platform-overview/tools/function-calling)
Configure endpoint
In the Config tab:
  1. Enter the API URL for your endpoint
  2. Add any required headers using the “Add” button in the Headers section


3
[](http://docs.vogent.ai/platform-overview/tools/function-calling)
Define schema
In the Inputs and Outputs tabs:
  1. Add input fields that your API endpoint expects
  2. Define the output schema that matches your API’s response format


When your agent calls this function, Vogent will make a POST request to your endpoint with the specified headers and input parameters, then return the response to your agent.
All API calls are made via POST requests. Make sure your endpoint is configured to accept POST methods.
### 
[​](http://docs.vogent.ai/platform-overview/tools/function-calling#knowledge-base)
Knowledge Base
The Knowledge Base function type enables your agent to search and retrieve information from your uploaded knowledge base documents. This is useful for giving your agent access to company-specific information or documentation.
#### 
[​](http://docs.vogent.ai/platform-overview/tools/function-calling#configuration-2)
Configuration
1
[](http://docs.vogent.ai/platform-overview/tools/function-calling)
Select function type
Choose “Knowledge Base” as the Function Type in the dropdown menu.
2
[](http://docs.vogent.ai/platform-overview/tools/function-calling)
Select knowledge base
In the Config tab, select the knowledge base you want your agent to access from the dropdown menu.
#### 
[​](http://docs.vogent.ai/platform-overview/tools/function-calling#function-schema)
Function Schema
The function uses a simple query-response format:
  * Input: `query` (string) - The query that’d be answered by the knowledge base files
  * Output: Returns an answer to the query

When your agent calls this function, it will search the selected knowledge base using the provided query and return an answer to the query for the agent to use in its response.
Make sure you’ve uploaded and indexed your documents in the Knowledge Base section before creating a knowledge base function. For more information on how knowledge bases work in Vogent, check out our [knowledge base guide](http://docs.vogent.ai/platform-overview/tools/knowledge-bases).
### 
[​](http://docs.vogent.ai/platform-overview/tools/function-calling#call-transfer)
Call Transfer
The Call Transfer function type allows your agent to transfer calls to specified phone numbers. This is useful for scenarios where the conversation needs to be escalated to a human agent or redirected to another department. Call transfer functions accept a single input parameter:
  * `destination`: The phone number where the call should be transferred (must match one of the allowed numbers configured)


#### 
[​](http://docs.vogent.ai/platform-overview/tools/function-calling#configuration-3)
Configuration
To set up a call transfer function:
1
[](http://docs.vogent.ai/platform-overview/tools/function-calling)
Select function type
Choose “Call Transfer” as the Function Type in the dropdown menu.
2
[](http://docs.vogent.ai/platform-overview/tools/function-calling)
Configure allowed numbers
In the Config tab:
  1. Click the “Add” button to input permitted phone numbers
  2. Use the country code selector to specify the region (e.g., +1 for US/Canada)
  3. Add all phone numbers that should be available as transfer destinations


#### 
[​](http://docs.vogent.ai/platform-overview/tools/function-calling#function-schema-2)
Function Schema
The function accepts a single input parameter:
  * `destination`: The phone number where the call should be transferred (must match one of the allowed numbers configured)

When your agent calls this function, the active call will be transferred to the specified destination number, ending the conversation with the AI agent.
#### 
[​](http://docs.vogent.ai/platform-overview/tools/function-calling#example-usage)
Example Usage
In your agent prompts, you can include instructions like:
> If the customer requests to speak with a human representative, call the `transfer_call` function with the appropriate destination number from the allowed list.
[Voice Cloning](http://docs.vogent.ai/platform-overview/voices/voice-cloning)[Knowledge Bases](http://docs.vogent.ai/platform-overview/tools/knowledge-bases)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
