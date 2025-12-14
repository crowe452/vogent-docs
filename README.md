<p align="center">
  <img src="https://img.shields.io/badge/Context7-Ready-00D4AA?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIyIi8+PHBhdGggZD0iTTggMTJMIDExIDE1TDE2IDkiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMiIvPjwvc3ZnPg==" alt="Context7 Ready" />
  <img src="https://img.shields.io/badge/Docs-101%20Pages-blue?style=for-the-badge" alt="Documentation Pages" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License" />
  <img src="https://img.shields.io/badge/Voice%20AI-Vogent-purple?style=for-the-badge" alt="Vogent" />
</p>

<h1 align="center">Vogent Documentation</h1>

<p align="center">
  <strong>Community-maintained documentation for Vogent Voice AI platform</strong><br/>
  Optimized for <a href="https://context7.com">Context7</a> integration with AI code editors
</p>

<p align="center">
  <a href="https://docs.vogent.ai">Official Docs</a> •
  <a href="https://app.vogent.ai">Dashboard</a> •
  <a href="https://discord.gg/An5z6xhYfS">Discord</a> •
  <a href="#quick-start">Quick Start</a>
</p>

---

## What is Vogent?

Vogent is an all-in-one platform for building **humanlike, intelligent voice AI agents**. From outbound sales calls to inbound support, Vogent provides the infrastructure to deploy production-grade voice AI at scale.

### Key Capabilities

| Feature | Description |
|---------|-------------|
| **IVR Navigation** | Automatically detect and navigate phone trees with AI |
| **Voice Cloning** | Clone any voice or use Sesame CSM-1B ultra-low-latency TTS |
| **Flow Builder** | Visual interface for structured conversation paths |
| **Function Calling** | Real-time webhooks for dynamic decision-making |
| **Batch Dialing** | Scale outbound campaigns with queued dials |
| **HIPAA Compliance** | Enterprise-ready for healthcare applications |

---

## Quick Start

### Using with Context7

```bash
# In any Context7-compatible AI editor (Cursor, Windsurf, Claude Code, etc.)
use context7 /crowe452/vogent-docs
```

Or search for **"vogent"** in Context7's library search.

### API Authentication

```bash
# All API requests require Bearer token authentication
curl -X POST https://api.vogent.ai/api/dials \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"agentId": "...", "toNumber": "+1234567890"}'
```

Generate API keys at [app.vogent.ai](https://app.vogent.ai) → Settings → API Keys

---

## Documentation Structure

```
docs/
├── api-reference_*.md      # 30+ API endpoint docs
│   ├── create-a-new-dial   # Initiate outbound calls
│   ├── create-agent        # Configure voice agents
│   ├── clone-voice         # Voice cloning API
│   └── ...
│
├── platform-overview_*.md  # Platform guides
│   ├── how-vogent-works    # Architecture overview
│   ├── flow-builder        # Visual conversation design
│   ├── functions           # Webhook integrations
│   └── ...
│
├── quickstart_*.md         # Getting started guides
│
├── webhooks_*.md           # Event documentation
│   ├── dial-transcript     # Real-time transcripts
│   ├── function-call       # Dynamic webhooks
│   └── dial-status-updated # Call lifecycle events
│
├── voicelab_*.md           # Voice synthesis
│   ├── models              # Sesame CSM-1B, etc.
│   ├── fine-tuning         # Custom voice training
│   └── voices              # Voice library
│
└── telephony_*.md          # SIP/PSTN integration
    ├── twilio              # Twilio SIP trunking
    ├── telnyx              # Telnyx integration
    └── vonage              # Vonage setup
```

---

## API Quick Reference

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/dials` | POST | Create a new outbound dial |
| `/dials/{id}` | GET | Get dial status and transcript |
| `/agents` | POST | Create a voice agent |
| `/agents/{id}` | PATCH | Update agent configuration |
| `/voices` | GET | List available voices |
| `/voices/clone` | POST | Clone a voice from audio |
| `/batch-dial-jobs` | POST | Create batch dial campaign |
| `/functions` | POST | Register webhook function |

**Base URL:** `https://api.vogent.ai/api`

---

## Webhook Events

Vogent sends real-time webhooks for call lifecycle events:

| Event | Trigger |
|-------|---------|
| `dial.created` | Call initiated |
| `dial.updated` | Status change (ringing, answered, ended) |
| `dial.transcript` | New transcript segment available |
| `function_call` | Agent requests external data |

**Signature Verification:** Use `X-Elto-Signature` header with HMAC-SHA256

---

## Official Resources

| Resource | URL |
|----------|-----|
| Documentation | [docs.vogent.ai](https://docs.vogent.ai) |
| Dashboard | [app.vogent.ai](https://app.vogent.ai) |
| API Base | [api.vogent.ai/api](https://api.vogent.ai/api) |
| Discord | [discord.gg/An5z6xhYfS](https://discord.gg/An5z6xhYfS) |

---

## Contributing

Found an error or want to improve the docs?

1. Fork this repository
2. Make your changes
3. Submit a pull request

For major changes, please open an issue first to discuss.

---

## Disclaimer

This is a **community-maintained mirror** of Vogent documentation, optimized for Context7 integration. For official, up-to-date documentation, always refer to [docs.vogent.ai](https://docs.vogent.ai).

This project is not affiliated with, endorsed by, or sponsored by Vogent Inc.

---

<p align="center">
  <sub>Built for the AI-native development ecosystem</sub><br/>
  <a href="https://github.com/crowe452">@crowe452</a>
</p>
