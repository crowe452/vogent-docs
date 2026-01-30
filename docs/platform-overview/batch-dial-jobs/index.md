[Skip to main content](https://docs.vogent.ai/platform-overview/batch-dial-jobs#content-area)
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
Batch Dial Jobs
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
  * [Overview](https://docs.vogent.ai/platform-overview/batch-dial-jobs#overview)
  * [Creating a Batch Dial Job](https://docs.vogent.ai/platform-overview/batch-dial-jobs#creating-a-batch-dial-job)
  * [1. Prepare Your Data](https://docs.vogent.ai/platform-overview/batch-dial-jobs#1-prepare-your-data)
  * [2. Create the Batch Job](https://docs.vogent.ai/platform-overview/batch-dial-jobs#2-create-the-batch-job)
  * [3. Start the Job](https://docs.vogent.ai/platform-overview/batch-dial-jobs#3-start-the-job)
  * [Managing Batch Jobs](https://docs.vogent.ai/platform-overview/batch-dial-jobs#managing-batch-jobs)
  * [Check Job Status](https://docs.vogent.ai/platform-overview/batch-dial-jobs#check-job-status)
  * [Update Job Configuration](https://docs.vogent.ai/platform-overview/batch-dial-jobs#update-job-configuration)
  * [View Queued Dials](https://docs.vogent.ai/platform-overview/batch-dial-jobs#view-queued-dials)
  * [Scheduling](https://docs.vogent.ai/platform-overview/batch-dial-jobs#scheduling)
  * [Weekly Schedule Format](https://docs.vogent.ai/platform-overview/batch-dial-jobs#weekly-schedule-format)
  * [Time Zone Support](https://docs.vogent.ai/platform-overview/batch-dial-jobs#time-zone-support)
  * [Best Practices](https://docs.vogent.ai/platform-overview/batch-dial-jobs#best-practices)
  * [Phone Number Pool](https://docs.vogent.ai/platform-overview/batch-dial-jobs#phone-number-pool)
  * [Data Management](https://docs.vogent.ai/platform-overview/batch-dial-jobs#data-management)
  * [Job Statuses](https://docs.vogent.ai/platform-overview/batch-dial-jobs#job-statuses)


Platform Overview
# Batch Dial Jobs
Automate large-scale outbound calling campaigns with scheduled batch dial jobs
Batch dial jobs enable you to execute large-scale outbound calling campaigns by creating and managing multiple dials in batches. This feature is perfect for sales campaigns, customer surveys, appointment reminders, and other scenarios where you need to make hundreds or thousands of calls efficiently.
## 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#overview)
Overview
A batch dial job consists of:
  * **Target phone numbers** : A list of phone numbers to call
  * **Agent configuration** : The AI agent that will handle the conversations
  * **Scheduling** : When the calls should be made
  * **Concurrency limits** : How many calls to make simultaneously (this may not exceed your workspace’s concurrent dial limit)
  * **Phone number pool** : Which of your phone numbers to use for outbound calls


## 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#creating-a-batch-dial-job)
Creating a Batch Dial Job
### 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#1-prepare-your-data)
1. Prepare Your Data
First, prepare a list of phone numbers and any associated data (like names, account numbers, etc.) that your agent will need during the calls.
Copy
```
[
 {
  "toNumber": "+1234567890",
  "inputs": {
   "customer_name": "John Doe",
   "account_id": "ACC123"
  }
 },
 {
  "toNumber": "+1987654321",
  "inputs": {
   "customer_name": "Jane Smith",
   "account_id": "ACC456"
  }
 }
]

```

### 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#2-create-the-batch-job)
2. Create the Batch Job
Use the API to create your batch dial job:
Copy
```
curl -X POST "https://api.vogent.ai/api/batch_dial_jobs" \
 -H "Content-Type: application/json" \
 -H "api_key: YOUR_API_KEY" \
 -d '{
  "name": "Customer Survey Campaign",
  "callAgentId": "your-agent-id",
  "maxConcurrentDials": 5,
  "fromPhoneNumberIds": ["your-phone-number-id"],
  "schedule": {
   "days": [
    {
     "dayOfWeek": 1,
     "timeSlots": [
      {
       "startTime": "09:00",
       "endTime": "17:00"
      }
     ]
    }
   ],
   "timezone": "America/New_York"
  },
  "rows": [
   {
    "toNumber": "+1234567890",
    "inputs": {
     "customer_name": "John Doe",
     "account_id": "ACC123"
    }
   }
  ]
 }'

```

You may view your job in the Vogent UI by going to the _Batch Dials_ page.
### 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#3-start-the-job)
3. Start the Job
Batch jobs are created in the `INIT` state. You must start them explicitly:
Copy
```
curl -X POST "https://api.vogent.ai/api/batch_dial_jobs/{job-id}/paused" \
 -H "Content-Type: application/json" \
 -H "api_key: YOUR_API_KEY" \
 -d '{"paused": false}'

```

## 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#managing-batch-jobs)
Managing Batch Jobs
### 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#check-job-status)
Check Job Status
Monitor your batch job’s progress:
Copy
```
curl -X GET "https://api.vogent.ai/api/batch_dial_jobs/{job-id}" \
 -H "api_key: YOUR_API_KEY"

```

Response includes:
  * Current status (`INIT`, `ACTIVE`, `PAUSED`, `COMPLETE`, `CANCELLED`)
  * Creation timestamp
  * Configuration details


### 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#update-job-configuration)
Update Job Configuration
You may update an existing job’s settings, after it’s been created. The changes won’t apply until the workflow is paused.
Copy
```
curl -X PUT "https://api.vogent.ai/api/batch_dial_jobs/{job-id}" \
 -H "Content-Type: application/json" \
 -H "api_key: YOUR_API_KEY" \
 -d '{
  "maxConcurrentDials": 10,
  "schedule": {
   "days": [
    {
     "dayOfWeek": 1,
     "timeSlots": [
      {
       "startTime": "09:00",
       "endTime": "18:00"
      }
     ]
    }
   ],
   "timezone": "America/New_York"
  }
 }'

```

### 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#view-queued-dials)
View Queued Dials
See all the rows that are queued to run on your batch job. This won’t show dials that have already completed or are in progress.
Copy
```
curl -X GET "https://api.vogent.ai/api/batch_dial_jobs/{job-id}/queue" \
 -H "api_key: YOUR_API_KEY"

```

## 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#scheduling)
Scheduling
Batch dial jobs support sophisticated scheduling to ensure calls are made at appropriate times:
### 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#weekly-schedule-format)
Weekly Schedule Format
Copy
```
{
 "schedule": {
  "days": [
   {
    "dayOfWeek": 1, // Monday (0=Sunday, 1=Monday, etc.)
    "timeSlots": [
     {
      "startTime": "09:00",
      "endTime": "12:00"
     },
     {
      "startTime": "13:00",
      "endTime": "17:00"
     }
    ]
   }
  ],
  "timezone": "America/New_York"
 }
}

```

### 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#time-zone-support)
Time Zone Support
All schedules use the specified timezone. Common timezone values:
  * `America/New_York` - Eastern Time
  * `America/Chicago` - Central Time
  * `America/Denver` - Mountain Time
  * `America/Los_Angeles` - Pacific Time
  * `UTC` - Coordinated Universal Time


## 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#best-practices)
Best Practices
### 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#phone-number-pool)
Phone Number Pool
Use multiple phone numbers to increase call success rates and distribute call volume over multiple numbers.
### 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#data-management)
Data Management
Structure your `inputs` data consistently:
  * Use the same field names across all rows
  * Include all data your agent prompt references
  * All your values must be strings


### 
[​](https://docs.vogent.ai/platform-overview/batch-dial-jobs#job-statuses)
Job Statuses
Your job will go through the following statuses:
  * **INIT** : Job is just created and hasn’t been started yet
  * **ACTIVE** : Job is running normally
  * **PAUSED** : Job is temporarily stopped
  * **COMPLETE** : All dials have been attempted
  * **CANCELLED** : Job was manually stopped


[Live Dials](https://docs.vogent.ai/platform-overview/live-dials)[API Settings](https://docs.vogent.ai/platform-overview/api-settings)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
