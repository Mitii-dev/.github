
<div align="center">
  <strong>Local-first AI coding agent</strong><br />
  Repository-aware context · Controlled execution · Your models

  <a href="https://marketplace.visualstudio.com/items?itemName=mitii.mitii-ai-agent"><img alt="VS Code Marketplace" src="https://img.shields.io/badge/VS%20Code-Marketplace-007ACC?logo=visualstudiocode" /></a>
  <a href="https://github.com/Mitii-dev/Mitii"><img alt="License: AGPL v3" src="https://img.shields.io/badge/License-AGPL_v3-blue.svg" /></a>
  <img alt="Status" src="https://img.shields.io/badge/status-early%20access-ff751f" />
</div>

---

> [!WARNING]
> **Website and docs are in progress.**  
> Please wait for the public release — or, if you’re curious now, use **module-specific READMEs** inside the monorepo (e.g. `packages/v8/`, `apps/vscode/`, `packages/sdk/`).  
> [mitii.dev](https://mitii.dev) and [docs.mitii.dev](https://docs.mitii.dev) are not the source of truth yet.

---

## What is Mitii?

Mitii is a **local-first AI coding agent** for VS Code. It indexes your repository, reasons with bounded context, and applies changes under approvals and checkpoints — with local models (Ollama, LM Studio) or any OpenAI-compatible / Anthropic / Gemini endpoint.

Not “chat that dumps a patch.” A short, inspectable loop:

```text
[mitii] 1. MEASURE   ➔ Indexed 128 files | Scope: 14k tokens
[mitii] 2. IDENTIFY  ➔ Symbol resolution complete | Root cause pinned to auth.ts:42
[mitii] 3. TASK      ➔ Drafted Plan/Act contract | 3 files targeted for edit
[mitii] 4. IMPLEMENT ➔ Patch applied | Git checkpoint saved (stash@0)
[mitii] 5. IMPROVE   ➔ TypeScript build clean | 12/12 unit tests passing
```

---

## Start here

| | |
| --- | --- |
| **Product** | [Mitii](https://github.com/Mitii-dev/Mitii) — monorepo (VS Code extension, CLI, V8 runtime, SDK) |
| **Install** | [VS Code Marketplace — Mitii AI Agent](https://marketplace.visualstudio.com/items?itemName=mitii.mitii-ai-agent) |
| **Architecture** | [`packages/v8/ARCHITECTURE.md`](https://github.com/Mitii-dev/Mitii/blob/main/packages/v8/ARCHITECTURE.md) |
| **Extension** | [`apps/vscode/README.md`](https://github.com/Mitii-dev/Mitii/blob/main/apps/vscode/README.md) |
| **Issues** | [Mitii-dev/Mitii/issues](https://github.com/Mitii-dev/Mitii/issues) |

---

## Org focus

We build **agent infrastructure you can inspect**: hybrid retrieval, decision policy, tool runtime, verification — host-neutral runtime (`@mitii/v8`) behind thin hosts (VS Code, CLI).

```text
VS Code / CLI  →  @mitii/sdk  →  @mitii/v8  →  models + tools + index
```

**Privacy-first by default.** Run fully local when you want; cloud when you need more capacity.

---

<div align="center">
  <sub>>Mitii.dev_ · Measure → Identify → Task → Implement → Improve</sub>
</div>
