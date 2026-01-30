[Skip to main content](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Model
Prompted Models
[Guides](https://docs.vogent.ai/introduction)[API Reference](https://docs.vogent.ai/api-reference/introduction)[SDK](https://docs.vogent.ai/sdk/web-sdk)[Voicelab](https://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](https://docs.vogent.ai/introduction)
  * Quickstart


##### Platform Overview
  * [Introduction](https://docs.vogent.ai/platform-overview/introduction)
  * Agents
    * [Overview](https://docs.vogent.ai/platform-overview/agents/overview)
    * Configuration
    * Model
      * [Overview](https://docs.vogent.ai/platform-overview/agents/model/overview)
      * [Prompted Models](https://docs.vogent.ai/platform-overview/agents/model/prompted-models)
      * [Flow Builder](https://docs.vogent.ai/platform-overview/agents/model/flow-builder)
      * [Fine Tuning](https://docs.vogent.ai/platform-overview/agents/model/fine-tuning)
    * Post-Call Analysis
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
  * [Key Features](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#key-features)
  * [Getting Started](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#getting-started)
  * [Choosing the Right Model](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#choosing-the-right-model)
  * [Third-Party Models](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#third-party-models)
  * [Vogent Base Conversations Model](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#vogent-base-conversations-model)
  * [Writing Effective Prompts](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#writing-effective-prompts)
  * [When to Use Prompted Models](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#when-to-use-prompted-models)
  * [Example Implementation](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#example-implementation)
  * [Next Steps](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#next-steps)


Model
# Prompted Models
Configure your agent’s conversational behavior using a prompt
Prompted models enable you to design conversational AI agents by providing detailed instructions about how they should behave and respond. This approach offers substantial flexibility while requiring minimal technical setup.
## 
[​](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#key-features)
Key Features
  * Support for third-party models like GPT and Vogent’s Base Conversations Model
  * Simple prompt-based configuration interface
  * Natural, context-aware conversations
  * Customizable agent personas and behaviors


## 
[​](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#getting-started)
Getting Started
To create a prompted model agent:
  1. Navigate to the Model tab in your agent configuration
  2. Select “Prompted Model” as your model type
  3. Choose your preferred model (GPT or Vogent Base Conversations)
  4. Write your prompt instructions
  5. Test and refine your agent’s responses


## 
[​](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#choosing-the-right-model)
Choosing the Right Model
### 
[​](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#third-party-models)
Third-Party Models
Vogent offers off-the-shelf models, like GPT-4o.
### 
[​](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#vogent-base-conversations-model)
Vogent Base Conversations Model
Our in-house model is specifically trained for conversational tasks and performs exceptionally well through prompting alone. It’s optimized for voice interactions and common conversation patterns.
## 
[​](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#writing-effective-prompts)
Writing Effective Prompts
For guidance on creating effective prompts, check out our [prompting guide](https://docs.vogent.ai/platform-overview/agents/model/prompted-models). The guide covers:
  * Best practices for prompt engineering
  * Template examples
  * Common patterns and anti-patterns
  * Optimization techniques


## 
[​](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#when-to-use-prompted-models)
When to Use Prompted Models
Prompted models are ideal for:
  * Open-ended conversations
  * Customer service interactions
  * Information gathering
  * General Q&A

For more structured interactions like surveys or form-filling, consider using our [Flow Builder](https://docs.vogent.ai/platform-overview/agents/model/flow-builder) instead.
## 
[​](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#example-implementation)
Example Implementation
The interface provides a straightforward way to configure your prompted model:
  1. Set your agent’s basic information (name, type)
  2. Choose your preferred model
  3. Write your prompt instructions
  4. Define opening lines and responses
  5. Configure any additional parameters

Your prompt should include clear instructions about the agent’s role, desired behavior, and any specific responses or patterns to follow.
## 
[​](https://docs.vogent.ai/platform-overview/agents/model/prompted-models#next-steps)
Next Steps
  * Explore our [prompting guide](https://docs.vogent.ai/platform-overview/agents/model/prompted-models) for detailed tips
  * Try different model types to find the best fit for your use case
  * Test your agent thoroughly with various user inputs
  * Iterate on your prompts based on actual conversation data


[Overview](https://docs.vogent.ai/platform-overview/agents/model/overview)[Flow Builder](https://docs.vogent.ai/platform-overview/agents/model/flow-builder)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
