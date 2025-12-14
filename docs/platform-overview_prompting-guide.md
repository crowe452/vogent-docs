Platform Overview

Prompting Guide



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      



  * [When to use text prompts (as opposed to the Flow Builder)](#when-to-use-text-prompts-as-opposed-to-the-flow-builder)
  * [Text Prompt Tips](#text-prompt-tips)
  * [Keywords](#keywords)
  * [Instructing Your Voice Agent](#instructing-your-voice-agent)
  * [Flow Builder Tips](#flow-builder-tips)



Platform Overview

# Prompting Guide

A guide to designing effective voice agents in Vogent

Prompting your way to a useful voice agent can be difficult. Here are some tips to make it easier.

### 

[​](#when-to-use-text-prompts-as-opposed-to-the-flow-builder)

When to use text prompts (as opposed to the Flow Builder)

Flow Builder models are a better fit for conversations that have structure, and that require passing through a number of known steps. For example:

  * Outbound surveys
  * Inbound lead/client handling

On the other hand, prompted agents perform well when you have a defined goal but the conversation is unstructured. They’re useful in more dynamic situations, in which you have an outcome to achieve but can’t anticipate the types of objections that might arise. Examples of this include:

  * Calling insurance to check on a claim
  * Calling airlines to book flights or add ancillaries
  * Calling small businesses to inquire about hours or check on orders



## 

[​](#text-prompt-tips)

Text Prompt Tips

### 

[​](#keywords)

Keywords

  * The `<|press:{number}|>` keyword will make the agent press a button on the phone (e.g. `<|press:1|>` will make the agent press the 1 key). If you use a letter (e.g. `<|press:a|>`), the agent will press the corresponding number using a keypad mapping.
  * The `<|hangup|>` keyword will make the agent hang up the call.



### 

[​](#instructing-your-voice-agent)

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

[​](#flow-builder-tips)

Flow Builder Tips

  * Clone an agent template (like our [quickstart Flow Agent](quickstart/flow-builder)) to get a sense of the structure of a complete flow agent.
  * Reference answers from past nodes using `@` to make questions more specific and/or personalized. For example, if you ask the respondent for their name in the initial question, referencing it in future questions can be a nice touch.
  * Preface questions with some sort of affirmative phrase (like “got it.”). It can be jarring when the agent moves into a new node after a response without some sort of acknowledgement.



[Billing](/platform-overview/billing)[Overview](/telephony/overview)