[Skip to main content](http://docs.vogent.ai/platform-overview/api-settings#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Platform Overview
API Settings
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
  * [API Keys](http://docs.vogent.ai/platform-overview/api-settings#api-keys)
  * [Webhooks](http://docs.vogent.ai/platform-overview/api-settings#webhooks)
  * [Webhook Configuration](http://docs.vogent.ai/platform-overview/api-settings#webhook-configuration)
  * [Verifying the Webhook Signature](http://docs.vogent.ai/platform-overview/api-settings#verifying-the-webhook-signature)
  * [Concurrent Dial Limits](http://docs.vogent.ai/platform-overview/api-settings#concurrent-dial-limits)
  * [Requesting a Limit Increase](http://docs.vogent.ai/platform-overview/api-settings#requesting-a-limit-increase)


Platform Overview
# API Settings
Manage API keys, webhooks, and concurrency limits
You can configure API access, webhook endpoints, and concurrent phone call limits by visiting the **API** tab in the left sidebar.
## 
[​](http://docs.vogent.ai/platform-overview/api-settings#api-keys)
API Keys
Navigate to the **Keys** tab and click **New Key** to create a new API key.
If you remove a user from your workspace, their API keys will be deactivated as well.
## 
[​](http://docs.vogent.ai/platform-overview/api-settings#webhooks)
Webhooks
Configure webhook settings to receive real-time updates about your voice agents’ activities. Webhooks allow your application to receive automatic notifications about events like call status changes, transcripts, and recordings.
### 
[​](http://docs.vogent.ai/platform-overview/api-settings#webhook-configuration)
Webhook Configuration
  1. **Webhook Signing Secret** : A secure key used to verify that incoming webhooks are genuinely from Vogent. Keep this secret secure and use it to validate webhook signatures.
  2. **Webhook URL** : The endpoint where Vogent will send webhook events. This should be a publicly accessible HTTPS URL that can receive POST requests.


For detailed information about webhook payloads and event types, visit our [Webhooks documentation](http://docs.vogent.ai/developers/webhooks).
#### 
[​](http://docs.vogent.ai/platform-overview/api-settings#verifying-the-webhook-signature)
Verifying the Webhook Signature
To verify the webhook signature, you need to use the webhook signing secret. The signature is included in the `X-Elto-Signature` header of the webhook request. Here’s an example of how to verify the signature in JavaScript:
Webhook Signature Verification
Copy
```
function verifyWebhook(
 payload,
 signature,
 signingSecret,
 algorithm = 'sha256'
) {
 // Convert payload to buffer if not already
 const buf = Buffer.isBuffer(payload) ? payload : Buffer.from(payload, 'utf8');
 // Convert signature from hex string to buffer
 const sig = Buffer.from(signature, 'hex');
 // Create HMAC with secret
 const hmac = crypto.createHmac(algorithm, signingSecret);
 // Calculate digest of payload
 const digest = Buffer.from(hmac.update(buf).digest('hex'), 'hex');
 // Compare calculated digest with provided signature
 if (sig.length !== digest.length || !crypto.timingSafeEqual(digest, sig)) {
  throw new Error('Invalid webhook signature');
 }
 return true;
}

```

## 
[​](http://docs.vogent.ai/platform-overview/api-settings#concurrent-dial-limits)
Concurrent Dial Limits
Control how many simultaneous phone calls your agents can handle.
  * View your current concurrent dial limit
  * Monitor current usage (“Currently using X”)
  * Request an increase if you need to handle more concurrent calls


Reaching your concurrent dial limit will prevent new calls from being initiated until active calls are completed.
### 
[​](http://docs.vogent.ai/platform-overview/api-settings#requesting-a-limit-increase)
Requesting a Limit Increase
Click the **Request Increase** button to submit a request for a higher concurrent dial limit. Our team will review your request and respond ASAP.
[Batch Dial Jobs](http://docs.vogent.ai/platform-overview/batch-dial-jobs)[Team](http://docs.vogent.ai/platform-overview/team)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
