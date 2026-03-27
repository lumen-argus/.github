<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/Lumen_Argus-DLP_for_AI_Coding_Tools-4f46e5?style=for-the-badge&logo=shield&logoColor=white">
    <img src="https://img.shields.io/badge/Lumen_Argus-DLP_for_AI_Coding_Tools-4f46e5?style=for-the-badge&logo=shield&logoColor=white" alt="Lumen Argus">
  </picture>
</p>

<p align="center">
  <strong>Protect secrets, PII, and proprietary data from leaking through AI coding tools.</strong>
</p>

<p align="center">
  <a href="https://github.com/lumen-argus/lumen-argus"><img src="https://img.shields.io/github/license/lumen-argus/lumen-argus?style=flat-square" alt="License"></a>
  <a href="https://github.com/lumen-argus/lumen-argus/actions/workflows/test.yml"><img src="https://github.com/lumen-argus/lumen-argus/actions/workflows/test.yml/badge.svg" alt="Tests"></a>
  <a href="https://lumen-argus.github.io/lumen-argus/docs/"><img src="https://img.shields.io/badge/docs-mkdocs-blue?style=flat-square" alt="Docs"></a>
  <img src="https://img.shields.io/badge/python-3.11+-blue?style=flat-square&logo=python&logoColor=white" alt="Python 3.11+">
</p>

---

## What is Lumen Argus?

Lumen Argus is a **local HTTP proxy** that sits between AI coding tools (Claude Code, GitHub Copilot, Cursor, etc.) and their API providers. Every outbound request is scanned for sensitive data before it leaves your machine or network.

```
AI Coding Tool  ──>  Lumen Argus (proxy)  ──>  AI Provider
                          |
                 Scan for secrets, PII,
                 and proprietary data
                          |
                 Action: block | alert | redact | log
```

### Why?

AI coding assistants send your code context to external APIs on every request. This creates real data leak risks: API keys, database credentials, customer PII, and proprietary algorithms can all be transmitted without your knowledge.

## Projects

| Repository | Description |
|:-----------|:------------|
| [**lumen-argus**](https://github.com/lumen-argus/lumen-argus) | Core DLP proxy - detection engine, web dashboard, rule management, WebSocket support, MCP tool scanning |
| [**crossfire**](https://github.com/lumen-argus/crossfire) | Regex rule overlap analyzer - find duplicate and redundant detection rules across any rule set |

## Key Features

- **1,700+ detection rules** covering secrets, API keys, tokens, PII, and prompt injection
- **Real-time web dashboard** with findings, rule management, allowlists, and analytics
- **Multiple actions** per finding: block, alert, redact, or log
- **WebSocket and MCP support** for scanning bidirectional and tool-calling traffic
- **Rule overlap analysis** powered by Crossfire to eliminate redundant rules
- **Notification channels** for Slack, Teams, PagerDuty, Email, OpsGenie, Jira, and webhooks
- **Zero external dependencies at runtime** - pure Python with optional extras
- **Enterprise features** available with Pro license (NLP PII detection, SIMD acceleration, scheduled analysis, compliance reports)

## Getting Started

See the [documentation](https://lumen-argus.github.io/lumen-argus/docs/) for installation, configuration, and deployment guides.

## License

MIT
