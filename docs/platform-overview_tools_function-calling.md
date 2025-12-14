Tools

Function Calling



    * Quickstart





    * Agents

  * Voices

  * Tools

                    



    * Importing via SIP

  



      



  * Webhooks

      



  * [Defining a function](#defining-a-function)
  * [API](#api)
  * [Configuration](#configuration)
  * [Knowledge Base](#knowledge-base)
  * [Configuration](#configuration-2)
  * [Function Schema](#function-schema)
  * [Call Transfer](#call-transfer)
  * [Configuration](#configuration-3)
  * [Function Schema](#function-schema-2)
  * [Example Usage](#example-usage)



Tools

# Function Calling

Connect agents to external data and systems

## 

[​](#defining-a-function)

Defining a function

When you create a function in the **Functions** tab, you’ll have a few different options for defining it.

### 

[​](#api)

API

The API function type allows your agent to make external API calls during conversations. This is useful for retrieving real-time data or performing actions in external systems.

#### 

[​](#configuration)

Configuration

1

Select function type

Choose “API” as the Function Type in the dropdown menu.

2

Configure endpoint

In the Config tab:

  1. Enter the API URL for your endpoint
  2. Add any required headers using the “Add” button in the Headers section



3

Define schema

In the Inputs and Outputs tabs:

  1. Add input fields that your API endpoint expects
  2. Define the output schema that matches your API’s response format



When your agent calls this function, Vogent will make a POST request to your endpoint with the specified headers and input parameters, then return the response to your agent.

All API calls are made via POST requests. Make sure your endpoint is configured to accept POST methods.

### 

[​](#knowledge-base)

Knowledge Base

The Knowledge Base function type enables your agent to search and retrieve information from your uploaded knowledge base documents. This is useful for giving your agent access to company-specific information or documentation.

#### 

[​](#configuration-2)

Configuration

1

Select function type

Choose “Knowledge Base” as the Function Type in the dropdown menu.

2

Select knowledge base

In the Config tab, select the knowledge base you want your agent to access from the dropdown menu.

#### 

[​](#function-schema)

Function Schema

The function uses a simple query-response format:

  * Input: `query` (string) - The query that’d be answered by the knowledge base files
  * Output: Returns an answer to the query

When your agent calls this function, it will search the selected knowledge base using the provided query and return an answer to the query for the agent to use in its response.

Make sure you’ve uploaded and indexed your documents in the Knowledge Base section before creating a knowledge base function. For more information on how knowledge bases work in Vogent, check out our [knowledge base guide](/platform-overview/tools/knowledge-bases).

### 

[​](#call-transfer)

Call Transfer

The Call Transfer function type allows your agent to transfer calls to specified phone numbers. This is useful for scenarios where the conversation needs to be escalated to a human agent or redirected to another department. Call transfer functions accept a single input parameter:

  * `destination`: The phone number where the call should be transferred (must match one of the allowed numbers configured)



#### 

[​](#configuration-3)

Configuration

To set up a call transfer function:

1

Select function type

Choose “Call Transfer” as the Function Type in the dropdown menu.

2

Configure allowed numbers

In the Config tab:

  1. Click the “Add” button to input permitted phone numbers
  2. Use the country code selector to specify the region (e.g., +1 for US/Canada)
  3. Add all phone numbers that should be available as transfer destinations



#### 

[​](#function-schema-2)

Function Schema

The function accepts a single input parameter:

  * `destination`: The phone number where the call should be transferred (must match one of the allowed numbers configured)

When your agent calls this function, the active call will be transferred to the specified destination number, ending the conversation with the AI agent.

#### 

[​](#example-usage)

Example Usage

In your agent prompts, you can include instructions like:

> If the customer requests to speak with a human representative, call the `transfer_call` function with the appropriate destination number from the allowed list.

[Voice Cloning](/platform-overview/voices/voice-cloning)[Knowledge Bases](/platform-overview/tools/knowledge-bases)