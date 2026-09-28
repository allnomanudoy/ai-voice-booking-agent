# AI Voice Booking Agent — VAPI + n8n + Airtable

A 24/7 AI phone receptionist that answers calls instantly, checks live availability, and books rooms automatically. No human on the line.

Built for **hotels, dental clinics, restaurants, and any business stuck on phone-based scheduling**.

## How it works

```
Caller  →  VAPI (AI voice, natural conversation)
        →  n8n (webhook trigger, routes the intent)
        →  Airtable (checks availability / creates booking)
        →  VAPI speaks the confirmation back to the caller
```

- Answers in under 1 second, 24/7.
- Understands "I want a King room, Oct 12–15, two guests".
- Writes every booking to a database row. Zero data entry errors.

## What's in this repo

| File | What it is |
|---|---|
| `n8n-workflow.json` | Importable n8n workflow (Webhook → Switch → Airtable → Respond) |
| `2-vapi-assistant.md` | VAPI system prompt + tool definitions, ready to paste |
| `3-airtable-schema.md` | Airtable tables: Rooms, Bookings, BlockedDates, CallLogs |
| `1-SETUP.md` | 15-minute setup guide |

## Quick start

1. Create the Airtable tables in `3-airtable-schema.md`.
2. Import `n8n-workflow.json` into n8n, add your Airtable credentials.
3. Paste the prompt + tools from `2-vapi-assistant.md` into VAPI.
4. Point VAPI's webhook at your n8n URL.
5. Call your number.

## Why this stack

- **VAPI** — handles the actual phone call and natural voice.
- **n8n** — visual automation; every step inspectable, no-code.
- **Airtable** — spreadsheet-simple database your client can actually use.

## Connect with me

I build these for businesses that want to stop missing after-hours calls.
LinkedIn: [Md. All Noman Udoy](https://www.linkedin.com/in/md-all-noman-udoy-7b8011252/)

## License

MIT — use it, fork it, build your own client versions.
