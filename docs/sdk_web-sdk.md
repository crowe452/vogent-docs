SDKs

Web SDK



  



  * [Overview](#overview)
  * [Installation](#installation)
  * [Prerequisites](#prerequisites)
  * [Quick Start](#quick-start)
  * [API Reference](#api-reference)
  * [VogentCall Constructor](#vogentcall-constructor)
  * [Methods](#methods)
  * [start()](#start)
  * [connectAudio()](#connectaudio)
  * [monitorTranscript(callback)](#monitortranscript-callback)
  * [setPaused(paused)](#setpaused-paused)
  * [hangup()](#hangup)
  * [Events](#events)
  * [status](#status)
  * [TypeScript Support](#typescript-support)
  * [Error Handling](#error-handling)
  * [Best Practices](#best-practices)



SDKs

# Web SDK

Integrate Vogent into your web applications with the Vogent Web Client SDK

## 

[​](#overview)

Overview

The Vogent Web Client is a TypeScript/JavaScript library that allows you to integrate Vogent voice capabilities directly into your web applications. It provides real-time call management, audio streaming, and transcript monitoring. ## [GitHub RepositoryView the source code and contribute on GitHub](https://github.com/vogent/vogent-web-client)

## 

[​](#installation)

Installation

Install the Vogent Web Client using your preferred package manager:

Bun

NPM

Yarn

Copy

```
`bun add @vogent/vogent-web-client `
```

## 

[​](#prerequisites)

Prerequisites

Before using the Web SDK, you’ll need:

  * **sessionId** : Unique session identifier
  * **dialId** : Unique dial/call identifier
  * **token** : Authentication token (dial token)



**Important** : Use a public API key when creating browser-based calls. Never expose your secret API key in client-side code.

## 

[​](#quick-start)

Quick Start

Here’s a complete example of how to initiate a call and monitor transcripts:

Copy

```
`import { VogentCall } from '@vogent/vogent-web-client'; // Step 1: Create a dial via the Vogent API const response = await fetch('https://api.vogent.ai/api/dials', { method: 'POST', headers: { 'Authorization': 'Bearer pub_vogent_...', // Use your public API key 'Content-Type': 'application/json' }, body: JSON.stringify({ callAgentId: 'your_call_agent_id', browserCall: true // Important: Enable browser call mode }) }); const { dialToken, sessionId, dialId } = await response.json(); // Step 2: Initialize the VogentCall instance const call = new VogentCall({ sessionId, dialId, token: dialToken }); // Step 3: Start the call session await call.start(); // Step 4: Connect audio const audioConnection = await call.connectAudio(); // Step 5: Monitor transcripts in real-time const unsubscribe = call.monitorTranscript((transcript) => { transcript.forEach(({ text, speaker }) => { console.log(`${speaker}: ${text}`); }); }); // Step 6: Listen for status changes call.on('status', (status) => { console.log('Call status:', status); }); // Cleanup when done unsubscribe(); await call.hangup(); `
```

## 

[​](#api-reference)

API Reference

### 

[​](#vogentcall-constructor)

VogentCall Constructor

Initialize a new call instance:

Copy

```
`const call = new VogentCall({ sessionId: string, dialId: string, token: string }); `
```

**Parameters:**

  * `sessionId` (string): Unique identifier for the session
  * `dialId` (string): Unique identifier for the dial/call
  * `token` (string): Authentication token (dial token)



### 

[​](#methods)

Methods

#### 

[​](#start)

`start()`

Initiates the call session.

Copy

```
`await call.start(); `
```

**Returns:** `Promise<void>`

#### 

[​](#connectaudio)

`connectAudio()`

Establishes the audio connection for the call.

Copy

```
`const audioConnection = await call.connectAudio(); `
```

**Returns:** `Promise<AudioConnection>`

#### 

[​](#monitortranscript-callback)

`monitorTranscript(callback)`

Monitors the call transcript in real-time.

Copy

```
`const unsubscribe = call.monitorTranscript((transcript) => { transcript.forEach(({ text, speaker }) => { console.log(`${speaker}: ${text}`); }); }); `
```

**Parameters:**

  * `callback` (function): Function called with transcript updates

**Returns:** `function` - Unsubscribe function to stop monitoring **Transcript Object:**

  * `text` (string): The transcribed text
  * `speaker` (string): Speaker identifier (e.g., “user”, “agent”)



#### 

[​](#setpaused-paused)

`setPaused(paused)`

Pauses or resumes AI interaction during the call.

Copy

```
`await call.setPaused(true); // Pause AI await call.setPaused(false); // Resume AI `
```

**Parameters:**

  * `paused` (boolean): `true` to pause, `false` to resume

**Returns:** `Promise<void>`

#### 

[​](#hangup)

`hangup()`

Ends the call.

Copy

```
`await call.hangup(); `
```

**Returns:** `Promise<void>`

### 

[​](#events)

Events

#### 

[​](#status)

`status`

Listen for call status changes:

Copy

```
`call.on('status', (status) => { console.log('Call status:', status); }); `
```

**Status values:**

  * `connecting`: Call is being established
  * `connected`: Call is active
  * `ended`: Call has ended
  * `error`: An error occurred



## 

[​](#typescript-support)

TypeScript Support

The Vogent Web Client is written in TypeScript and includes full type definitions for an enhanced development experience.

Copy

```
`import type { VogentCall, TranscriptItem } from '@vogent/vogent-web-client'; `
```

## 

[​](#error-handling)

Error Handling

Always wrap your calls in try-catch blocks to handle errors gracefully:

Copy

```
`try { await call.start(); await call.connectAudio(); } catch (error) { console.error('Call error:', error); // Handle error appropriately } `
```

## 

[​](#best-practices)

Best Practices

Use Public API Keys

Always use public API keys (prefixed with `pub_`) in client-side code. Never expose secret API keys in your web application.

Clean Up Resources

Always unsubscribe from transcript monitoring and properly hang up calls when done:

Copy

```
`const unsubscribe = call.monitorTranscript(...); // ... later unsubscribe(); await call.hangup(); `
```