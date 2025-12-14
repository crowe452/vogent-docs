Phone Numbers

Using a SIP Domain



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      



  * [Creating a SIP Domain](#creating-a-sip-domain)
  * [Example: Using a SIP Domain with Twilio](#example%3A-using-a-sip-domain-with-twilio)



Phone Numbers

# Using a SIP Domain

Create a SIP domain to make and receive calls

Vogent also supports creating a SIP domain to make and receive calls. This allows you to completely manage telephony side of the stack, and use SIP to allow Vogent to communicate with the calls you originate.

## 

[​](#creating-a-sip-domain)

Creating a SIP Domain

  1. Go to the **Call Settings** tab in the left sidebar, click **Add Phone Number** , then select **Vogent SIP**.
  2. Enter a SIP username/prefix, and an authentication username/password, and click **Add SIP URI**.
  3. You’re now ready to use this SIP domain to make and receive calls from any number in your workspace.



## 

[​](#example:-using-a-sip-domain-with-twilio)

Example: Using a SIP Domain with Twilio

You can use a SIP domain to service a Twilio phone number. Link the following TwiML to your Twilio phone number, replacing the auth_username, auth_password, and prefix with the values you created above.

Copy

```
`<Response> <Dial> <Sip username="{{auth_username}}" password="{{auth_password}}">{{prefix}}@sip.vogent.ai</Sip> </Dial> </Response> `
```

[Telnyx SIP Import](/telephony/sip/telnyx)[Self Learning Overview](/platform-overview/self-learning/overview)