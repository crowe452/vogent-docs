Post-Call Analysis

Dial History



    * Quickstart





    * Agents

        * Configuration

    * Model

    * Post-Call Analysis

                          * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      



  * [Viewing Dial History](#viewing-dial-history)
  * [Analyzing Individual Dials](#analyzing-individual-dials)
  * [Transcript](#transcript)
  * [Results](#results)
  * [Invocation](#invocation)
  * [Counterfactuals](#counterfactuals)
  * [Filtering and Navigation](#filtering-and-navigation)
  * [Exporting Data](#exporting-data)



Post-Call Analysis

# Dial History

View and analyze past dials

The Dial History page allows you to review all past calls made to and from your agent. You can access detailed information about each call, including recordings, transcripts, and extracted results. You can also use the Counterfactuals feature to test how different versions of your agent would have handled past conversations.

## 

[​](#viewing-dial-history)

Viewing Dial History

There are two ways to view dial history:

  1. Navigate to your agent’s **Dials** tab to view all calls to/from the agent.
  2. Click the **Dial History** button on the left sidebar to view dial history across agents.



## 

[​](#analyzing-individual-dials)

Analyzing Individual Dials

Click on any dial to view its detailed information.

### 

[​](#transcript)

Transcript

The transcript tab shows the complete conversation between the user and your AI agent. Each message is labeled with the speaker (Human/AI) and displayed chronologically. You can click on any Human line to jump to the corresponding timestamp in the recording.

### 

[​](#results)

Results

The **Results** tab provides:

  * Completion reason (e.g., “User Hung Up”)
  * Extractor results (if any extractors were configured)
  * Option to add comments for team collaboration



### 

[​](#invocation)

Invocation

The **Invocation** tab displays:

  * Agent information
  * Agent version used for the call
  * The inputs provided for this call’s invocation



## 

[​](#counterfactuals)

Counterfactuals

The **Run Counterfactual** feature lets you test how different versions of your agent would handle past conversations:

1

Select Version

Choose the prompt version you want to test from the dropdown menu

2

Run Test

Click the “Run” button to simulate how that version would have responded

3

Review Results

Compare the counterfactual responses with the original conversation

This feature is particularly useful when:

  * Evaluating new agent versions before deployment
  * Debugging conversation flows
  * Training and improving your agent’s responses



The **Run Counterfactual** feature runs by passing your model version the dial transcript up to the point of the counterfactual and outputting the response at that point. This isn’t a fully accurate simulation of the conversation (as we can’t simulate the counterparty’s response to your tested model’s output), but it can still be useful for testing your model against specific problematic scenarios.

## 

[​](#filtering-and-navigation)

Filtering and 
Use the Filters menu to:

  * Search for specific dials
  * Filter by date range
  * Filter by call outcome
  * Filter by phone number or connection type



## 

[​](#exporting-data)

Exporting Data

Click the **Export** button to download dial history.

[Extractors](/platform-overview/agents/evaluation/extractors)[Versioning and Evaluation](/platform-overview/agents/evaluation/versioning-and-evaluation)