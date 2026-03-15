# 🎉 Follow-Through

**Turn event connections into lasting relationships — automatically.**

You go to a hackathon, conference, or mixer. You meet 15+ people. You connect on LinkedIn. Then... nothing happens.

This skill fixes that.

---

## 🎬 Demo: From Hackathon to Follow-Up in 2 Minutes

> **Friday night:** You just left a hackathon. You met 18 people. You're tired. You connected on LinkedIn in the Uber home.
>
> **Saturday morning:** You tell your agent "I went to a hackathon yesterday."

**What happens next:**

```
You: I went to a hackathon yesterday

Agent: 🔍 Scanning your LinkedIn...
       Found 18 new connections from March 14-15. Here's everyone:

       1.  Sarah Kim — Community Builder @ AI Collective
       ...and 18 more

       How do you want to follow up?
       ☕ Coffee  |  🤝 Collab (tell me what you talked about)  |  👋 Stay in touch
```
```
You: Sarah — collab, we talked about hosting AI workshops for women in tech.
     James — coffee.
     Rest stay in touch.
```
```
Agent: Here are your drafts:

  🤝 Sarah: "Hey Sarah! So great meeting you at the hackathon — I loved
  hearing about what you're building with AI Collective... Let me know
  if you'd be down to chat more about this! 😊"

  ☕ James: "..."
  ...and more drafts ready

  Which ones should I send for you, and which do you want to send yourself?
```
```
You: Send the stay-in-touch ones for me. I'll send Sarah, James, and Wei myself.

Agent: Sending...
       ✅ Priya — sent
       ✅ ... (x more sent)

       📝 Sarah, James, and Wei drafts ready for you to copy.
       ⏰ Follow-up reminder set for April 15 for Sarah, James, and Wei.
```

> **Total time: ~2 minutes.** 18 personalized messages. Zero copy-paste from a template. Chinese messages for Chinese contacts. And in a month, you'll get a reminder to check back in.

---

## Before & After

| Without Follow-Through | With Follow-Through |
|----------------------|---------------------|
| Meet 18 people at event | Meet 18 people at event |
| Connect on LinkedIn | Connect on LinkedIn |
| "I'll message them tomorrow" | Agent scans + drafts in 30 seconds |
| Tomorrow never comes | You review, pick send method, done |
| 3 months later: "who was that?" | 1-month reminder: "Check in with Sarah about workshops" |
| Generic "Great meeting you!" if anything | Messages in YOUR voice, in their language |

---

## The Problem

Every builder has experienced this:
1. Attend amazing event, meet incredible people
2. Connect on LinkedIn
3. ...crickets
4. 3 months later: "who was that person again?"

The follow-up is where relationships are built — but it's also the most tedious part.

## How It Works

Tell your AI agent "I went to [event]" and it handles the rest:

### 1. Scan → Find Your New Connections
Agent opens your LinkedIn, finds everyone you connected with around the event date.

### 2. Categorize → By What You Want to Do

This skill uses **action-based tiers**:

| Action | You Provide | Agent Drafts |
|--------|------------|--------------|
| ☕ **Coffee** | Nothing | Warm message + your location-based invite |
| 🤝 **Collab** | "We talked about X" | Deeply personalized message referencing your actual conversation |
| 👋 **Stay in touch** | Nothing | Short, friendly, offers to share future events |

### 3. Draft → In Your Voice (Not AI Slop)

The skill maintains a **voice profile** that learns from you:
- First event: starts with templates
- You send messages, agent studies what you actually wrote vs the draft
- Next event: drafts sound like *you* — your humor, emoji preferences, even language switching

### 4. Send → You Choose

"Send the stay-in-touch ones for me, I'll handle collab myself."

Agent can send via LinkedIn browser automation, or just give you text to copy. Your choice. You're always in control.

### 5. Post → LinkedIn, 小红书, Twitter/X

Event recap posts drafted for each platform:
- **LinkedIn** — professional, tag people, highlight themes
- **Twitter/X** — punchy, build-in-public energy
- **Ins/Xiaohongshu** — visual, lifestyle angle

### 6. Remind → Don't Let It Go Cold

1-month follow-up reminders for coffee and collab connections. Includes names, event, and conversation context so you remember who they are.

## What Makes This Different

### Voice Learning
Most AI tools draft generic messages. This skill studies the *difference* between what it drafted and what you actually sent, then improves. After 2-3 events, drafts sound genuinely like you.

**Example of what it learns:**
- "She uses 😊 not 🙌"
- "She writes in Chinese to Chinese contacts"
- "She always offers to share events (value-first)"
- "She adds humor with ':D' and 'haha'"
- "For collab messages, she references specific conversation topics"

### Multilingual
Auto-detects Chinese contacts and writes in Chinese. Supports bilingual Xiaohongshu posts.

## Platform Support

Built for **OpenClaw** and **Claude Code** — where you get the full experience:
- 🔍 LinkedIn scanning via browser automation
- 📨 Send messages directly from LinkedIn
- 🧠 Voice learning that persists across sessions
- ⏰ Automated follow-up reminders (cron)
- 🔄 Feedback loop that improves drafts over time

The skill is plain markdown, so you can adapt it for other agent frameworks — the core workflow (categorize → draft → review → send) works anywhere. Browser automation and persistent memory will need your own setup.

## Installation

### OpenClaw
Place the skill folder in your `skills/` directory.

### Claude Code
```bash
/plugin install follow-through
```
Or clone and point to the skill folder.

## File Structure

```
post-event-networking/
├── SKILL.md                          # Core instructions
├── README.md                         # You're reading this
└── references/
    ├── message-templates.md          # Starting templates
    └── voice-notes.md                # Learned voice profile (evolves)
```

## Design Decisions

**Why action-based tiers?** "Hot" doesn't tell the agent anything actionable. You might have had an amazing conversation but just want to stay in touch. Actions are practical.

**Why voice learning?** Generic AI networking messages are cringe. By studying what you actually send, the skill captures your real voice.

**Why not auto-send everything?** These messages go out under your name to real people. You should always choose what gets sent automatically.

## Contributing

PRs welcome! Especially:
- New platform support (WeChat, LINE, etc.)
- Better voice learning patterns
- Templates for different event types

## License
MIT

## Author
Built by [Aria Chen](https://linkedin.com/in/ariac) after attending a hackathon and realizing follow-up is the hardest part of networking 💌

Built on the [Agent Skills](https://agentskills.io) standard. Full experience on [OpenClaw](https://openclaw.ai) and [Claude Code](https://docs.anthropic.com/en/docs/claude-code). Adaptable to other frameworks.

---

**Star ⭐ if this is useful! PRs welcome.**
