Importing via SIP

SIP Trunking Overview



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

                  



      



  * Webhooks

      



  * [Outbound Overview](#outbound-overview)
  * [Inbound Overview](#inbound-overview)



Importing via SIP

# SIP Trunking Overview

Overview of SIP trunking in Vogent

Vogent supports connecting numbers you own through any compatible provider to the platform, for both inbound and outbound calls. Any VoIP provider that offers an Elastic SIP trunking service or equivalent should work with Vogent. Detailed instructions for setting up SIP trunking on select carriers are provided below. For other carriers, please use the general instructions below, and contact support if you need help.

## 

[​](#outbound-overview)

Outbound Overview

  1. Create a SIP trunk with your carrier.
  2. Find or create a termination URI for your SIP trunk. It should look something like `your-domain.voip-provider.com` (for example, `domain.pstn.twilio.com` for Twilio).
  3. You will likely be asked to either create a username and password for SIP authentication, or provide an allowed list of IP addresses. Yould create a username and password, and allow traffic from all IPs. Vogent does not currently support a static range of IP addresses for outbound SIP calls outside of the enterprise plan.
  4. In Vogent, Go to the **Call Settings** tab in the left sidebar, and click **Import via SIP** , and enter the termination URI and credentials you created in steps 1-3. You may also do this using the [Create Number API](/api-reference/create-number) with `type` set to `sip_import`.



![](https://mintcdn.com/elto-1/A2c2RA9tHzdkFUXP/images/sip-import-dialog-vogent.png?fit=max&auto=format&n=A2c2RA9tHzdkFUXP&q=85&s=2f2e631683a75c4e1db7186f2e6ae2fe)

  1. Click **Import** to create the number, and you should be able to use the number to make outbound calls.



## 

[​](#inbound-overview)

Inbound Overview

  1. Make sure you complete the outbound SIP trunking steps first.
  2. Find the section in your carrier’s SIP trunking settings that lets you select an origination/outbound URL. You should fill this in with `sip:sip.vogent.ai` or `sip.vogent.ai`, depending on the format that’s expected by your carrier.
  3. You’ll need to link the phone numbers you want to use for inbound calls to your SIP trunk with your carrier. Usually this is done within the trunk settings.
  4. Now, go to Vogent, and go to the **Numbers** tab under the Agent you want to use for this phone number, and link the phone number to the agent.



[Overview](/telephony/overview)[Twilio SIP Import](/telephony/sip/twilio)