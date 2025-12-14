Voicelab

Models



              



  * [Voicelab Models](#voicelab-models)
  * [Featured Models](#featured-models)
  * [Sesame CSM-1B](#sesame-csm-1b)
  * [Dia](#dia)
  * [Orpheus](#orpheus)
  * [Coming Soon](#coming-soon)
  * [Model Specifications](#model-specifications)
  * [Supported Features](#supported-features)



Voicelab

# Models

Explore the available text-to-speech models and their capabilities

# 

[​](#voicelab-models)

Voicelab Models

Voicelab provides access to state-of-the-art open-source text-to-speech models.

## 

[​](#featured-models)

Featured Models

### 

[​](#sesame-csm-1b)

Sesame CSM-1B

**State-of-the-art conversational speech model** This model is **optimized** and certain voices are **professionally cloned**. This means that we offer fast, low-cost inference for this model, and that select voices will have more consistent quality.

  * **Parameters** : 1 billion
  * **Specialization** : Natural conversation and dialogue
  * **Languages** : English
  * **Key Features** : 
    * Exceptional naturalness in conversational contexts
    * Low latency inference
    * Consistent voice quality across long generations
    * Optimized for real-time applications



### 

[​](#dia)

Dia

**general-purpose TTS model**

This model is not yet optimized or post-trained. Generation quality may be inconsistent.

  * **Parameters** : 1.6 billion
  * **Specialization** : General-purpose text-to-speech
  * **Languages** : English
  * **Key Features** : 
    * Accepts emotive tokens (e.g. laughing, sighing)
    * Efficient inference
    * Less stable than CSM-1B

**Emotive Tags** : `(laughs)`, `(clears throat)`, `(sighs)`, `(gasps)`, `(coughs)`, `(singing)`, `(sings)`, `(mumbles)`, `(beep)`, `(groans)`, `(sniffs)`, `(claps)`, `(screams)`, `(inhales)`, `(exhales)`, `(applause)`, `(burps)`, `(humming)`, `(sneezes)`, `(chuckle)`, `(whistles)`

### 

[​](#orpheus)

Orpheus

**Expressive and emotional speech synthesis**

This model is not post-trained; the hosted weights are as-is.

  * **Parameters** : 750 million
  * **Specialization** : Emotional and expressive speech
  * **Languages** : English (primary)
  * **Key Features** : 
    * Advanced emotional control
    * Dynamic prosody and intonation
    * Character voice capabilities
    * Rich vocal expressions

**Emotive tags** : `<laugh>`, `<chuckle>`, `<sigh>`, `<cough>`, `<sniffle>`, `<groan>`, `<yawn>`, `<gasp>`

### 

[​](#coming-soon)

Coming Soon

Kokoro, Chatterbox, Kyutai TTS

## 

[​](#model-specifications)

Model Specifications

### 

[​](#supported-features)

Supported Features

Feature| Sesame CSM-1B| Dia| Orpheus  
---|---|---|---  
Voice Cloning| ✅| ✅| ✅  
Emotive Tokens| ❌| ✅| ✅  
Multi-speaker| ✅| ✅| ✅  
Real-time Streaming| ✅| ✅| ✅  
Custom Fine-tuning| ✅| ✅| ✅  
  
While CSM-1B doesn’t accept emotive tokens (laugh/sigh/etc.), it has the capacity to generate these artifacts in output audio based on conversational context.

[Quickstart](/voicelab/quickstart)[Voices and Voice Cloning](/voicelab/voices)