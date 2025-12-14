For Developers

Dials and Dial Sessions



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      


For Developers

# Dials and Dial Sessions

Core objects in Elto.

Elto has 2 objects that that you need to be familiar with when you make calls. When you create a one-off dial, you create a `DialSession`. When the `DialSession` is started, a `Dial` is created, and initiated. The reason for this distinction is to allow you to specify a configuration that may be used for multiple dials, that can then be orchestrated by Elto without overrunning any concurrent call limits. When you make a one off phone call, the dial is started automatically, for web calls, the dial is automatically started once a user connects their browser/client. The endpoint returns a dial session ID. Once the `Dial` is created, you’ll get a webhook, in case you need to manage the `Dial` further.

[Function Call](/developers/webhooks/function-call)[Dials Statuses](/developers/dial-statuses)