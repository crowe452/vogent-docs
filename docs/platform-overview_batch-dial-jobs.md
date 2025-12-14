Platform Overview

Batch Dial Jobs



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      



  * [Overview](#overview)
  * [Creating a Batch Dial Job](#creating-a-batch-dial-job)
  * [1. Prepare Your Data](#1-prepare-your-data)
  * [2. Create the Batch Job](#2-create-the-batch-job)
  * [3. Start the Job](#3-start-the-job)
  * [Managing Batch Jobs](#managing-batch-jobs)
  * [Check Job Status](#check-job-status)
  * [Update Job Configuration](#update-job-configuration)
  * [View Queued Dials](#view-queued-dials)
  * [Scheduling](#scheduling)
  * [Weekly Schedule Format](#weekly-schedule-format)
  * [Time Zone Support](#time-zone-support)
  * [Best Practices](#best-practices)
  * [Phone Number Pool](#phone-number-pool)
  * [Data Management](#data-management)
  * [Job Statuses](#job-statuses)



Platform Overview

# Batch Dial Jobs

Automate large-scale outbound calling campaigns with scheduled batch dial jobs

Batch dial jobs enable you to execute large-scale outbound calling campaigns by creating and managing multiple dials in batches. This feature is perfect for sales campaigns, customer surveys, appointment reminders, and other scenarios where you need to make hundreds or thousands of calls efficiently.

## 

[​](#overview)

Overview

A batch dial job consists of:

  * **Target phone numbers** : A list of phone numbers to call
  * **Agent configuration** : The AI agent that will handle the conversations
  * **Scheduling** : When the calls should be made
  * **Concurrency limits** : How many calls to make simultaneously (this may not exceed your workspace’s concurrent dial limit)
  * **Phone number pool** : Which of your phone numbers to use for outbound calls



## 

[​](#creating-a-batch-dial-job)

Creating a Batch Dial Job

### 

[​](#1-prepare-your-data)

1. Prepare Your Data

First, prepare a list of phone numbers and any associated data (like names, account numbers, etc.) that your agent will need during the calls.

Copy

```
`[ { "toNumber": "+1234567890", "inputs": { "customer_name": "John Doe", "account_id": "ACC123" } }, { "toNumber": "+1987654321", "inputs": { "customer_name": "Jane Smith", "account_id": "ACC456" } } ] `
```

### 

[​](#2-create-the-batch-job)

2. Create the Batch Job

Use the API to create your batch dial job:

Copy

```
`curl -X POST "https://api.vogent.ai/api/batch_dial_jobs" \ -H "Content-Type: application/json" \ -H "api_key: YOUR_API_KEY" \ -d '{ "name": "Customer Survey Campaign", "callAgentId": "your-agent-id", "maxConcurrentDials": 5, "fromPhoneNumberIds": ["your-phone-number-id"], "schedule": { "days": [ { "dayOfWeek": 1, "timeSlots": [ { "startTime": "09:00", "endTime": "17:00" } ] } ], "timezone": "America/New_York" }, "rows": [ { "toNumber": "+1234567890", "inputs": { "customer_name": "John Doe", "account_id": "ACC123" } } ] }' `
```

You may view your job in the Vogent UI by going to the _Batch Dials_ page.

### 

[​](#3-start-the-job)

3. Start the Job

Batch jobs are created in the `INIT` state. You must start them explicitly:

Copy

```
`curl -X POST "https://api.vogent.ai/api/batch_dial_jobs/{job-id}/paused" \ -H "Content-Type: application/json" \ -H "api_key: YOUR_API_KEY" \ -d '{"paused": false}' `
```

## 

[​](#managing-batch-jobs)

Managing Batch Jobs

### 

[​](#check-job-status)

Check Job Status

Monitor your batch job’s progress:

Copy

```
`curl -X GET "https://api.vogent.ai/api/batch_dial_jobs/{job-id}" \ -H "api_key: YOUR_API_KEY" `
```

Response includes:

  * Current status (`INIT`, `ACTIVE`, `PAUSED`, `COMPLETE`, `CANCELLED`)
  * Creation timestamp
  * Configuration details



### 

[​](#update-job-configuration)

Update Job Configuration

You may update an existing job’s settings, after it’s been created. The changes won’t apply until the workflow is paused.

Copy

```
`curl -X PUT "https://api.vogent.ai/api/batch_dial_jobs/{job-id}" \ -H "Content-Type: application/json" \ -H "api_key: YOUR_API_KEY" \ -d '{ "maxConcurrentDials": 10, "schedule": { "days": [ { "dayOfWeek": 1, "timeSlots": [ { "startTime": "09:00", "endTime": "18:00" } ] } ], "timezone": "America/New_York" } }' `
```

### 

[​](#view-queued-dials)

View Queued Dials

See all the rows that are queued to run on your batch job. This won’t show dials that have already completed or are in progress.

Copy

```
`curl -X GET "https://api.vogent.ai/api/batch_dial_jobs/{job-id}/queue" \ -H "api_key: YOUR_API_KEY" `
```

## 

[​](#scheduling)

Scheduling

Batch dial jobs support sophisticated scheduling to ensure calls are made at appropriate times:

### 

[​](#weekly-schedule-format)

Weekly Schedule Format

Copy

```
`{ "schedule": { "days": [ { "dayOfWeek": 1, // Monday (0=Sunday, 1=Monday, etc.) "timeSlots": [ { "startTime": "09:00", "endTime": "12:00" }, { "startTime": "13:00", "endTime": "17:00" } ] } ], "timezone": "America/New_York" } } `
```

### 

[​](#time-zone-support)

Time Zone Support

All schedules use the specified timezone. Common timezone values:

  * `America/New_York` - Eastern Time
  * `America/Chicago` - Central Time
  * `America/Denver` - Mountain Time
  * `America/Los_Angeles` - Pacific Time
  * `UTC` - Coordinated Universal Time



## 

[​](#best-practices)

Best Practices

### 

[​](#phone-number-pool)

Phone Number Pool

Use multiple phone numbers to increase call success rates and distribute call volume over multiple numbers.

### 

[​](#data-management)

Data Management

Structure your `inputs` data consistently:

  * Use the same field names across all rows
  * Include all data your agent prompt references
  * All your values must be strings



### 

[​](#job-statuses)

Job Statuses

Your job will go through the following statuses:

  * **INIT** : Job is just created and hasn’t been started yet
  * **ACTIVE** : Job is running normally
  * **PAUSED** : Job is temporarily stopped
  * **COMPLETE** : All dials have been attempted
  * **CANCELLED** : Job was manually stopped



[Live Dials](/platform-overview/live-dials)[API Settings](/platform-overview/api-settings)