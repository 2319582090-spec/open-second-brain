# Existing Tools and Projects

This document tracks existing tools that may help build an open 24-hour AI-native second brain. Inclusion does not mean endorsement.

## Capture and Lifelogging

### Screenpipe

- Link: https://docs.screenpi.pe/
- Role: desktop screen, audio, OCR, app activity, browser context, local-first capture.
- Why it matters: closest fit for 24/7 computer memory.
- Questions: storage cost, consent defaults, long-term retention, MCP integration maturity.

### Omi

- Link: https://docs.omi.me/doc/developer/api/overview
- Role: wearable and mobile conversation memory, transcripts, memories, action items, MCP, API.
- Why it matters: strong candidate for real-world audio and wearable memory.
- Questions: hardware availability, cloud dependency, export quality, local processing options.

### Pieces OS

- Link: https://docs.pieces.app/products/core-dependencies/pieces-os/quick-menu
- Role: developer and work-context long-term memory.
- Why it matters: practical memory for code, docs, chats, browser context, and MCP clients.
- Questions: data ownership, export, non-developer workflows.

## AI Memory Infrastructure

### Graphiti

- Link: https://help.getzep.com/graphiti/getting-started/welcome
- Role: temporal knowledge graph for evolving facts and relationships.
- Why it matters: second brains need time-aware memory, not only vector search.
- Questions: personal-memory schema, local deployment, MCP integration.

### Mem0 / OpenMemory

- Link: https://github.com/mem0ai/mem0
- Role: AI agent memory, user preferences, durable facts, MCP memory layer.
- Why it matters: useful for sharing memory across AI tools.
- Questions: privacy boundaries, user-facing review, conflict resolution.

### Supermemory

- Link: https://github.com/supermemoryai/supermemory
- Role: shared memory for AI tools, browser extension, API, MCP-oriented workflows.
- Why it matters: simple path for AI apps to share user memory.
- Questions: local-first options, raw data policy, personal data export.

## Model Providers and AI Interfaces

### Local LLMs

- Examples: Ollama, llama.cpp, local multimodal models.
- Role: private summarization, extraction, tagging, and local recall.
- Why it matters: raw sensitive memory should not require cloud processing.

### Doubao / Volcengine Ark

- Link: https://www.volcengine.com/product/ark
- Role: Chinese-language reasoning, multimodal processing, cloud model API, OpenAI-compatible integration patterns.
- Why it matters: useful for high-quality Chinese summaries and model routing.
- Questions: pricing, data retention, privacy guarantees, API compatibility.

### MCP Clients

- Examples: Codex, Cursor, Claude Desktop, ChatGPT-compatible tools where supported.
- Role: give AI tools controlled access to personal memory.
- Why it matters: memory should be available in the tools people already use.

## Hardware Categories

### Audio Pendants

- Examples: Omi, Plaud, other wearable recorders.
- Role: real-world conversation capture.
- Requirements: consent, visible recording, export, retention, local processing if possible.

### Smart Glasses

- Examples: Omi Glass, Ray-Ban Meta, developer kits.
- Role: first-person image/video context.
- Requirements: strict privacy controls, short default retention, visible indicators, bystander consent.

### Phones

- Role: camera roll, location, health, voice notes, messages where legal and permitted.
- Requirements: user-controlled permissions, encrypted sync, cross-platform support.

### Home and Environment Devices

- Examples: cameras, presence sensors, smart home events.
- Role: optional environmental memory.
- Requirements: avoid blanket surveillance; prefer event summaries over raw long-term video.

## Evaluation Criteria

We evaluate tools by:

- Does it capture useful context automatically?
- Does it support local-first or user-owned data?
- Does it expose API, MCP, export, or integration hooks?
- Can it work with multiple AI models?
- Does it handle retention, deletion, and consent?
- Can it support a 24-hour memory system without overwhelming storage or the user?

