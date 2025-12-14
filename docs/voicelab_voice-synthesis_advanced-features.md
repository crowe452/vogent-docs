Advanced Voice Synthesis Features



              



  * [Advanced Voice Synthesis Features](#advanced-voice-synthesis-features)
  * [Multispeaker Text to Speech](#multispeaker-text-to-speech)
  * [Basic Multispeaker Usage](#basic-multispeaker-usage)
  * [Advanced Multispeaker Scenarios](#advanced-multispeaker-scenarios)
  * [Customer Service Training](#customer-service-training)
  * [Educational Content](#educational-content)
  * [Voice Selection Best Practices](#voice-selection-best-practices)
  * [Professional Contexts](#professional-contexts)
  * [Casual and Creative Content](#casual-and-creative-content)
  * [Voice Pairing Guidelines](#voice-pairing-guidelines)
  * [Streaming Audio Output](#streaming-audio-output)
  * [Benefits of Streaming](#benefits-of-streaming)
  * [Implementation Tips](#implementation-tips)
  * [Error Handling and Best Practices](#error-handling-and-best-practices)
  * [Common Error Scenarios](#common-error-scenarios)
  * [Rate Limiting Best Practices](#rate-limiting-best-practices)
  * [Performance Optimization](#performance-optimization)
  * [Text Length Considerations](#text-length-considerations)
  * [Batch Processing](#batch-processing)
  * [Integration Examples](#integration-examples)
  * [Web Application Integration](#web-application-integration)
  * [Mobile App Integration](#mobile-app-integration)



# Advanced Voice Synthesis Features

Explore advanced voice synthesis capabilities

# 

[​](#advanced-voice-synthesis-features)

Advanced Voice Synthesis Features

Discover the advanced features available in Voicelab’s voice synthesis engine.

## 

[​](#multispeaker-text-to-speech)

Multispeaker Text to Speech

Create conversations and dialogues with multiple distinct voices in a single audio file.

### 

[​](#basic-multispeaker-usage)

Basic Multispeaker Usage

Generate conversations with different speakers:

Copy

```
`import requests response = requests.post( "https://api.vogent.ai/api/tts/multispeaker", headers={"Authorization": f"Bearer {api_key}"}, json={ "lines": [ { "text": "Welcome to our store! How can I help you today?", "voiceId": "professional-female-1" }, { "text": "Hi, I'm looking for a new laptop for work.", "voiceId": "conversational-male-1" }, { "text": "Great! I can help you find the perfect laptop. What type of work do you do?", "voiceId": "professional-female-1" } ] } ) if response.status_code == 200: with open("conversation.wav", "wb") as f: f.write(response.content) print("Conversation saved successfully!") `
```

### 

[​](#advanced-multispeaker-scenarios)

Advanced Multispeaker Scenarios

Create complex dialogues for various use cases:

#### 

[​](#customer-service-training)

Customer Service Training

Copy

```
`training_dialogue = { "lines": [ {"text": "Thank you for calling customer support. How can I assist you today?", "voiceId": "professional-female-1"}, {"text": "I'm having trouble with my recent order. It hasn't arrived yet.", "voiceId": "conversational-male-1"}, {"text": "I understand your concern. Let me look up your order details. Can you provide your order number?", "voiceId": "professional-female-1"}, {"text": "Sure, it's order number 12345.", "voiceId": "conversational-male-1"}, {"text": "Thank you. I can see your order was shipped yesterday and should arrive by tomorrow.", "voiceId": "professional-female-1"} ] } response = requests.post("https://api.vogent.ai/tts/multispeaker", headers=headers, json=training_dialogue) `
```

#### 

[​](#educational-content)

Educational Content

Copy

```
`lesson_dialogue = { "lines": [ {"text": "Today we're learning about photosynthesis. Can anyone tell me what plants need for photosynthesis?", "voiceId": "professional-female-1"}, {"text": "They need sunlight, water, and carbon dioxide!", "voiceId": "conversational-female-1"}, {"text": "Excellent! And what do plants produce during photosynthesis?", "voiceId": "professional-female-1"}, {"text": "They produce oxygen and glucose!", "voiceId": "conversational-male-1"} ] } `
```

## 

[​](#voice-selection-best-practices)

Voice Selection Best Practices

Choose appropriate voices for different scenarios:

### 

[​](#professional-contexts)

Professional Contexts

  * **Business presentations** : Use `professional-female-1` or `professional-male-1`
  * **Corporate training** : Professional voices for instructors, conversational for participants
  * **Customer service** : Professional voices for representatives



### 

[​](#casual-and-creative-content)

Casual and Creative Content

  * **Podcasts** : Mix of conversational and expressive voices
  * **Audiobooks** : Expressive voices for characters, conversational for narration
  * **Social media content** : Conversational voices for relatability



### 

[​](#voice-pairing-guidelines)

Voice Pairing Guidelines

When using multiple voices in a conversation:

  1. **Contrast is key** : Use different genders or voice types for clarity
  2. **Consistency** : Keep the same voice for each character throughout
  3. **Context matching** : Match voice formality to the scenario



Copy

```
`# Good voice pairing example customer_service_scenario = { "lines": [ {"text": "Good morning, how may I help you?", "voiceId": "professional-female-1"}, # Formal representative {"text": "Hi, I need help with my account.", "voiceId": "conversational-male-1"}, # Casual customer {"text": "I'd be happy to assist you with that.", "voiceId": "professional-female-1"} # Consistent representative ] } `
```

## 

[​](#streaming-audio-output)

Streaming Audio Output

Voicelab automatically streams audio bytes as they are generated, providing optimal performance for real-time applications.

### 

[​](#benefits-of-streaming)

Benefits of Streaming

  * **Lower latency** : Audio starts playing before generation is complete
  * **Memory efficiency** : No need to buffer entire audio files
  * **Better user experience** : Immediate audio feedback



### 

[​](#implementation-tips)

Implementation Tips

Copy

```
`import requests # Stream audio directly to a file response = requests.post( "https://api.vogent.ai/api/tts", headers={"Authorization": f"Bearer {api_key}"}, json={"text": "This is a streaming audio example.", "voiceId": "professional-female-1"}, stream=True ) with open("streaming_audio.wav", "wb") as f: for chunk in response.iter_content(chunk_size=8192): if chunk: f.write(chunk) `
```

## 

[​](#error-handling-and-best-practices)

Error Handling and Best Practices

### 

[​](#common-error-scenarios)

Common Error Scenarios

Copy

```
`import requests def synthesize_text(text, voice_id): try: response = requests.post( "https://api.vogent.ai/api/tts", headers={"Authorization": f"Bearer {api_key}"}, json={"text": text, "voiceId": voice_id} ) if response.status_code == 200: return response.content elif response.status_code == 400: print("Error: Invalid input - check your text and voice ID") elif response.status_code == 422: print("Error: Validation failed - invalid voice ID or text format") elif response.status_code == 429: print("Error: Rate limit exceeded - please wait before retrying") else: print(f"Error: Unexpected status code {response.status_code}") except requests.exceptions.RequestException as e: print(f"Network error: {e}") return None `
```

### 

[​](#rate-limiting-best-practices)

Rate Limiting Best Practices

Copy

```
`import time import requests def synthesize_with_retry(text, voice_id, max_retries=3): for attempt in range(max_retries): try: response = requests.post( "https://api.vogent.ai/api/tts", headers={"Authorization": f"Bearer {api_key}"}, json={"text": text, "voiceId": voice_id} ) if response.status_code == 200: return response.content elif response.status_code == 429: # Rate limited, wait and retry wait_time = 2 ** attempt # Exponential backoff print(f"Rate limited. Waiting {wait_time} seconds before retry...") time.sleep(wait_time) continue else: print(f"Error: {response.status_code}") break except requests.exceptions.RequestException as e: print(f"Network error: {e}") time.sleep(2 ** attempt) return None `
```

## 

[​](#performance-optimization)

Performance Optimization

### 

[​](#text-length-considerations)

Text Length Considerations

  * **Optimal length** : 100-1000 characters per request
  * **Maximum length** : 5000 characters for single TTS
  * **Multispeaker limits** : 500 characters per line, 10 lines maximum



### 

[​](#batch-processing)

Batch Processing

For large amounts of text, split into smaller chunks:

Copy

```
`def batch_synthesize(long_text, voice_id, chunk_size=1000): chunks = [long_text[i:i+chunk_size] for i in range(0, len(long_text), chunk_size)] audio_files = [] for i, chunk in enumerate(chunks): audio_data = synthesize_text(chunk, voice_id) if audio_data: filename = f"chunk_{i}.wav" with open(filename, "wb") as f: f.write(audio_data) audio_files.append(filename) return audio_files `
```

## 

[​](#integration-examples)

Integration Examples

### 

[​](#web-application-integration)

Web Application Integration

Copy

```
`// Frontend JavaScript example async function synthesizeText(text, voiceId) { try { const response = await fetch('/api/tts', { method: 'POST', headers: { 'Content-Type': 'application/json', }, body: JSON.stringify({ text, voiceId }) }); if (response.ok) { const audioBlob = await response.blob(); const audioUrl = URL.createObjectURL(audioBlob); const audio = new Audio(audioUrl); audio.play(); } } catch (error) { console.error('TTS Error:', error); } } `
```

### 

[​](#mobile-app-integration)

Mobile App Integration

Copy

```
`# Python backend for mobile app from flask import Flask, request, Response import requests app = Flask(__name__) @app.route('/tts', methods=['POST']) def text_to_speech(): data = request.json response = requests.post( "https://api.vogent.ai/tts", headers={"Authorization": f"Bearer {API_KEY}"}, json=data ) if response.status_code == 200: return Response( response.content, mimetype='audio/wav', headers={'Content-Disposition': 'attachment; filename=speech.wav'} ) else: return {'error': 'TTS generation failed'}, 500 `
```