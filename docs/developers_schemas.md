[Skip to main content](http://docs.vogent.ai/developers/schemas#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
For Developers
Flow Builder Schemas
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
  * [Dials and Dial Sessions](http://docs.vogent.ai/developers/dials-dialsessions)
  * [Dials Statuses](http://docs.vogent.ai/developers/dial-statuses)
  * [Flow Builder Schemas](http://docs.vogent.ai/developers/schemas)


On this page
  * [Function Call](http://docs.vogent.ai/developers/schemas#function-call)
  * [Question](http://docs.vogent.ai/developers/schemas#question)
  * [Freeform](http://docs.vogent.ai/developers/schemas#freeform)


For Developers
# Flow Builder Schemas
The API allows you to describe flow nodes through the API. When creating/updating a versioned prompt, you want to specify an object that conforms to the appropriate schema in the `nodeData` field. If you want to use the output of a previous node in a future node, you can reference it by using double curly braces. For example, if you have a node with the ID `node_1` and you want to use the output of `node_1` in `node_2`, you can reference it as `{{node.node_1.output}}` in any string field. The notation to lookup any data is `{{node.node_id.field_name}}`.
### 
[​](http://docs.vogent.ai/developers/schemas#function-call)
Function Call
**Type:** `function_call` **Schema:**
Copy
```
{
 functionId: string, // The ID of the function to call within vogent
 inputs: {
  name: string,
  value: string
 }[], // The inputs to the function
 outputs: {
  type: "BOOLEAN" | "STRING" | "INTEGER" | "FLOAT" | "CUSTOM",
  name: string,
  nullable: bool,
  description: string,
  customFieldJsonSchema?: string, // If the type is CUSTOM, this is the JSON schema for the field
 }[]
}

```

### 
[​](http://docs.vogent.ai/developers/schemas#question)
Question
**Type:** `question` **Schema:**
Copy
```
{
 questionSchemaId?: string,
 question: string,
 questionType: "multiple_choice" | "multiple_select" | "freeform" | "numeric",
 options?: string[],
 clarificationDetails?: string, // Any clarification details that may be helpful to the model
}

```

### 
[​](http://docs.vogent.ai/developers/schemas#freeform)
Freeform
**Type:** `freeform` **Schema:**
Copy
```
{
 prompt: string // The prompt to feed to the model
}

```

[Dials Statuses](http://docs.vogent.ai/developers/dial-statuses)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
