Importing via SIP

Vonage SIP Import



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

                  



      



  * Webhooks

      



  * [For Outbound Calls](#for-outbound-calls)
  * [For Inbound Calls](#for-inbound-calls)



Importing via SIP

# Vonage SIP Import

Import a Vonage phone number into Vogent

Here are the steps to import a Vonage phone number into Vogent.

## 

[​](#for-outbound-calls)

For Outbound Calls

  1. Go to the Vonage Console and select SIP, under the Voice section.



![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/vonage-sip-trunks.png?fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=6a647b6661bf066160b8303ea0937aac)

  1. Click **Create New** , you should automatically be taken to the page where you can configure your SIP trunk.
  2. Click **Add Authentication** and create a new user key and secret, make sure to click the plus icon when you’re done, to add the credentials.



![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/vonage-sip-auth.png?fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=43ffc3183848ad739e25f19a92be0cba)

Make sure you leave the ACL field empty, as Vogent does not support a static range of IP addresses for outbound SIP calls outside of the enterprise plan. Please contact us if this is a security requirement for your use case.

  1. Copy one of the termination URIs that are shown. They should look something like `your-trunk-name.sip-us.vonage.com`.
  2. In Vogent, Go to the **Call Settings** tab in the left sidebar, and click **Import via SIP** , and enter the termination URI and credentials you created in steps 1-3. You may also do this using the [Create Number API](/api-reference/create-number) with `type` set to `sip_import`.



![](https://mintcdn.com/elto-1/A2c2RA9tHzdkFUXP/images/sip-import-dialog-vogent.png?fit=max&auto=format&n=A2c2RA9tHzdkFUXP&q=85&s=2f2e631683a75c4e1db7186f2e6ae2fe)

  1. Click **Import** to create the number, and you should be able to use the number to make outbound calls.



## 

[​](#for-inbound-calls)

For Inbound Calls

  1. Make sure you complete the outbound SIP trunking steps first.
  2. Under the Inbound Calling section, go to the “Select Region” dropdown, and select the region you want to use for inbound calls. Then hit the save icon to save the changes.
  3. Under the “Add URI” section, enter “sip.vogent.ai” under URI, and click the plus icon.



![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/vonage-sip-inbound.png?fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=23df3e506291bd832398f0e4927f423f)

  1. Under the “Link Numbers” section, add the numbers you wish to use for inbound calls.
  2. Now, go to Vogent, and go to the **Numbers** tab under the Agent you want to use for this phone number, and link the phone number to the agent.



[Twilio SIP Import](/telephony/sip/twilio)[Telnyx SIP Import](/telephony/sip/telnyx)





![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/vonage-sip-trunks.png?w=1100&fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=d82d710b5934825d73602715e41769ba)

![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/vonage-sip-auth.png?w=1100&fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=805e00b09d5647b377212b0a828ee41d)

![](https://mintcdn.com/elto-1/A2c2RA9tHzdkFUXP/images/sip-import-dialog-vogent.png?w=1100&fit=max&auto=format&n=A2c2RA9tHzdkFUXP&q=85&s=33f5f857e7bf90277446553f1509e16e)

![](https://mintcdn.com/elto-1/azBE43ot8reGwUsO/images/vonage-sip-inbound.png?w=1100&fit=max&auto=format&n=azBE43ot8reGwUsO&q=85&s=4e12a0318f02c06770b238aa9546c414)