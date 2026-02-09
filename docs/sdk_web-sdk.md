[Skip to main content](http://docs.vogent.ai/sdk/web-sdk#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
SDKs
Web SDK
[Guides](http://docs.vogent.ai/introduction)[API Reference](http://docs.vogent.ai/api-reference/introduction)[SDK](http://docs.vogent.ai/sdk/web-sdk)[Voicelab](http://docs.vogent.ai/voicelab/introduction)
##### SDKs
  * [Web SDK](http://docs.vogent.ai/sdk/web-sdk)


On this page
  * [Overview](http://docs.vogent.ai/sdk/web-sdk#overview)
  * [Installation](http://docs.vogent.ai/sdk/web-sdk#installation)
  * [Prerequisites](http://docs.vogent.ai/sdk/web-sdk#prerequisites)
  * [Quick Start](http://docs.vogent.ai/sdk/web-sdk#quick-start)
  * [API Reference](http://docs.vogent.ai/sdk/web-sdk#api-reference)
  * [VogentCall Constructor](http://docs.vogent.ai/sdk/web-sdk#vogentcall-constructor)
  * [Methods](http://docs.vogent.ai/sdk/web-sdk#methods)
  * [start()](http://docs.vogent.ai/sdk/web-sdk#start)
  * [connectAudio()](http://docs.vogent.ai/sdk/web-sdk#connectaudio)
  * [monitorTranscript(callback)](http://docs.vogent.ai/sdk/web-sdk#monitortranscript-callback)
  * [setPaused(paused)](http://docs.vogent.ai/sdk/web-sdk#setpaused-paused)
  * [hangup()](http://docs.vogent.ai/sdk/web-sdk#hangup)
  * [Events](http://docs.vogent.ai/sdk/web-sdk#events)
  * [status](http://docs.vogent.ai/sdk/web-sdk#status)
  * [TypeScript Support](http://docs.vogent.ai/sdk/web-sdk#typescript-support)
  * [Error Handling](http://docs.vogent.ai/sdk/web-sdk#error-handling)
  * [Best Practices](http://docs.vogent.ai/sdk/web-sdk#best-practices)


SDKs
# Web SDK
Integrate Vogent into your web applications with the Vogent Web Client SDK
## 
[​](http://docs.vogent.ai/sdk/web-sdk#overview)
Overview
The Vogent Web Client is a TypeScript/JavaScript library that allows you to integrate Vogent voice capabilities directly into your web applications. It provides real-time call management, audio streaming, and transcript monitoring. ## [GitHub RepositoryView the source code and contribute on GitHub](https://github.com/vogent/vogent-web-client)
## 
[​](http://docs.vogent.ai/sdk/web-sdk#installation)
Installation
Install the Vogent Web Client using your preferred package manager:
Bun
NPM
Yarn
Copy
```
bun add @vogent/vogent-web-client

```

## 
[​](http://docs.vogent.ai/sdk/web-sdk#prerequisites)
Prerequisites
Before using the Web SDK, you’ll need:
  * **sessionId** : Unique session identifier
  * **dialId** : Unique dial/call identifier
  * **token** : Authentication token (dial token)


**Important** : Use a public API key when creating browser-based calls. Never expose your secret API key in client-side code.
## 
[​](http://docs.vogent.ai/sdk/web-sdk#quick-start)
Quick Start
Here’s a complete example of how to initiate a call and monitor transcripts:
Copy
```
import { VogentCall } from '@vogent/vogent-web-client';
// Step 1: Create a dial via the Vogent API
const response = await fetch('https://api.vogent.ai/api/dials', {
 method: 'POST',
 headers: {
  'Authorization': 'Bearer pub_vogent_...', // Use your public API key
  'Content-Type': 'application/json'
 },
 body: JSON.stringify({
  callAgentId: 'your_call_agent_id',
  browserCall: true // Important: Enable browser call mode
 })
});
const { dialToken, sessionId, dialId } = await response.json();
// Step 2: Initialize the VogentCall instance
const call = new VogentCall({
 sessionId,
 dialId,
 token: dialToken
});
// Step 3: Start the call session
await call.start();
// Step 4: Connect audio
const audioConnection = await call.connectAudio();
// Step 5: Monitor transcripts in real-time
const unsubscribe = call.monitorTranscript((transcript) => {
 transcript.forEach(({ text, speaker }) => {
  console.log(`${speaker}: ${text}`);
 });
});
// Step 6: Listen for status changes
call.on('status', (status) => {
 console.log('Call status:', status);
});
// Cleanup when done
unsubscribe();
await call.hangup();

```

## 
[​](http://docs.vogent.ai/sdk/web-sdk#api-reference)
API Reference
### 
[​](http://docs.vogent.ai/sdk/web-sdk#vogentcall-constructor)
VogentCall Constructor
Initialize a new call instance:
Copy
```
const call = new VogentCall({
 sessionId: string,
 dialId: string,
 token: string
});

```

**Parameters:**
  * `sessionId` (string): Unique identifier for the session
  * `dialId` (string): Unique identifier for the dial/call
  * `token` (string): Authentication token (dial token)


### 
[​](http://docs.vogent.ai/sdk/web-sdk#methods)
Methods
#### 
[​](http://docs.vogent.ai/sdk/web-sdk#start)
`start()`
Initiates the call session.
Copy
```
await call.start();

```

**Returns:** `Promise<void>`
#### 
[​](http://docs.vogent.ai/sdk/web-sdk#connectaudio)
`connectAudio()`
Establishes the audio connection for the call.
Copy
```
const audioConnection = await call.connectAudio();

```

**Returns:** `Promise<AudioConnection>`
#### 
[​](http://docs.vogent.ai/sdk/web-sdk#monitortranscript-callback)
`monitorTranscript(callback)`
Monitors the call transcript in real-time.
Copy
```
const unsubscribe = call.monitorTranscript((transcript) => {
 transcript.forEach(({ text, speaker }) => {
  console.log(`${speaker}: ${text}`);
 });
});

```

**Parameters:**
  * `callback` (function): Function called with transcript updates

**Returns:** `function` - Unsubscribe function to stop monitoring **Transcript Object:**
  * `text` (string): The transcribed text
  * `speaker` (string): Speaker identifier (e.g., “user”, “agent”)


#### 
[​](http://docs.vogent.ai/sdk/web-sdk#setpaused-paused)
`setPaused(paused)`
Pauses or resumes AI interaction during the call.
Copy
```
await call.setPaused(true); // Pause AI
await call.setPaused(false); // Resume AI

```

**Parameters:**
  * `paused` (boolean): `true` to pause, `false` to resume

**Returns:** `Promise<void>`
#### 
[​](http://docs.vogent.ai/sdk/web-sdk#hangup)
`hangup()`
Ends the call.
Copy
```
await call.hangup();

```

**Returns:** `Promise<void>`
### 
[​](http://docs.vogent.ai/sdk/web-sdk#events)
Events
#### 
[​](http://docs.vogent.ai/sdk/web-sdk#status)
`status`
Listen for call status changes:
Copy
```
call.on('status', (status) => {
 console.log('Call status:', status);
});

```

**Status values:**
  * `connecting`: Call is being established
  * `connected`: Call is active
  * `ended`: Call has ended
  * `error`: An error occurred


## 
[​](http://docs.vogent.ai/sdk/web-sdk#typescript-support)
TypeScript Support
The Vogent Web Client is written in TypeScript and includes full type definitions for an enhanced development experience.
Copy
```
import type { VogentCall, TranscriptItem } from '@vogent/vogent-web-client';

```

## 
[​](http://docs.vogent.ai/sdk/web-sdk#error-handling)
Error Handling
Always wrap your calls in try-catch blocks to handle errors gracefully:
Copy
```
try {
 await call.start();
 await call.connectAudio();
} catch (error) {
 console.error('Call error:', error);
 // Handle error appropriately
}

```

## 
[​](http://docs.vogent.ai/sdk/web-sdk#best-practices)
Best Practices
Use Public API Keys
Always use public API keys (prefixed with `pub_`) in client-side code. Never expose secret API keys in your web application.
Clean Up Resources
Always unsubscribe from transcript monitoring and properly hang up calls when done:
Copy
```
const unsubscribe = call.monitorTranscript(...);
// ... later
unsubscribe();
await call.hangup();

```

⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
