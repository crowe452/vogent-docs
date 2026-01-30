[Skip to main content](https://docs.vogent.ai/telephony/sip-domain/overview#content-area)
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
Using a SIP Domain
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
  * [Creating a SIP Domain](https://docs.vogent.ai/telephony/sip-domain/overview#creating-a-sip-domain)
  * [Example: Using a SIP Domain with Twilio](https://docs.vogent.ai/telephony/sip-domain/overview#example%3A-using-a-sip-domain-with-twilio)


Phone Numbers
# Using a SIP Domain
Create a SIP domain to make and receive calls
Vogent also supports creating a SIP domain to make and receive calls. This allows you to completely manage telephony side of the stack, and use SIP to allow Vogent to communicate with the calls you originate.
## 
[​](https://docs.vogent.ai/telephony/sip-domain/overview#creating-a-sip-domain)
Creating a SIP Domain
  1. Go to the **Call Settings** tab in the left sidebar, click **Add Phone Number** , then select **Vogent SIP**.
  2. Enter a SIP username/prefix, and an authentication username/password, and click **Add SIP URI**.
  3. You’re now ready to use this SIP domain to make and receive calls from any number in your workspace.


## 
[​](https://docs.vogent.ai/telephony/sip-domain/overview#example:-using-a-sip-domain-with-twilio)
Example: Using a SIP Domain with Twilio
You can use a SIP domain to service a Twilio phone number. Link the following TwiML to your Twilio phone number, replacing the auth_username, auth_password, and prefix with the values you created above.
Copy
```
<Response>
 <Dial>
  <Sip username="{{auth_username}}" password="{{auth_password}}">{{prefix}}@sip.vogent.ai</Sip>
 </Dial>
</Response>

```

[Telnyx SIP Import](https://docs.vogent.ai/telephony/sip/telnyx)[Self Learning Overview](https://docs.vogent.ai/platform-overview/self-learning/overview)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
