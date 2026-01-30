[Skip to main content](https://docs.vogent.ai/telephony/sip/overview#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](https://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Importing via SIP
SIP Trunking Overview
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
    * [SIP Trunking Overview](https://docs.vogent.ai/telephony/sip/overview)
    * [Twilio SIP Import](https://docs.vogent.ai/telephony/sip/twilio)
    * [Vonage SIP Import](https://docs.vogent.ai/telephony/sip/vonage)
    * [Telnyx SIP Import](https://docs.vogent.ai/telephony/sip/telnyx)
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
  * [Outbound Overview](https://docs.vogent.ai/telephony/sip/overview#outbound-overview)
  * [Inbound Overview](https://docs.vogent.ai/telephony/sip/overview#inbound-overview)


Importing via SIP
# SIP Trunking Overview
Overview of SIP trunking in Vogent
Vogent supports connecting numbers you own through any compatible provider to the platform, for both inbound and outbound calls. Any VoIP provider that offers an Elastic SIP trunking service or equivalent should work with Vogent. Detailed instructions for setting up SIP trunking on select carriers are provided below. For other carriers, please use the general instructions below, and contact support if you need help.
## 
[​](https://docs.vogent.ai/telephony/sip/overview#outbound-overview)
Outbound Overview
  1. Create a SIP trunk with your carrier.
  2. Find or create a termination URI for your SIP trunk. It should look something like `your-domain.voip-provider.com` (for example, `domain.pstn.twilio.com` for Twilio).
  3. You will likely be asked to either create a username and password for SIP authentication, or provide an allowed list of IP addresses. Yould create a username and password, and allow traffic from all IPs. Vogent does not currently support a static range of IP addresses for outbound SIP calls outside of the enterprise plan.
  4. In Vogent, Go to the **Call Settings** tab in the left sidebar, and click **Import via SIP** , and enter the termination URI and credentials you created in steps 1-3. You may also do this using the [Create Number API](https://docs.vogent.ai/api-reference/create-number) with `type` set to `sip_import`.


![](https://mintcdn.com/elto-1/A2c2RA9tHzdkFUXP/images/sip-import-dialog-vogent.png?fit=max&auto=format&n=A2c2RA9tHzdkFUXP&q=85&s=2f2e631683a75c4e1db7186f2e6ae2fe)
  1. Click **Import** to create the number, and you should be able to use the number to make outbound calls.


## 
[​](https://docs.vogent.ai/telephony/sip/overview#inbound-overview)
Inbound Overview
  1. Make sure you complete the outbound SIP trunking steps first.
  2. Find the section in your carrier’s SIP trunking settings that lets you select an origination/outbound URL. You should fill this in with `sip:sip.vogent.ai` or `sip.vogent.ai`, depending on the format that’s expected by your carrier.
  3. You’ll need to link the phone numbers you want to use for inbound calls to your SIP trunk with your carrier. Usually this is done within the trunk settings.
  4. Now, go to Vogent, and go to the **Numbers** tab under the Agent you want to use for this phone number, and link the phone number to the agent.


[Overview](https://docs.vogent.ai/telephony/overview)[Twilio SIP Import](https://docs.vogent.ai/telephony/sip/twilio)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
