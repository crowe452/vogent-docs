[Skip to main content](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Post-Call Analysis
Extractors
[Guides](http://docs.vogent.ai/introduction)[API Reference](http://docs.vogent.ai/api-reference/introduction)[SDK](http://docs.vogent.ai/sdk/web-sdk)[Voicelab](http://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](http://docs.vogent.ai/introduction)
  * Quickstart


##### Platform Overview
  * [Introduction](http://docs.vogent.ai/platform-overview/introduction)
  * Agents
    * [Overview](http://docs.vogent.ai/platform-overview/agents/overview)
    * Configuration
    * Model
    * Post-Call Analysis
      * [Overview](http://docs.vogent.ai/platform-overview/agents/evaluation/overview)
      * [Extractors](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
      * [Dial History](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history)
      * [Versioning and Evaluation](http://docs.vogent.ai/platform-overview/agents/evaluation/versioning-and-evaluation)
  * Voices
  * Tools
  * [Live Dials](http://docs.vogent.ai/platform-overview/live-dials)
  * [Batch Dial Jobs](http://docs.vogent.ai/platform-overview/batch-dial-jobs)
  * [API Settings](http://docs.vogent.ai/platform-overview/api-settings)
  * [Team](http://docs.vogent.ai/platform-overview/team)
  * [Billing](http://docs.vogent.ai/platform-overview/billing)
  * [Prompting Guide](http://docs.vogent.ai/platform-overview/prompting-guide)


##### Phone Numbers
  * [Overview](http://docs.vogent.ai/telephony/overview)
  * Importing via SIP
  * [Using a SIP Domain](http://docs.vogent.ai/telephony/sip-domain/overview)


##### Self Learning
  * [Self Learning Overview](http://docs.vogent.ai/platform-overview/self-learning/overview)
  * [Auto-Create Agents](http://docs.vogent.ai/platform-overview/self-learning/create)
  * [Optimize Agents](http://docs.vogent.ai/platform-overview/self-learning/optimize)


##### For Developers
  * Webhooks
  * [Dials and Dial Sessions](http://docs.vogent.ai/developers/dials-dialsessions)
  * [Dials Statuses](http://docs.vogent.ai/developers/dial-statuses)
  * [Flow Builder Schemas](http://docs.vogent.ai/developers/schemas)


On this page
  * [Creating an Extractor](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#creating-an-extractor)
  * [General Settings](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#general-settings)
  * [Extraction Fields](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#extraction-fields)
  * [Testing Extractors](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#testing-extractors)
  * [Managing Versions](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#managing-versions)
  * [Best Practices](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#best-practices)
  * [Technical Details](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#technical-details)


Post-Call Analysis
# Extractors
Extract data after each call in a structured format
Extractors enable you to gather structured data after each call. You can then use this data to interface with your own systems or track performance over time. For example, in our quickstart guide’s [Restaurant Ordering Agent](http://docs.vogent.ai/quickstart/inbound#retrieving-the-order-post-call), we use extractors to gather the customer’s name and order in a consistent format, which we can then use to e.g. hit a point-of-sale system’s API reliably. While you can view all extractor results in the UI, you can also use the [Dial Extractor webhook](http://docs.vogent.ai/webhooks/dial-extractor) to send the data to your own systems after each call.
## 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#creating-an-extractor)
Creating an Extractor
To create an extractor, navigate to your agent’s **Extractor** tab. Click the **Create New Version** dropdown to start defining a new extractor configuration.
![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/extractor-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=f0584ec5e2047e4c51b723d2d4484c3a)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/extractor-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=b3861b9ce921ed757f24da27176fbd18)
### 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#general-settings)
General Settings
Each extractor version needs a name that will be used to identify it in the UI.
### 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#extraction-fields)
Extraction Fields
Extraction fields define the schema of data you want to capture from each call. To add a field:
1
[](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
Add a new field
Click the **Add Field** button
2
[](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
Name the field
Provide a name for the field
3
[](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
Select field type
Select the field type from the following options:
  * Text: For string values
  * Integer: For whole numbers
  * Float: For decimal numbers
  * Boolean: For true/false values
  * Custom: For complex or nested data structures (e.g. JSON objects)


4
[](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
Configure nullability
Toggle **Nullable** if the field is optional
5
[](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
Add description
Add a description to document the field’s purpose; this aids our extraction model in understanding the data you’re trying to capture in this field
If you’re using the _Custom_ field type to capture a JSON object, we recommend adding a description to each field within the object.
### 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#testing-extractors)
Testing Extractors
You can test new extractor versions on past dials before deploying them. Once your extractor has been created:
1
[](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
Click Test
Make sure that you’ve created your extractor by hitting **Save** ; if you’re still on the extractor creation page, the **Test** button will not appear
2
[](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
Select Version
Select the extractor version that you’d like to test
3
[](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
Select Dial
Provide the Dial ID of the dial that you’d like to test against (check out the [Dial History](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history) section to learn about browsing past dials)
4
[](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors)
Run Extractor
Click **Test** to run the extractor on this dial. It may take a few seconds to complete.
### 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#managing-versions)
Managing Versions
Each extractor configuration is version-controlled. You can:
  * Create new versions to iterate on your extraction schema
  * Make a version the default by clicking **Make Default**
  * Test different versions to ensure they work as expected
  * View when versions were created and last updated


If you’re rolling out a new extractor version, double-check that it’s set as the default version.
## 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#best-practices)
Best Practices
  * Give fields clear, descriptive names that reflect their purpose
  * Use appropriate field types to ensure data consistency
  * Add descriptions to document what each field represents
  * Test extractors thoroughly before making them the default version
  * Consider making fields nullable if they might not always be available. This prevents inconsistent empty value formats.


## 
[​](http://docs.vogent.ai/platform-overview/agents/evaluation/extractors#technical-details)
Technical Details
Each extractor has a unique ID that can be used to reference it in your integration code. You can find this ID in the General section of your extractor configuration.
[Overview](http://docs.vogent.ai/platform-overview/agents/evaluation/overview)[Dial History](http://docs.vogent.ai/platform-overview/agents/evaluation/dial-history)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
