Post-Call Analysis

Versioning and Evaluation



    * Quickstart





    * Agents

        * Configuration

    * Model

    * Post-Call Analysis

                          * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      



  * [Accessing Model and Extractor Versions](#accessing-model-and-extractor-versions)
  * [Creating a New Version](#creating-a-new-version)
  * [Making a Version the Default](#making-a-version-the-default)
  * [Testing Model and Extractor Versions](#testing-model-and-extractor-versions)
  * [Testing Model Versions](#testing-model-versions)
  * [Testing Extractor Versions](#testing-extractor-versions)



Post-Call Analysis

# Versioning and Evaluation

Manage model and extractor versions

Iterating and evaluating is pivotal to building effective agents. Every agent’s model and extractor is versioned, allowing you to improve agents safely and evaluate them against past dials. The Vogent API’s support for versioning also allows you to roll out new agent versions carefully, making A/B testing etc. easier.

## 

[​](#accessing-model-and-extractor-versions)

Accessing Model and Extractor Versions

All model and extractor versions can be found in the **Version** dropdown in your agent’s **Model** or **Extractor** tabs, respectively.

### 

[​](#creating-a-new-version)

Creating a New Version

To create a new version, click the **Create Version** button in the **Version** dropdown, fill in the configuration for your model or extractor, and click **Save**.

### 

[​](#making-a-version-the-default)

Making a Version the Default

To make a version the default, click the **Default** button under the **Version** dropdown.

Once you roll out a default version, all initiated calls without an otherwise specified version will use this version. To protect against regressions, we recommend testing new versions thoroughly before making them the default, and passing explicit version IDs when creating calls via the API.

## 

[​](#testing-model-and-extractor-versions)

Testing Model and Extractor Versions

Vogent provides capabilities for testing model and extractor versions against past dials.

### 

[​](#testing-model-versions)

Testing Model Versions

For more information on testing a model version against past dials, see [Counterfactuals](/platform-overview/agents/evaluation/dial-history#counterfactuals).

### 

[​](#testing-extractor-versions)

Testing Extractor Versions

For more information on testing an extractor version against past dials, see [Extractor Testing](/platform-overview/agents/evaluation/extractors#testing-extractors).

[Dial History](/platform-overview/agents/evaluation/dial-history)[Voice Library](/platform-overview/voices)