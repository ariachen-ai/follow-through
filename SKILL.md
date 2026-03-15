---
name: follow-through
description: Post-event networking follow-up and relationship management. Use when the user attended an event (hackathon, conference, mixer, meetup, dinner, summit, happy hour) and wants to follow up with new connections. Handles contact scanning, personalized message drafting, sending messages, social media post drafting (LinkedIn, Xiaohongshu/小红书, Twitter/X), and follow-up reminders with voice learning. Use when user says "I went to [event]", "scan my new contacts", "networking follow-up", "event follow-up", "draft messages for people I met", "post about [event]", "who did I connect with", or "follow up from [event]". Do NOT use for general LinkedIn browsing or social media posting unrelated to events.
---

# Follow-Through: Post-Event Networking

## Workflow

### Step 1: Collect Event Context
Gather (ask if not provided):
- Event name, type (hackathon / conference / mixer / meetup), date(s)
- Where contacts were added (LinkedIn, Luma, email, business cards — default LinkedIn)

### Step 2: Scan Connections
Scan the user's recently added connections around the event date (±1 day).

**LinkedIn (default):**
- Navigate to LinkedIn connections sorted "Recently added" via browser
- Collect: name, title/company, connected date

**Manual/CSV fallback:**
- User pastes a list of names, or provides a CSV/spreadsheet of contacts
- User can also say "here are the people I met: [names]" and agent builds the list

**Luma/Eventbrite:**
- If user has attendee list access, parse it for names and titles

Present numbered list for review.

### Step 3: Categorize by Action
Ask user to categorize by **what they want to do** (default all to 👋):

- ☕ **Coffee invite** — want to meet IRL. Add user's location-based coffee line.
- 🤝 **Collab** — user provides context: "we talked about X, I want to follow up on Y." Use their answer to write a deeply personalized message.
- 👋 **Stay in touch** — light, friendly, offer to share events. No context needed.

User can say: "Sarah — collab, we talked about AI communities. James — coffee. Rest stay in touch."

**Auto-detect Chinese contacts → write message in Chinese.**

### Step 4: Draft Messages
1. Read `references/voice-notes.md` for user's established writing style
2. Draft messages matched to action tier + voice profile:
   - ☕ Coffee: personalized + location-based coffee invite
   - 🤝 Collab: reference actual conversation topics user provided + specific collab ask
   - 👋 Stay in touch: short, warm, offer to share events
3. Present all drafts for review

### Step 5: Choose Send Method
Ask: **"Which ones do you want me to send, and which do you want to send yourself?"**

Options:
- "send all" → send everything via platform automation
- "send the warm ones, I'll do collab myself" → send warm, provide collab as text
- "I'll send them all" → just provide drafts to copy
- Specific names → send only those

**CRITICAL: Never send without user explicitly choosing. Stop immediately if user says stop. Report which were sent and which remain.**

#### Sending Messages

**LinkedIn (browser automation):**
1. Navigate to compose: `linkedin.com/messaging/compose/?recipient=[profileURN]`
2. Type approved message → Click Send
3. Confirm: "✅ Sent to [Name]"

**Email:**
1. Compose email to contact's address
2. Subject: "Great meeting you at [Event]!"
3. Send via user's email client/API

**iMessage / WhatsApp / Telegram:**
1. If user has contact's phone number, send via messaging platform
2. Use appropriate tone (more casual for messaging apps)

**Manual (any platform):**
1. Provide formatted draft text for user to copy-paste
2. Works with any platform — Twitter DMs, Discord, WeChat, LINE, etc.

### Step 6: Draft Social Posts (if requested)
Offer posts for:
- **LinkedIn** — professional recap, tag people, highlight themes
- **Xiaohongshu/小红书** — Chinese, visual/personal, lifestyle angle, hashtags (湾区活动, 科技圈, networking, 硅谷生活)
- **Twitter/X** — punchy, 1-2 takeaways, build-in-public energy
- **WeChat Moments / 朋友圈** — Chinese, casual, photo-forward

Study recent post trends on each platform before drafting. If user has event photos, suggest including them.

### Step 7: Log and Remind
1. Log event + contacts to a persistent file (e.g. `memory/networking.md` or equivalent)
2. Log all drafted messages for future reference
3. Set **1-month follow-up reminder** for ☕ and 🤝 contacts
   - Use cron/scheduled tasks if available
   - Otherwise, remind user to set a calendar event
4. Include person names, event name, and context in reminder text

#### Follow-Up Reminder Flow (when reminder fires)
1. Surface the original contact list with action tiers and conversation context
2. Ask user: "Want to check in with these people? I can draft follow-up messages."
3. Draft follow-up messages referencing the original conversation + time passed
4. Same send flow as Step 5

### Step 8: Learn from Feedback Loop
After user sends their own messages:
1. Ask user to share what they actually sent, or check sent messages if browser available
2. Compare drafts vs actual for each contact
3. Update `references/voice-notes.md` with:
   - What user changed (tone, length, phrases, structure)
   - What user kept (validates the draft)
   - New patterns (language switching, emoji preferences, value offers)
4. Apply all learnings to future drafts — the skill gets smarter every time

## Event Log Format

```
## [Event Name] — YYYY-MM-DD
Type: hackathon | conference | mixer
Contacts:
- ☕ Name — Title @ Company
- 🤝 Name — Title @ Company — [collab context]
- 👋 Name — Title @ Company
Posts: [links or "pending"]
Follow-up: YYYY-MM-DD
```

## Voice Profile
Before drafting any message, read `references/voice-notes.md`. If it's empty (first use), draft messages in a warm, casual tone and start learning from user's edits.

Key principles:
- Match user's language to recipient's language (Chinese contacts → Chinese)
- Always offer value, not just "nice to meet you"
- Collab messages MUST have conversation context from user — never guess from LinkedIn bios
- Short messages for stay-in-touch, longer for collab
- Adapt to user's emoji, humor, and greeting style over time

## Platform Compatibility

This skill is designed to work with any AI agent framework:

| Feature | Full Support | Partial Support | Manual Fallback |
|---------|-------------|-----------------|-----------------|
| LinkedIn scan | Browser automation | User pastes list | User provides names |
| Send messages | Browser / email API | Copy-paste drafts | User sends manually |
| Reminders | Cron / scheduled tasks | Calendar invite | User sets own reminder |
| Voice learning | File-based memory | Session memory | User re-describes style |

**Works with:** Claude.ai, Claude Code, OpenClaw, ChatGPT, Cursor, any agent that can read markdown instructions.

## Troubleshooting

### No browser available
Skip LinkedIn scanning. Ask user to paste their new connections list or share a screenshot. Draft messages as text for user to copy-paste.

### LinkedIn not loading
Cause: Browser session expired
Solution: Re-authenticate or switch to manual mode

### User aborts sending
Stop immediately. Report which messages were sent and which remain. Never retry without asking.

### No conversation context for collab tier
Do NOT guess or use LinkedIn bio as substitute. Ask user: "What did you talk about with [Name]? What do you want to follow up on?"
