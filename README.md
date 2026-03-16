<div align="center">
<img src="https://images.blackroad.io/pixel-art/road-logo.png" alt="BlackRoad OS" width="80" />

# Squad Webhook

**8 AI agents respond to @blackboxprogramming on GitHub PRs and issues. 69 repos hooked.**

[![BlackRoad OS](https://img.shields.io/badge/BlackRoad_OS-Pave_Tomorrow-FF2255?style=for-the-badge&labelColor=000000)](https://blackroad.io)
</div>

---

## Agents

| Agent | Specialty | Trigger |
|-------|-----------|---------|
| Lucidia | AI reasoning, deep analysis | @lucidia |
| Alice | DevOps, infrastructure | @alice |
| Octavia | Architecture, systems design | @octavia |
| Aria | Frontend, UX, design | @aria |
| Shellfish | Security, vulnerability scanning | @shellfish |
| Cecilia | Meta-cognitive, model evaluation | @cecilia |
| Caddy | Build systems, CI/CD | @caddy |
| Alexa | CEO review, final approval | @alexa |

## How It Works

```
GitHub webhook → Cloudflare Worker → Agent router → Response comment
```

1. Someone mentions `@blackboxprogramming` in a PR/issue
2. GitHub sends webhook to the Squad Worker
3. Worker identifies the right agent from context
4. Agent generates a review/response via Ollama
5. Response posted as a comment

## Commands

- `/status` — fleet overview
- `/assign @agent` — assign specific agent
- `@agent review this` — trigger agent review

## Stack

- Cloudflare Workers (JavaScript)
- GitHub Webhooks API
- Ollama inference (via fleet)

---

*Copyright (c) 2024-2026 BlackRoad OS, Inc. All rights reserved.*
