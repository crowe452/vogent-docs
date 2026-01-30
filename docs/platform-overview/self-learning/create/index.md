[Skip to main content](https://docs.vogent.ai/platform-overview/self-learning/create#content-area)
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
Auto-Create Agents
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
  * [Creating a new agent](https://docs.vogent.ai/platform-overview/self-learning/create#creating-a-new-agent)
  * [Guidelines for Recordings/Transcripts](https://docs.vogent.ai/platform-overview/self-learning/create#guidelines-for-recordings%2Ftranscripts)
  * [PII](https://docs.vogent.ai/platform-overview/self-learning/create#pii)
  * [Human Agent Accuracy](https://docs.vogent.ai/platform-overview/self-learning/create#human-agent-accuracy)
  * [Recordings vs Transcripts](https://docs.vogent.ai/platform-overview/self-learning/create#recordings-vs-transcripts)
  * [Data Size](https://docs.vogent.ai/platform-overview/self-learning/create#data-size)
  * [Guidelines for Talk Tracks](https://docs.vogent.ai/platform-overview/self-learning/create#guidelines-for-talk-tracks)


Self Learning
# Auto-Create Agents
Create agents from recordings and talk tracks
## 
[​](https://docs.vogent.ai/platform-overview/self-learning/create#creating-a-new-agent)
Creating a new agent
To create a new auto-designing agent, navigate to the **Agents** tab on the left sidebar and click the **New Agent** button on the top right. Then, you should select the “Self Design” tab.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/auto-create-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=e31bd3308a3642af9445ba149404b15e)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/auto-create-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=c29b817debae90944c76e4081b10b2c6)
You can then upload recordings and talk tracks that correspond to the agent you want to create.
## 
[​](https://docs.vogent.ai/platform-overview/self-learning/create#guidelines-for-recordings/transcripts)
Guidelines for Recordings/Transcripts
Our self-learning system works in two stages: we first use the scripts and recordings you provide us to generate an optimal prompt for the agent, then, we run simulations to optimize the model itself to fit your use case more closely. This helps make your agent less likely to hallucinate, and perform the task more effectively. To optimize the performance of the system, there are a few guidelines you should follow when uploading data into Vogent:
### 
[​](https://docs.vogent.ai/platform-overview/self-learning/create#pii)
PII
We attempt to strip out any PII from the transcripts and recordings you upload to prevent any potential data leakage into your model and prompts. If you have anonymized recordings or transcripts, however, you should upload those to Vogent instead. If you have sensitive use cases (e.g. use cases with PHI), please contact us before uploading any data that may be covered under HIPAA, etc.
### 
[​](https://docs.vogent.ai/platform-overview/self-learning/create#human-agent-accuracy)
Human Agent Accuracy
You don’t have to necessarily upload recordings in which the human agents perform perfectly — we pre-process transcripts to remove instances of humans making one-off errors, so this behavior doesn’t affect the agent. However, the recordings must be generally representative of the task being performed successfully; you shouldn’t have a large number of failed tasks, or off-topic conversations in the recordings.
### 
[​](https://docs.vogent.ai/platform-overview/self-learning/create#recordings-vs-transcripts)
Recordings vs Transcripts
We train models on the text level, so if you upload recordings, they will be converted into transcripts on our backend. If you have transcripts, you should upload those instead of recordings, since this will speed up the design process.
### 
[​](https://docs.vogent.ai/platform-overview/self-learning/create#data-size)
Data Size
For best results we suggest uploading as many transcripts/recordings as possible, but we’ve seen good results with as few as 100 recordings. The smaller your dataset, the less representative it may be of all the scenarios we may encounter in real calls, however.
## 
[​](https://docs.vogent.ai/platform-overview/self-learning/create#guidelines-for-talk-tracks)
Guidelines for Talk Tracks
Recordings and transcripts are the gold standard for data, however, we can work with talk tracks and training material if necessary. You should upload data in .pdf, .md, or .txt format. If you have your data in other formats, and cannot convert them, please contact us.
[Self Learning Overview](https://docs.vogent.ai/platform-overview/self-learning/overview)[Optimize Agents](https://docs.vogent.ai/platform-overview/self-learning/optimize)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
