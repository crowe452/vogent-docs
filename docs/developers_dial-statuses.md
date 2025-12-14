For Developers

Dials Statuses



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      


For Developers

# Dials Statuses

Lifecycle of a dial.

A dial in elto goes through a number of statuses, both for browser and web calls. The `dial.updated` webhook will be called whenever the status changes, so you can keep track of the changes on your server.

  * `queued` All dials start off in `queued` status. This means that the dial is created, and either the model is warming up, the call is queued by the telephony provider, or in the case of browser calls, is waiting on the user to connect to the data.
  * `ringing` This means that the call is being made, in the case of a telephone call, this means the call is ringing, in the case of a browser call, it just means that the web call is being connected.
  * `in-progress` The call has been connected and the agent is hooked into the call.
  * `completed`, `failed`, `canceled`, `busy`, `no-answer` These are call completed statuses. The `completed` status indicates that the call completed successfully, the other completed statuses are only used for phone calls and indicate errors that caused the call not to be picked up.



[Dials and Dial Sessions](/developers/dials-dialsessions)[Flow Builder Schemas](/developers/schemas)