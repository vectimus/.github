## Deterministic governance for AI agents. Open source. Sub-10ms. Zero config.

AI coding agents and agentic frameworks can run shell commands, write files, call APIs and invoke MCP tools. Vectimus intercepts every action and evaluates it against Cedar policies before execution. Same input, same decision, every time.

```
pipx install vectimus
vectimus init
```

Two commands. 78 policies. Your agents governed before they execute.

---

### Repositories

| | |
|---|---|
| **[vectimus](https://github.com/vectimus/vectimus)** | The core policy engine. Persistent daemon evaluates Cedar policies in under 10ms with zero telemetry. Works with Claude Code, Cursor, GitHub Copilot, Gemini CLI, LangGraph, Google ADK and the Claude Agent SDK. Apache 2.0. |
| **[policies](https://github.com/vectimus/policies)** | 78 Cedar rules across 11 policy packs: destructive ops, secrets, supply chain, infrastructure, code execution, data exfiltration, file integrity, database, git safety, MCP safety and agent governance. Every rule traces to a real incident and maps to OWASP, NIST, SOC 2 and ISO 27001 controls. |
| **[sentinel](https://github.com/vectimus/sentinel)** | Autonomous threat-to-policy pipeline. Three AI agents scan the agentic AI threat landscape daily, draft Cedar policies, prove them against reconstructed attacks in a sandbox, then open PRs for human review. Sentinel's own tool calls are governed by Vectimus. |

---

### How it works

```
Agent tool call ──> Vectimus daemon ──> Cedar policy evaluation ──> Allow / Deny
                         |
                    Signed audit receipt (Ed25519)
```

- **Deterministic** -- No LLM in the governance loop. Cedar policies, not probability.
- **Local** -- Everything evaluates on your machine. No telemetry, no account, no cloud calls.
- **Fast** -- Persistent daemon keeps the Cedar engine warm. Sub-10ms per evaluation.
- **Observable** -- Cryptographically signed audit receipts for every decision. Start in observe mode, enforce when ready.
- **Incident-driven** -- Sentinel discovers real-world attacks and ships verified policies daily.

### Compliance coverage

OWASP Agentic Top 10 (all 10 categories) | SOC 2 | NIST AI RMF | NIST CSF 2.0 | ISO 27001 | EU AI Act | SLSA | CIS Controls

---

<p align="center">
  <a href="https://vectimus.com">Website</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;<a href="https://vectimus.com/docs">Docs</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;<a href="https://vectimus.com/blog">Blog</a>
</p>
