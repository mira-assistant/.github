# Dadei

Dadei runs quietly in the background and pays attention to your conversations — understanding context, remembering what was said, and taking action when something needs to get done.

---

## The idea

Most AI assistants require you to stop what you're doing, phrase a command, and wait for a response. Dadei works the other way around. It listens passively across your devices, builds an episodic memory of your conversations over time, and surfaces actions automatically — scheduling a meeting you mentioned, drafting an email you said you'd send, or setting a reminder you nearly forgot.

You keep talking. Dadei keeps up.

---

## What it does

**Remembers your conversations** — every session is transcribed, attributed to the right speaker, and stored. The context doesn't disappear when the conversation ends. Ask Dadei what was decided last week, who committed to something, or what time a plan was made — and it will tell you, grounded in what was actually said through a RAG pipeline that combines semantic and keyword search across your history.

**Knows who's in the room** — Dadei identifies individual speakers through voice recognition and ties everything to the right person, so your history is always accurate and attributable.

**Acts on what it hears** — when a plan, commitment, or intention surfaces in conversation, Dadei parses it and follows through: creating calendar events in Google Calendar, sending texts, drafting emails, and setting reminders — without you needing to ask explicitly.

**Works across your devices** — run the client on multiple machines simultaneously. Dadei evaluates audio quality in real time and uses the clearest feed, so nothing is missed regardless of where you are in the room.

---

## Repositories

| Repo | Description |
|---|---|
| [`backend`](https://github.com/dadei-app/backend) | Core service — audio processing, speaker diarization, episodic memory, RAG pipeline, action execution |
| [`frontend`](https://github.com/dadei-app/frontend) | Browser-based client & Native desktop client for macOS, Windows, and Linux |
