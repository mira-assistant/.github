# Mira

Mira is a voice-activated AI assistant that pays attention so you don't have to. It listens passively across your devices, understands the context of your conversations, and takes action — scheduling meetings, sending messages, drafting emails, and setting reminders — all from natural speech, without you ever touching a keyboard.

---

## How it works

Most AI assistants are stateless. You ask a question, get an answer, and the context disappears. Mira is different: every conversation is transcribed, attributed to the right speaker, and stored in an episodic memory that persists across sessions. When you ask a follow-up hours or days later, Mira retrieves the relevant context through a RAG pipeline that combines semantic search with keyword matching — so answers are grounded in what was actually said, not hallucinated from scratch.

Natural language processing runs continuously in the background, extracting plans, commitments, and intentions from your conversations as they happen. When Mira detects something actionable, it surfaces it and acts on it.

---

## What Mira can do

**Remember who said what** — Mira identifies individual speakers through voice recognition and ties every interaction to the right person, so your conversation history is always accurate and attributable.

**Take action from speech** — say you want to grab lunch on Friday, follow up with someone, or be reminded about a deadline. Mira parses the intent and turns it into a calendar event, a text, or an email — no explicit commands required.

**Connect to your tools** — Mira integrates with Google Calendar to schedule events directly, and can send messages and emails on your behalf using context it has already gathered from the conversation.

**Answer questions about past conversations** — ask Mira what was decided in last week's discussion, who said they'd handle something, or what time something was planned for. The episodic memory and RAG pipeline surface the right answer from your actual history.

**Run across multiple devices** — open a client on your laptop and your desktop simultaneously. Mira evaluates audio quality in real time and uses the clearest feed, so the experience is seamless regardless of which machine you're closest to.

---

## Repositories

| Repo | Description |
|---|---|
| [`backend`](https://github.com/mira-assistant/backend) | Core service — audio processing, speaker diarization, episodic memory, RAG pipeline, action execution |
| [`desktop-app`](https://github.com/mira-assistant/desktop-app) | Native client for macOS, Windows, and Linux |
| [`web`](https://github.com/mira-assistant/web) | Browser-based client — same experience, no install required |
