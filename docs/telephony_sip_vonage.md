[Skip to main content](http://docs.vogent.ai/telephony/sip/vonage#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Importing via SIP
Vonage SIP Import
[Guides](http://docs.vogent.ai/introduction)[API Reference](http://docs.vogent.ai/api-reference/introduction)[SDK](http://docs.vogent.ai/sdk/web-sdk)[Voicelab](http://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](http://docs.vogent.ai/introduction)
  * Quickstart


##### Platform Overview
  * [Introduction](http://docs.vogent.ai/platform-overview/introduction)
  * Agents
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
    * [SIP Trunking Overview](http://docs.vogent.ai/telephony/sip/overview)
    * [Twilio SIP Import](http://docs.vogent.ai/telephony/sip/twilio)
    * [Vonage SIP Import](http://docs.vogent.ai/telephony/sip/vonage)
    * [Telnyx SIP Import](http://docs.vogent.ai/telephony/sip/telnyx)
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
  * [For Outbound Calls](http://docs.vogent.ai/telephony/sip/vonage#for-outbound-calls)
  * [For Inbound Calls](http://docs.vogent.ai/telephony/sip/vonage#for-inbound-calls)


Importing via SIP
# Vonage SIP Import
Import a Vonage phone number into Vogent
Here are the steps to import a Vonage phone number into Vogent.
## 
[​](http://docs.vogent.ai/telephony/sip/vonage#for-outbound-calls)
For Outbound Calls
  1. Go to the Vonage Console and select SIP, under the Voice section.


![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/vonage-sip-trunks.png?fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=6a647b6661bf066160b8303ea0937aac)
  1. Click **Create New** , you should automatically be taken to the page where you can configure your SIP trunk.
  2. Click **Add Authentication** and create a new user key and secret, make sure to click the plus icon when you’re done, to add the credentials.


![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/vonage-sip-auth.png?fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=43ffc3183848ad739e25f19a92be0cba)
Make sure you leave the ACL field empty, as Vogent does not support a static range of IP addresses for outbound SIP calls outside of the enterprise plan. Please contact us if this is a security requirement for your use case.
  1. Copy one of the termination URIs that are shown. They should look something like `your-trunk-name.sip-us.vonage.com`.
  2. In Vogent, Go to the **Call Settings** tab in the left sidebar, and click **Import via SIP** , and enter the termination URI and credentials you created in steps 1-3. You may also do this using the [Create Number API](http://docs.vogent.ai/api-reference/create-number) with `type` set to `sip_import`.


![](https://mintcdn.com/elto-1/A2c2RA9tHzdkFUXP/images/sip-import-dialog-vogent.png?fit=max&auto=format&n=A2c2RA9tHzdkFUXP&q=85&s=2f2e631683a75c4e1db7186f2e6ae2fe)
  1. Click **Import** to create the number, and you should be able to use the number to make outbound calls.


## 
[​](http://docs.vogent.ai/telephony/sip/vonage#for-inbound-calls)
For Inbound Calls
  1. Make sure you complete the outbound SIP trunking steps first.
  2. Under the Inbound Calling section, go to the “Select Region” dropdown, and select the region you want to use for inbound calls. Then hit the save icon to save the changes.
  3. Under the “Add URI” section, enter “sip.vogent.ai” under URI, and click the plus icon.


![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/vonage-sip-inbound.png?fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=23df3e506291bd832398f0e4927f423f)
  1. Under the “Link Numbers” section, add the numbers you wish to use for inbound calls.
  2. Now, go to Vogent, and go to the **Numbers** tab under the Agent you want to use for this phone number, and link the phone number to the agent.


[Twilio SIP Import](http://docs.vogent.ai/telephony/sip/twilio)[Telnyx SIP Import](http://docs.vogent.ai/telephony/sip/telnyx)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
