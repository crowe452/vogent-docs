Post-Call Analysis

Extractors



    * Quickstart





    * Agents

        * Configuration

    * Model

    * Post-Call Analysis

                          * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      



  * [Creating an Extractor](#creating-an-extractor)
  * [General Settings](#general-settings)
  * [Extraction Fields](#extraction-fields)
  * [Testing Extractors](#testing-extractors)
  * [Managing Versions](#managing-versions)
  * [Best Practices](#best-practices)
  * [Technical Details](#technical-details)



Post-Call Analysis

# Extractors

Extract data after each call in a structured format

Extractors enable you to gather structured data after each call. You can then use this data to interface with your own systems or track performance over time. For example, in our quickstart guide’s [Restaurant Ordering Agent](/quickstart/inbound#retrieving-the-order-post-call), we use extractors to gather the customer’s name and order in a consistent format, which we can then use to e.g. hit a point-of-sale system’s API reliably. While you can view all extractor results in the UI, you can also use the [Dial Extractor webhook](/webhooks/dial-extractor) to send the data to your own systems after each call.

## 

[​](#creating-an-extractor)

Creating an Extractor

To create an extractor, navigate to your agent’s **Extractor** tab. Click the **Create New Version** dropdown to start defining a new extractor configuration.

![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/extractor-light.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=f0584ec5e2047e4c51b723d2d4484c3a)![](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/images/extractor-dark.png?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=b3861b9ce921ed757f24da27176fbd18)

### 

[​](#general-settings)

General Settings

Each extractor version needs a name that will be used to identify it in the UI.

### 

[​](#extraction-fields)

Extraction Fields

Extraction fields define the schema of data you want to capture from each call. To add a field:

1

Add a new field

Click the **Add Field** button

2

Name the field

Provide a name for the field

3

Select field type

Select the field type from the following options:

  * Text: For string values
  * Integer: For whole numbers
  * Float: For decimal numbers
  * Boolean: For true/false values
  * Custom: For complex or nested data structures (e.g. JSON objects)



4

Configure nullability

Toggle **Nullable** if the field is optional

5

Add description

Add a description to document the field’s purpose; this aids our extraction model in understanding the data you’re trying to capture in this field

If you’re using the _Custom_ field type to capture a JSON object, we recommend adding a description to each field within the object.

### 

[​](#testing-extractors)

Testing Extractors

You can test new extractor versions on past dials before deploying them. Once your extractor has been created:

1

Click Test

Make sure that you’ve created your extractor by hitting **Save** ; if you’re still on the extractor creation page, the **Test** button will not appear

2

Select Version

Select the extractor version that you’d like to test

3

Select Dial

Provide the Dial ID of the dial that you’d like to test against (check out the [Dial History](/platform-overview/agents/evaluation/dial-history) section to learn about browsing past dials)

4

Run Extractor

Click **Test** to run the extractor on this dial. It may take a few seconds to complete.

### 

[​](#managing-versions)

Managing Versions

Each extractor configuration is version-controlled. You can:

  * Create new versions to iterate on your extraction schema
  * Make a version the default by clicking **Make Default**
  * Test different versions to ensure they work as expected
  * View when versions were created and last updated



If you’re rolling out a new extractor version, double-check that it’s set as the default version.

## 

[​](#best-practices)

Best Practices

  * Give fields clear, descriptive names that reflect their purpose
  * Use appropriate field types to ensure data consistency
  * Add descriptions to document what each field represents
  * Test extractors thoroughly before making them the default version
  * Consider making fields nullable if they might not always be available. This prevents inconsistent empty value formats.



## 

[​](#technical-details)

Technical Details

Each extractor has a unique ID that can be used to reference it in your integration code. You can find this ID in the General section of your extractor configuration.

[Overview](/platform-overview/agents/evaluation/overview)[Dial History](/platform-overview/agents/evaluation/dial-history)