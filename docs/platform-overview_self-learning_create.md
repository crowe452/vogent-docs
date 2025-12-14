Self Learning

Auto-Create Agents



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      



  * [Creating a new agent](#creating-a-new-agent)
  * [Guidelines for Recordings/Transcripts](#guidelines-for-recordings%2Ftranscripts)
  * [PII](#pii)
  * [Human Agent Accuracy](#human-agent-accuracy)
  * [Recordings vs Transcripts](#recordings-vs-transcripts)
  * [Data Size](#data-size)
  * [Guidelines for Talk Tracks](#guidelines-for-talk-tracks)



Self Learning

# Auto-Create Agents

Create agents from recordings and talk tracks

## 

[​](#creating-a-new-agent)

Creating a new agent

To create a new auto-designing agent, navigate to the **Agents** tab on the left sidebar and click the **New Agent** button on the top right. Then, you should select the “Self Design” tab.

![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/auto-create-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=e31bd3308a3642af9445ba149404b15e)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/auto-create-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=c29b817debae90944c76e4081b10b2c6)

You can then upload recordings and talk tracks that correspond to the agent you want to create.

## 

[​](#guidelines-for-recordings/transcripts)

Guidelines for Recordings/Transcripts

Our self-learning system works in two stages: we first use the scripts and recordings you provide us to generate an optimal prompt for the agent, then, we run simulations to optimize the model itself to fit your use case more closely. This helps make your agent less likely to hallucinate, and perform the task more effectively. To optimize the performance of the system, there are a few guidelines you should follow when uploading data into Vogent:

### 

[​](#pii)

PII

We attempt to strip out any PII from the transcripts and recordings you upload to prevent any potential data leakage into your model and prompts. If you have anonymized recordings or transcripts, however, you should upload those to Vogent instead. If you have sensitive use cases (e.g. use cases with PHI), please contact us before uploading any data that may be covered under HIPAA, etc.

### 

[​](#human-agent-accuracy)

Human Agent Accuracy

You don’t have to necessarily upload recordings in which the human agents perform perfectly — we pre-process transcripts to remove instances of humans making one-off errors, so this behavior doesn’t affect the agent. However, the recordings must be generally representative of the task being performed successfully; you shouldn’t have a large number of failed tasks, or off-topic conversations in the recordings.

### 

[​](#recordings-vs-transcripts)

Recordings vs Transcripts

We train models on the text level, so if you upload recordings, they will be converted into transcripts on our backend. If you have transcripts, you should upload those instead of recordings, since this will speed up the design process.

### 

[​](#data-size)

Data Size

For best results we suggest uploading as many transcripts/recordings as possible, but we’ve seen good results with as few as 100 recordings. The smaller your dataset, the less representative it may be of all the scenarios we may encounter in real calls, however.

## 

[​](#guidelines-for-talk-tracks)

Guidelines for Talk Tracks

Recordings and transcripts are the gold standard for data, however, we can work with talk tracks and training material if necessary. You should upload data in .pdf, .md, or .txt format. If you have your data in other formats, and cannot convert them, please contact us.

[Self Learning Overview](/platform-overview/self-learning/overview)[Optimize Agents](/platform-overview/self-learning/optimize)