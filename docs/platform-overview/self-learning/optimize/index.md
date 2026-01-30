[Skip to main content](https://docs.vogent.ai/platform-overview/self-learning/optimize#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Self Learning
Optimize Agents
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
  * [Setting up optimization](https://docs.vogent.ai/platform-overview/self-learning/optimize#setting-up-optimization)
  * [Creating an evaluation](https://docs.vogent.ai/platform-overview/self-learning/optimize#creating-an-evaluation)
  * [Optimizing the agent](https://docs.vogent.ai/platform-overview/self-learning/optimize#optimizing-the-agent)
  * [Select dials](https://docs.vogent.ai/platform-overview/self-learning/optimize#select-dials)
  * [Review the optimized model](https://docs.vogent.ai/platform-overview/self-learning/optimize#review-the-optimized-model)


Self Learning
# Optimize Agents
Optimize performance based on historical dials and simulations
## 
[​](https://docs.vogent.ai/platform-overview/self-learning/optimize#setting-up-optimization)
Setting up optimization
Before you can optimize an agent, you’ll need to have an evaluation set up. This lets you get more granular about success/failure cases of your model, and lets us feed this feedback into the training process.
### 
[​](https://docs.vogent.ai/platform-overview/self-learning/optimize#creating-an-evaluation)
Creating an evaluation
To create an evaluation, navigate to the **Evaluations** tab on the left sidebar and click the **New Eval** button on the top right.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/eval-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=c96b6cfed455c897fc9ca683b84baac2)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/eval-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=93295b799b67cf5e902a10596084a676)
You want to be as explicit as possible about important success/failure cases of your model, in order to let Vogent know how to judge a call. We can also automatically generate eval criteria based on the talk track and recordings you upload, though we recommend you review the generated criteria and make sure it aligns with your use case.
### 
[​](https://docs.vogent.ai/platform-overview/self-learning/optimize#optimizing-the-agent)
Optimizing the agent
Once you’ve created an evaluation, you can optimize the agent by clicking the “Optimize” button next to the prompt.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/optimize-prompt-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=fe4a819a15cb004a06665e1447ab4e41)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/optimize-prompt-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=3de31c7f06dca0093bf668bf4f3d21ed)
### 
[​](https://docs.vogent.ai/platform-overview/self-learning/optimize#select-dials)
Select dials
You should select the dials you want to use as an optimization target. We evaluate the performance of the model on those historical dials, and use that feedback to train the model. We will generally keep the prompt the same, and only train the model weights, so you should make sure there aren’t any obvious oversights in the prompts that may be causing the issues, or explicitly indicate you want us to optimize the prompt, and not the model weights.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/optimize-modal-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=b67705c266a1522c2eed962851847c95)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/optimize-modal-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=b4f4b0e7e438d427c0d8cb29aa77221e)
You should select a dataset of approximately 100 dials.
### 
[​](https://docs.vogent.ai/platform-overview/self-learning/optimize#review-the-optimized-model)
Review the optimized model
The model will automatically evaluate the version you selected and train on the selected dials. The new version will be created in under the agent, and you can use our standard tools to test the version and evaluate the performance, like Counterfactuals and Evaluation.
[Auto-Create Agents](https://docs.vogent.ai/platform-overview/self-learning/create)[Create Dial](https://docs.vogent.ai/developers/webhooks/create-dial)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
