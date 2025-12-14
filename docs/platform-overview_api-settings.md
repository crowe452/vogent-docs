Platform Overview

API Settings



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      



  * [API Keys](#api-keys)
  * [Webhooks](#webhooks)
  * [Webhook Configuration](#webhook-configuration)
  * [Verifying the Webhook Signature](#verifying-the-webhook-signature)
  * [Concurrent Dial Limits](#concurrent-dial-limits)
  * [Requesting a Limit Increase](#requesting-a-limit-increase)



Platform Overview

# API Settings

Manage API keys, webhooks, and concurrency limits

You can configure API access, webhook endpoints, and concurrent phone call limits by visiting the **API** tab in the left sidebar.

## 

[​](#api-keys)

API Keys

Navigate to the **Keys** tab and click **New Key** to create a new API key.

If you remove a user from your workspace, their API keys will be deactivated as well.

## 

[​](#webhooks)

Webhooks

Configure webhook settings to receive real-time updates about your voice agents’ activities. Webhooks allow your application to receive automatic notifications about events like call status changes, transcripts, and recordings.

### 

[​](#webhook-configuration)

Webhook Configuration

  1. **Webhook Signing Secret** : A secure key used to verify that incoming webhooks are genuinely from Vogent. Keep this secret secure and use it to validate webhook signatures.
  2. **Webhook URL** : The endpoint where Vogent will send webhook events. This should be a publicly accessible HTTPS URL that can receive POST requests.



For detailed information about webhook payloads and event types, visit our [Webhooks documentation](/webhooks/create-dial).

#### 

[​](#verifying-the-webhook-signature)

Verifying the Webhook Signature

To verify the webhook signature, you need to use the webhook signing secret. The signature is included in the `X-Elto-Signature` header of the webhook request. Here’s an example of how to verify the signature in JavaScript:

Webhook Signature Verification

Copy

```
`function verifyWebhook( payload, signature, signingSecret, algorithm = 'sha256' ) { // Convert payload to buffer if not already const buf = Buffer.isBuffer(payload) ? payload : Buffer.from(payload, 'utf8'); // Convert signature from hex string to buffer const sig = Buffer.from(signature, 'hex'); // Create HMAC with secret const hmac = crypto.createHmac(algorithm, signingSecret); // Calculate digest of payload const digest = Buffer.from(hmac.update(buf).digest('hex'), 'hex'); // Compare calculated digest with provided signature if (sig.length !== digest.length || !crypto.timingSafeEqual(digest, sig)) { throw new Error('Invalid webhook signature'); } return true; } `
```

## 

[​](#concurrent-dial-limits)

Concurrent Dial Limits

Control how many simultaneous phone calls your agents can handle.

  * View your current concurrent dial limit
  * Monitor current usage (“Currently using X”)
  * Request an increase if you need to handle more concurrent calls



Reaching your concurrent dial limit will prevent new calls from being initiated until active calls are completed.

### 

[​](#requesting-a-limit-increase)

Requesting a Limit Increase

Click the **Request Increase** button to submit a request for a higher concurrent dial limit. Our team will review your request and respond ASAP.

[Batch Dial Jobs](/platform-overview/batch-dial-jobs)[Team](/platform-overview/team)