[Skip to main content](http://docs.vogent.ai/telephony/sip/telnyx#content-area)
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
Telnyx SIP Import
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


Importing via SIP
# Telnyx SIP Import
Import a Telnyx phone number into Vogent
Here are the steps to import a Telnyx phone number into Vogent.
  1. Go to the Telnyx Console and select SIP, under the Real-Time Communications > Voice section, and click **Create SIP Connection**.


![](https://mintcdn.com/elto-1/A2c2RA9tHzdkFUXP/images/telnyx-sip-trunks.png?fit=max&auto=format&n=A2c2RA9tHzdkFUXP&q=85&s=aa2b22885e878cf371a44380133fd30e)
  1. Select a name for your trunk, and select “FQDN” as the type, then click “Create”.


![](https://mintcdn.com/elto-1/A2c2RA9tHzdkFUXP/images/telnyx-sip-connection.png?fit=max&auto=format&n=A2c2RA9tHzdkFUXP&q=85&s=627ecb1a6f04eaeff6dc76e6b51b8d42)
  1. Click “Add FQDN”, and enter “sip.vogent.ai” as the FQDN to add.


![](https://mintcdn.com/elto-1/A2c2RA9tHzdkFUXP/images/telnyx-add-fqdn.png?fit=max&auto=format&n=A2c2RA9tHzdkFUXP&q=85&s=506fcf05b2095142590fdf5c32270db0)
  1. Select the FQDN you just added (sip.vogent.ai) under “Primary FQDN”.
  2. Under the “Outbound calls authentication” section, select “Credentials” as the type, and create a username and password for the credentials.


![](https://mintcdn.com/elto-1/A2c2RA9tHzdkFUXP/images/telnyx-sip-creds.png?fit=max&auto=format&n=A2c2RA9tHzdkFUXP&q=85&s=2fd65baa444941a6005035daff460224)
  1. On the “Configuration” step, click Next, you may leave the defaults as-is for this step.
  2. On the “Inbound” step, select “E.164” as the Origination number format, **do not use the default of “E.164 / National (e.g. US - 10 digits)”** , this may cause issues with non-US calls.


![](https://mintcdn.com/elto-1/ctCi8sSZ0gjwBHx2/images/telnyx-inbound-settings.png?fit=max&auto=format&n=ctCi8sSZ0gjwBHx2&q=85&s=a053bfd78ef82a9d071624dc7606e236)
  1. On the “Outbound” step, select “Default” as the outbound voice profile, and click Next.
  2. Select the numbers you wish to use for inbound calls in the “Assign Numbers” step, and click Complete.
  3. In Vogent, Go to the **Call Settings** tab in the left sidebar, and click **Import via SIP** , and enter sip.vogent.ai as the URI, and the username and password you created in step 5 as the credentials.


![](https://mintcdn.com/elto-1/A2c2RA9tHzdkFUXP/images/sip-import-dialog-vogent.png?fit=max&auto=format&n=A2c2RA9tHzdkFUXP&q=85&s=2f2e631683a75c4e1db7186f2e6ae2fe)
  1. Click **Import** to create the number, and you should be able to use the number to make outbound calls.
  2. To make inbound calls, you will need to add the numbers you selected in step 9 to the agent you want to use for inbound calls.


[Vonage SIP Import](http://docs.vogent.ai/telephony/sip/vonage)[Using a SIP Domain](http://docs.vogent.ai/telephony/sip-domain/overview)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
