[Skip to main content](https://docs.vogent.ai/telephony/overview#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Phone Numbers
Overview
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
  * [Creating and Managing Phone Numbers](https://docs.vogent.ai/telephony/overview#creating-and-managing-phone-numbers)
  * [Creating a Vogent-Managed Phone Number](https://docs.vogent.ai/telephony/overview#creating-a-vogent-managed-phone-number)
  * [Managing Phone Numbers](https://docs.vogent.ai/telephony/overview#managing-phone-numbers)
  * [Recordings](https://docs.vogent.ai/telephony/overview#recordings)
  * [Use your own carrier/numbers](https://docs.vogent.ai/telephony/overview#use-your-own-carrier%2Fnumbers)


Phone Numbers
# Overview
Overview of the Telephony features in Vogent
To manage phone numbers and telephony settings, visit the **Call Settings** tab in the left sidebar.
## 
[​](https://docs.vogent.ai/telephony/overview#creating-and-managing-phone-numbers)
Creating and Managing Phone Numbers
### 
[​](https://docs.vogent.ai/telephony/overview#creating-a-vogent-managed-phone-number)
Creating a Vogent-Managed Phone Number
To create a phone number, go to the **Numbers** tab and click **Add Phone Number**. Select a country code from the dropdown, enter an area code, and click the magnifying glass button. If we have numbers available for the area code you selected, you’ll see a list of available numbers. Click **Add** to add the number to your workspace.
Based on demand, we may not have numbers available for every area code. If you can’t find a number in the area code you want, try adjacent area codes; usually at least one area code in a region will be available.
Vogent supports US, Canadian (also under the US country code), and UK numbers in the self-serve product. If you need a different country, contact us or reach out on the Discord.
### 
[​](https://docs.vogent.ai/telephony/overview#managing-phone-numbers)
Managing Phone Numbers
Vogent allows you to **Spam Check** and **Remove** phone numbers by clicking the appropriate buttons next to the numbers. Spam checking a number will determine if any carrier/manufacturer has flagged the number as spam by dialing through a grid of cell phones across carriers and manufacturers. This process can take up to 6 hours; if your number is flagged as spam, an alert icon will appear next to the number.
You may perform up to 20 spam checks per month.
## 
[​](https://docs.vogent.ai/telephony/overview#recordings)
Recordings
If you are not notifying counterparties that you are recording calls, we advise filling out the _Banned Area Codes_ field under the **Recordings** tab with the following area codes to comply with two-party consent laws:
Two-Party Consent Area Codes
Copy
```
209, 213, 310, 323, 408, 415, 424, 442, 510, 530, 559, 562, 619, 626, 650, 657, 661, 669, 707, 714, 747, 760, 805, 818, 831, 858, 909, 916, 925, 949, 951, 203, 475, 860, 959, 239, 305, 321, 324, 352, 386, 407, 448, 561, 645, 656, 689, 727, 728, 754, 772, 786, 813, 850, 863, 904, 941, 954, 808, 217, 224, 309, 312, 331, 447, 464, 618, 630, 708, 773, 779, 815, 847, 861, 872, 240, 301, 410, 443, 667, 339, 351, 413, 508, 617, 774, 781, 857, 978, 231, 248, 269, 313, 517, 586, 616, 679, 734, 810, 906, 947, 989, 406, 702, 725, 775, 603, 215, 223, 267, 272, 412, 445, 484, 570, 582, 610, 717, 724, 814, 878, 206, 253, 360, 425, 509, 564

```

Don’t forget to click **Save** to save your changes.
## 
[​](https://docs.vogent.ai/telephony/overview#use-your-own-carrier/numbers)
Use your own carrier/numbers
Vogent supports using SIP trunking to connect your own carrier/numbers to Vogent.
## [SIP Trunking OverviewOverview of SIP trunking in Vogent.](https://docs.vogent.ai/telephony/sip-trunking)
[Prompting Guide](https://docs.vogent.ai/platform-overview/prompting-guide)[SIP Trunking Overview](https://docs.vogent.ai/telephony/sip/overview)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
