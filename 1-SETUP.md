# Hotel Voice Agent — Setup Guide

Takes ~15 minutes. Three accounts needed: **VAPI** (voice), **n8n** (automation), **Airtable** (data).

## Step 1 — Airtable (5 min)
1. Create a base named after your hotel.
2. Build the tables in `airtable-schema.md` (copy-paste the fields).
3. Get your **Airtable Personal Access Token** (Create > API scopes: `data.records:read` + `data.records:write`) and your **Base ID** (from the API help). Keep both handy.

## Step 2 — n8n (5 min)
1. In n8n: **Workflows > Import from File** → choose `n8n-workflow.json`.
2. Open the workflow. On every Airtable node: add your credential (Airtartable Base ID + token from Step 1).
3. On the **Webhook** node, click **Execute Test Workflow** once, copy the production webhook URL (looks like `https://your-n8n/webhook/vapi-booking`).
4. Activate the workflow (toggle Active).

## Step 3 — VAPI (5 min)
1. Create a new Assistant.
2. Paste the **system prompt** from `vapi-assistant.md`.
3. Add the tools listed in `vapi-assistant.md`, each pointing at the n8n webhook URL from Step 2.
4. Buy / port a phone number in VAPI and assign it to this assistant.

## Step 4 — Test
Call your number. Try:
- "Do you have a room available this weekend?"
- "Book it — my name is ___, number ___"
- "Cancel my booking"

Confirm a row appears in Airtable every time.

---

**Need help?** Send screenshots of any n8n error and we'll debug.
