[Skip to main content](http://docs.vogent.ai/telephony/sip/twilio#content-area)
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
Twilio SIP Import
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
  * [For Outbound Calls](http://docs.vogent.ai/telephony/sip/twilio#for-outbound-calls)
  * [For Inbound Calls](http://docs.vogent.ai/telephony/sip/twilio#for-inbound-calls)


Importing via SIP
# Twilio SIP Import
Import a Twilio phone number into Vogent
Here are the steps to import a Twilio phone number into Vogent.
## 
[​](http://docs.vogent.ai/telephony/sip/twilio#for-outbound-calls)
For Outbound Calls
  1. Go to the Twilio Console and search for “Elastic SIP Trunks,” and navigate to the page.


![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/twilio-elastic-sip-trunks.png?fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=c4c78818759d19471ee77838cb2f943e)
  1. Click **Create new SIP Trunk** , you should automatically be taken to the page where you can configure your SIP trunk.
  2. Go to the **Termination** tab, and enter a **Termination SIP URI** , you can pick any URI you want.


![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/twilio-sip-termination.png?fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=18d202a3b6022ea83fc0b0a140cfef60)
Make sure you leave Secure Trunking disabled.
  1. Go to the **Credential Lists** section and create a new credential list, use a strong username and password.


Make sure you leave the IP Access Control List empty, as Vogent does not support a static range of IP addresses for outbound SIP calls outside of the enterprise plan. Please contact us if this is a security requirement for your use case.
  1. Click **Save**.
  2. If you wish to allow Vogent to transfer calls, you must go to General and enable **Call Transfer (SIP REFER)**


![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/twilio-sip-transfer.png?fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=2340acd05b63e6674e0260c0227cba7d)
  1. In Vogent, Go to the **Call Settings** tab in the left sidebar, and click **Import via SIP** , and enter the termination URI and credentials you created in steps 1-3. You may also do this using the [Create Number API](http://docs.vogent.ai/api-reference/create-number) with `type` set to `sip_import`.


![](https://mintcdn.com/elto-1/A2c2RA9tHzdkFUXP/images/sip-import-dialog-vogent.png?fit=max&auto=format&n=A2c2RA9tHzdkFUXP&q=85&s=2f2e631683a75c4e1db7186f2e6ae2fe)
  1. Click **Import** to create the number, and you should be able to use the number to make outbound calls.


## 
[​](http://docs.vogent.ai/telephony/sip/twilio#for-inbound-calls)
For Inbound Calls
  1. Make sure you complete the outbound SIP trunking steps first.
  2. Go to the **Origination** tab in your SIP trunk settings, click “Add New Origination URI”, enter `sip:sip.vogent.ai`, and click **Add**.


![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/twilio-sip-origination.png?fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=80caff33828b26c82bc7f19e41f863c3)
  1. Go to the **Numbers** tab, and add the numbers you wish to use for inbound calls.


![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/twilio-sip-numbers.png?fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=a0c5a309c7d3bc1051683cbc4b22394f)
  1. Now, go to Vogent, and go to the **Numbers** tab under the Agent you want to use for this phone number, and link the phone number to the agent.


[SIP Trunking Overview](http://docs.vogent.ai/telephony/sip/overview)[Vonage SIP Import](http://docs.vogent.ai/telephony/sip/vonage)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
