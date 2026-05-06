# Open Second Brain Architecture

Open Second Brain is a reference architecture for a 24-hour AI-native personal memory system. The architecture is designed around capture, understanding, memory, interfaces, and governance.

## 1. Capture Layer

The capture layer collects raw or semi-structured personal context from software and hardware.

Primary sources:

- Desktop: screen frames, OCR text, audio, window titles, browser URLs, app activity, local files.
- Mobile: photos, videos, audio notes, location, health data, calendar, notifications where allowed.
- Wearables: audio pendants, smart glasses, watches, sensors, health devices.
- Home and environment: cameras, microphones, smart home events, presence sensors.
- Manual input: quick notes, voice notes, tags, corrections, private journals.

Capture should support retention controls from the beginning. Raw audio and video should have short default retention unless the user explicitly saves them.

## 2. Understanding Layer

The understanding layer turns raw data into searchable, human-readable memory objects.

Core tasks:

- OCR for screen and image text.
- Speech-to-text for conversations and audio notes.
- Image and video understanding for scenes, objects, documents, faces, and activities.
- Entity extraction for people, places, projects, files, companies, tasks, and decisions.
- Summarization for daily, weekly, project, relationship, and health timelines.
- Intent and action extraction for follow-ups, reminders, open loops, and decisions.

This layer should support local models for private data and cloud models for allowed summaries or high-value reasoning.

## 3. Memory Layer

The memory layer stores structured events, semantic chunks, relationships, timelines, preferences, and durable facts.

Recommended memory types:

- Episode memory: what happened, when, where, and from which source.
- Semantic memory: extracted facts, concepts, notes, summaries, and references.
- Entity memory: people, projects, places, devices, organizations, and relationships.
- Temporal graph memory: facts and relationships that change over time.
- Agent memory: preferences and durable rules used by AI tools.
- Archive memory: cold storage for raw files and exported records.

## Canonical Episode Schema

Each captured event should be normalized into an episode object:

```json
{
  "id": "episode_...",
  "source": "screenpipe|omi|pieces|mobile|manual|camera|other",
  "modality": "text|audio|image|video|activity|sensor|mixed",
  "start_time": "2026-05-06T09:00:00Z",
  "end_time": "2026-05-06T09:30:00Z",
  "raw_ref": "local://...",
  "transcript": "",
  "summary": "",
  "entities": [],
  "locations": [],
  "people": [],
  "projects": [],
  "tasks": [],
  "privacy_level": "private|personal|shareable|public",
  "retention_days": 14,
  "confidence": 0.8
}
```

## 4. Interface Layer

The interface layer makes memory useful.

Interfaces should include:

- Desktop app for review, search, and permission management.
- Mobile app for capture, daily review, and quick correction.
- Browser extension for web context and saved pages.
- MCP servers for Codex, Cursor, Claude, ChatGPT-compatible clients, and other AI tools.
- REST or local API for integrations.
- Export format for user-owned data portability.

## 5. Governance Layer

Governance is part of the product, not an afterthought.

Required controls:

- Local-first raw storage where possible.
- End-to-end encrypted sync for selected data.
- Consent-aware recording indicators and capture modes.
- Retention policies for raw audio, video, screenshots, and location.
- Redaction for sensitive people, locations, passwords, private documents, and minors.
- Full export and deletion.
- Audit log for cloud model calls and external sharing.

## MVP Architecture

The first practical MVP should connect:

- Screenpipe for desktop screen/audio/OCR capture.
- Omi or a similar wearable/mobile capture tool for conversations.
- Pieces OS for development and work context.
- Graphiti for temporal knowledge graph memory.
- Mem0/OpenMemory or Supermemory for AI-tool shared memory.
- Local LLMs for private summaries and cloud LLMs only for approved tasks.

## Open Questions

- What should be captured continuously, and what should require explicit action?
- What is the right default retention for raw audio, video, and screenshots?
- How should bystander consent work for smart glasses and audio pendants?
- Which schema should become the open interchange format for personal memory?
- How should AI tools ask for permission before retrieving sensitive memory?

