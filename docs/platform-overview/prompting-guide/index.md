[Skip to main content](https://docs.vogent.ai/platform-overview/prompting-guide#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Platform Overview
Prompting Guide
[Guides](https://docs.vogent.ai/introduction)[API Reference](https://docs.vogent.ai/api-reference/introduction)[SDK](https://docs.vogent.ai/sdk/web-sdk)[Voicelab](https://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](https://docs.vogent.ai/introduction)
  * Quickstart


##### Platform Overview
  * [Introduction](https://docs.vogent.ai/platform-overview/introduction)
  * Agents
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
  * [When to use text prompts (as opposed to the Flow Builder)](https://docs.vogent.ai/platform-overview/prompting-guide#when-to-use-text-prompts-as-opposed-to-the-flow-builder)
  * [Text Prompt Tips](https://docs.vogent.ai/platform-overview/prompting-guide#text-prompt-tips)
  * [Keywords](https://docs.vogent.ai/platform-overview/prompting-guide#keywords)
  * [Instructing Your Voice Agent](https://docs.vogent.ai/platform-overview/prompting-guide#instructing-your-voice-agent)
  * [Flow Builder Tips](https://docs.vogent.ai/platform-overview/prompting-guide#flow-builder-tips)


Platform Overview
# Prompting Guide
A guide to designing effective voice agents in Vogent
Prompting your way to a useful voice agent can be difficult. Here are some tips to make it easier.
### 
[​](https://docs.vogent.ai/platform-overview/prompting-guide#when-to-use-text-prompts-as-opposed-to-the-flow-builder)
When to use text prompts (as opposed to the Flow Builder)
Flow Builder models are a better fit for conversations that have structure, and that require passing through a number of known steps. For example:
  * Outbound surveys
  * Inbound lead/client handling

On the other hand, prompted agents perform well when you have a defined goal but the conversation is unstructured. They’re useful in more dynamic situations, in which you have an outcome to achieve but can’t anticipate the types of objections that might arise. Examples of this include:
  * Calling insurance to check on a claim
  * Calling airlines to book flights or add ancillaries
  * Calling small businesses to inquire about hours or check on orders


## 
[​](https://docs.vogent.ai/platform-overview/prompting-guide#text-prompt-tips)
Text Prompt Tips
### 
[​](https://docs.vogent.ai/platform-overview/prompting-guide#keywords)
Keywords
  * The `<|press:{number}|>` keyword will make the agent press a button on the phone (e.g. `<|press:1|>` will make the agent press the 1 key). If you use a letter (e.g. `<|press:a|>`), the agent will press the corresponding number using a keypad mapping.
  * The `<|hangup|>` keyword will make the agent hang up the call.


### 
[​](https://docs.vogent.ai/platform-overview/prompting-guide#instructing-your-voice-agent)
Instructing Your Voice Agent
There’s no single “right way” to prompt a voice agent, but we’ve found the most effective prompts (especially for the _Vogent Base Conversations_ model) follow a clear structure with specific components.
  * Start your prompt by clearly establishing the agent’s identity and the purpose of the call. This helps ground the agent in their role and mission:


> Your name is James Perez. You are calling an airline, `{{airline}}`, about a reservation for passenger `{{passenger_name}}` with confirmation number `{{confirmation_number}}`.
Next, provide specific, actionable objectives for the call. List exactly what information or actions the agent needs to accomplish:
> Ensure that during the call, you: Add checked baggage to the reservation Confirm the baggage fee amount Verify weight limits for checked bags Inquire about carry-on allowance Get a confirmation number for the baggage addition
Finally, add on specific instructions based on where the agent falls short on performing in testing.
> If asked for the confirmation number, you MUST give the FULL number (`{{confirmation_number}}`). Get a reference number for the baggage addition Confirm the exact fee amount Verify payment methods accepted Get baggage tracking information if provided
> Do not end the call until you have gathered ALL required information.
This structure ensures your agent stays focused on the task while maintaining natural conversation flow and gathering all necessary information.
## 
[​](https://docs.vogent.ai/platform-overview/prompting-guide#flow-builder-tips)
Flow Builder Tips
  * Clone an agent template (like our [quickstart Flow Agent](https://docs.vogent.ai/platform-overview/quickstart/flow-builder)) to get a sense of the structure of a complete flow agent.
  * Reference answers from past nodes using `@` to make questions more specific and/or personalized. For example, if you ask the respondent for their name in the initial question, referencing it in future questions can be a nice touch.
  * Preface questions with some sort of affirmative phrase (like “got it.”). It can be jarring when the agent moves into a new node after a response without some sort of acknowledgement.


[Billing](https://docs.vogent.ai/platform-overview/billing)[Overview](https://docs.vogent.ai/telephony/overview)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
