[Skip to main content](http://docs.vogent.ai/voicelab/quickstart#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Voicelab
Quickstart
[Guides](http://docs.vogent.ai/introduction)[API Reference](http://docs.vogent.ai/api-reference/introduction)[SDK](http://docs.vogent.ai/sdk/web-sdk)[Voicelab](http://docs.vogent.ai/voicelab/introduction)
##### Voicelab
  * [Introduction](http://docs.vogent.ai/voicelab/introduction)
  * [Quickstart](http://docs.vogent.ai/voicelab/quickstart)
  * [Models](http://docs.vogent.ai/voicelab/models)
  * [Voices and Voice Cloning](http://docs.vogent.ai/voicelab/voices)
  * [Fine-tuning and Hosting](http://docs.vogent.ai/voicelab/fine-tuning)
  * [On-premise Deployment](http://docs.vogent.ai/voicelab/on-premise)
  * [Roadmap](http://docs.vogent.ai/voicelab/roadmap)


On this page
  * [Step 1: Sign up and get your API key](http://docs.vogent.ai/voicelab/quickstart#step-1%3A-sign-up-and-get-your-api-key)
  * [Step 2: Make Your First Request](http://docs.vogent.ai/voicelab/quickstart#step-2%3A-make-your-first-request)
  * [Basic Text-to-Speech](http://docs.vogent.ai/voicelab/quickstart#basic-text-to-speech)
  * [Test the Audio](http://docs.vogent.ai/voicelab/quickstart#test-the-audio)
  * [Step 3: Create a Conversation](http://docs.vogent.ai/voicelab/quickstart#step-3%3A-create-a-conversation)
  * [Step 4: Real-time Streaming with WebSockets](http://docs.vogent.ai/voicelab/quickstart#step-4%3A-real-time-streaming-with-websockets)
  * [Why Use WebSocket Streaming?](http://docs.vogent.ai/voicelab/quickstart#why-use-websocket-streaming)
  * [Next Steps](http://docs.vogent.ai/voicelab/quickstart#next-steps)
  * [Need Help?](http://docs.vogent.ai/voicelab/quickstart#need-help)


Voicelab
# Quickstart
Create your first voice generations
## 
[​](http://docs.vogent.ai/voicelab/quickstart#step-1:-sign-up-and-get-your-api-key)
Step 1: Sign up and get your API key
First, you’ll need to obtain your API key from the Vogent dashboard.
  1. Go to [app.vogent.ai](https://app.vogent.ai)
  2. Sign up or log in to your account
  3. Navigate to **API** in the sidebar
  4. Create a new key by clicking **New Key**


This is a private API key; make sure to never expose it client-side.
## 
[​](http://docs.vogent.ai/voicelab/quickstart#step-2:-make-your-first-request)
Step 2: Make Your First Request
### 
[​](http://docs.vogent.ai/voicelab/quickstart#basic-text-to-speech)
Basic Text-to-Speech
Let’s start with a simple text-to-speech request:
cURL
Python
JavaScript
Copy
```
curl -X POST "https://api.vogent.ai/api/tts" \
 -H "Authorization: Bearer YOUR_API_KEY" \
 -H "Content-Type: application/json" \
 -d '{
  "text": "So I tried this new thing called Voicelab that I found online, and the voices that it generated were super realistic.",
  "voiceId": "23b2186b-ed56-4185-998c-8d19e1bb227a"
 }' \
 --output my-first-voice.wav

```

### 
[​](http://docs.vogent.ai/voicelab/quickstart#test-the-audio)
Test the Audio
After running the code above, you should have an audio file called `my-first-voice.wav`. Play it to hear the generation!
## 
[​](http://docs.vogent.ai/voicelab/quickstart#step-3:-create-a-conversation)
Step 3: Create a Conversation
Now let’s try the multispeaker feature to create a conversation:
Python
cURL
Copy
```
import requests
api_key = "YOUR_API_KEY"
# Create a conversation between two people
conversation = {
  "lines": [
    {
      "text": "So I tried this new thing called Voicelab that I found online, and the voices that it generated were super realistic.",
      "voiceId": "23b2186b-ed56-4185-998c-8d19e1bb227a" # The CSM-1B professional voice clone "Mabel"
    },
    {
      "text": "That's interesting, was it actually like super realistic or was it just not robotic.",
      "voiceId": "50c9287d-bcee-4f2a-943f-f0f2184a5d3b" # The CSM-1B professional voice clone "Kevin"
    },
    {
      "text": "I mean, it's hard to tell the difference from a real person speaking. The technology is incredible.",
      "voiceId": "23b2186b-ed56-4185-998c-8d19e1bb227a" # The CSM-1B professional voice clone "Mabel"
    },
    {
      "text": "Interesting, I've been looking for a new API to use in my app. I'll definitely check it out then.",
      "voiceId": "50c9287d-bcee-4f2a-943f-f0f2184a5d3b" # The CSM-1B professional voice clone "Kevin"
    }
  ]
}
response = requests.post(
  "https://api.vogent.ai/api/tts/multispeaker",
  headers={"Authorization": f"Bearer {api_key}"},
  json=conversation
)
if response.status_code == 200:
  with open("conversation.wav", "wb") as f:
    f.write(response.content)
  print("✅ Conversation saved as 'conversation.wav'")
else:
  print(f"❌ Error: {response.status_code}")

```

## 
[​](http://docs.vogent.ai/voicelab/quickstart#step-4:-real-time-streaming-with-websockets)
Step 4: Real-time Streaming with WebSockets
For real-time applications, you can use WebSockets to stream text and receive audio chunks as they’re generated:
Python
Copy
```
import asyncio
import websockets
import json
import base64
import uuid
import wave
SAMPLE_RATE = 24000
API_KEY = ""
async def stream_tts():
  # Connect to the WebSocket endpoint
  uri = f"wss://api.vogent.ai/api/tts/websocket?apiKey={API_KEY}"
  generation_id = f"gen_{uuid.uuid4()}"
  async with websockets.connect(uri) as websocket:
    print("🔗 Connected to Voicelab WebSocket")
    # Send initial text chunk
    await websocket.send(json.dumps({
      "generationId": generation_id,
      "voiceId": "36b87413-6d7b-421d-8745-bc0897770d1e", # Mabel voice
      "text": "Hello! This is a real-time streaming example.",
      "finalText": False,
      "sampleRate": 24000,
      "cancel": False
    }))
    # Send final text chunk
    await websocket.send(json.dumps({
      "generationId": generation_id,
      "voiceId": "36b87413-6d7b-421d-8745-bc0897770d1e",
      "text": " This demonstrates real-time text-to-speech streaming!",
      "finalText": True,
      "cancel": False
    }))
    audio_chunks = []
    print("Listening for audio")
    # Listen for audio chunks
    async for message in websocket:
      data = json.loads(message)
      if data["type"] == "chunk":
        # Decode and store audio chunk
        audio_data = base64.b64decode(data["audio"])
        audio_chunks.append(audio_data)
        print("🎵 Received audio chunk")
      elif data["type"] == "error":
        print(f"❌ Error: {data['error']}")
        break
      elif data["type"] == "finished":
        print("✅ Streaming complete!")
        with wave.open("streaming_audio.wav", "wb") as wf:
          wf.setnchannels(1)
          wf.setsampwidth(2)
          wf.setframerate(SAMPLE_RATE)
          print("Chunks", len(audio_chunks))
          for chunk in audio_chunks:
            wf.writeframes(chunk)
        print("💾 Audio saved as 'streaming_audio.wav'")
        break
# Run the streaming example
asyncio.run(stream_tts())

```

### 
[​](http://docs.vogent.ai/voicelab/quickstart#why-use-websocket-streaming)
Why Use WebSocket Streaming?
WebSocket streaming is perfect for:
  * **Live chatbots** - Generate speech as the conversation progresses
  * **Real-time applications** - Immediate audio feedback
  * **Interactive experiences** - Dynamic content that changes based on user input
  * **Low-latency needs** - Start playing audio before the full text is processed


## 
[​](http://docs.vogent.ai/voicelab/quickstart#next-steps)
Next Steps
Congratulations! You’ve successfully generated your first AI voices. Here’s what to explore next:
## [Explore ModelsLearn about different AI models and their capabilities](http://docs.vogent.ai/voicelab/models)## [Voice LibraryBrowse our complete voice library and cloning options](http://docs.vogent.ai/voicelab/voices)## [API ReferenceDetailed API documentation with all parameters](http://docs.vogent.ai/api-reference/voicelab-tts)## [Advanced FeaturesDiscover advanced features like voice cloning and SSML](http://docs.vogent.ai/voicelab/voice-synthesis/advanced-features)
## 
[​](http://docs.vogent.ai/voicelab/quickstart#need-help)
Need Help?
  * **Documentation** : Explore our comprehensive [API documentation](http://docs.vogent.ai/api-reference/voicelab-tts)
  * **Support** : Contact our support team at support@vogent.ai
  * **Community** : Join our [Discord community](https://discord.gg/JmThYcyG) for discussions and tips
  * **Examples** : Check out more examples in our [GitHub repository](https://github.com/vogent/voicelab-examples)


[Introduction](http://docs.vogent.ai/voicelab/introduction)[Models](http://docs.vogent.ai/voicelab/models)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
Assistant
Responses are generated using AI and may contain mistakes.
