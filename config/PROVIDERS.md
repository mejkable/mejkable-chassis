# PROVIDERS.md — AI Service Configuration

## Purpose

This file maps which AI services or tools are used for which tasks across the chassis. The phase PROMPT.md files are written provider-agnostically — this file is where you configure your actual stack.

---

## Active Providers

| Provider | Type | Used For | Notes |
|---|---|---|---|
| [e.g., Claude Code / Codex / OpenCode] | Agent / IDE | Primary agent rail, document generation, analysis | — |
| [e.g., Midjourney / Nano Banana] | Image generation | Concept visualisation, mood boards | — |
| [e.g., ChatGPT / Claude.ai] | Agent | Brainstorming, synthesis | — |
| [e.g., Perplexity] | Research | Market research, competitive analysis | — |

---

## Provider Mapping by Task Type

These are the common task types that appear across phases. Map each to your preferred provider.

| Task Type | Default Provider | Fallback |
|---|---|---|
| Research & analysis | | |
| Writing & documentation | | |
| Image / visual generation | | |
| CAD / 3D modelling | | |
| Data analysis & costing | | |
| Competitive intelligence | | |
| User interview synthesis | | |
| Regulatory & compliance research | | |

---

## Switching Providers

When switching a provider for a task type:

1. Update this file
2. Review the relevant PROMPT.md files — the task framing should still work, but check for assumptions
3. Note the change in the project LOG.md

---

## Provider-Specific Notes

[Any quirks, API limits, formatting preferences, or context window constraints worth noting for each provider.]

