[Skip to main content](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Post-Call Analysis
Versioning and Evaluation
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
    * Post-Call Analysis
      * [Overview](https://docs.vogent.ai/platform-overview/agents/evaluation/overview)
      * [Extractors](https://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
      * [Dial History](https://docs.vogent.ai/platform-overview/agents/evaluation/dial-history)
      * [Versioning and Evaluation](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation)
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
  * [Accessing Model and Extractor Versions](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#accessing-model-and-extractor-versions)
  * [Creating a New Version](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#creating-a-new-version)
  * [Making a Version the Default](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#making-a-version-the-default)
  * [Testing Model and Extractor Versions](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#testing-model-and-extractor-versions)
  * [Testing Model Versions](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#testing-model-versions)
  * [Testing Extractor Versions](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#testing-extractor-versions)


Post-Call Analysis
# Versioning and Evaluation
Manage model and extractor versions
Iterating and evaluating is pivotal to building effective agents. Every agent’s model and extractor is versioned, allowing you to improve agents safely and evaluate them against past dials. The Vogent API’s support for versioning also allows you to roll out new agent versions carefully, making A/B testing etc. easier.
## 
[​](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#accessing-model-and-extractor-versions)
Accessing Model and Extractor Versions
All model and extractor versions can be found in the **Version** dropdown in your agent’s **Model** or **Extractor** tabs, respectively.
### 
[​](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#creating-a-new-version)
Creating a New Version
To create a new version, click the **Create Version** button in the **Version** dropdown, fill in the configuration for your model or extractor, and click **Save**.
### 
[​](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#making-a-version-the-default)
Making a Version the Default
To make a version the default, click the **Default** button under the **Version** dropdown.
Once you roll out a default version, all initiated calls without an otherwise specified version will use this version. To protect against regressions, we recommend testing new versions thoroughly before making them the default, and passing explicit version IDs when creating calls via the API.
## 
[​](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#testing-model-and-extractor-versions)
Testing Model and Extractor Versions
Vogent provides capabilities for testing model and extractor versions against past dials.
### 
[​](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#testing-model-versions)
Testing Model Versions
For more information on testing a model version against past dials, see [Counterfactuals](https://docs.vogent.ai/platform-overview/agents/evaluation/dial-history#counterfactuals).
### 
[​](https://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation#testing-extractor-versions)
Testing Extractor Versions
For more information on testing an extractor version against past dials, see [Extractor Testing](https://docs.vogent.ai/platform-overview/agents/evaluation/extractors#testing-extractors).
[Dial History](https://docs.vogent.ai/platform-overview/agents/evaluation/dial-history)[Voice Library](https://docs.vogent.ai/platform-overview/voices)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
