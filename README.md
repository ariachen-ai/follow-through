# 🎉 Follow-Through

**Turn event connections into lasting relationships — automatically.**

You go to a hackathon, conference, or mixer. You meet 15+ people. You connect on LinkedIn. Then... nothing happens.

This skill fixes that.

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

## Installation

### Claude Code
```bash
/plugin install follow-through
```
Or clone and point to the skill folder.

### Claude.ai
1. Download this repo as a zip
2. Upload via Settings → Capabilities → Skills

### OpenClaw
Place the skill folder in your `skills/` directory.

### Any Other Agent (ChatGPT, Cursor, etc.)
Copy the contents of `SKILL.md` into your agent's system prompt or instructions. The skill is plain markdown — no framework lock-in.

## File Structure

```
post-event-networking/
├── SKILL.md                          # Core instructions
├── README.md                         # You're reading this
└── references/
    ├── message-templates.md          # Starting templates
    └── voice-notes.md                # Learned voice profile (evolves)
```

## Example

```
You: I went to a hackathon on Friday

Agent: Found 18 new LinkedIn connections. Here's the list:
       1. Sarah — Community Builder @ AI Collective
       2. James — Ex-Amazon Principal Engineer
       3. Wei — Stanford ML Researcher
       ...

       How do you want to categorize them?
       ☕ Coffee | 🤝 Collab (give me context) | 👋 Stay in touch

You: Sarah — collab, we talked about AI communities and hosting
     workshops for women in tech. James — coffee. Rest stay in touch.

Agent: Here are your drafts:

       Sarah: "Hi Sarah! It was so great meeting you at the hackathon.
       I love what you're building with AI Collective 🧃 I'd love to
       explore hosting workshops together for women in tech. Let me
       know if you'd be down to chat more about this!"

       James: "Hi James! Really enjoyed talking at the hackathon...
       If you're ever around Mountain View, let me know — I'd love to
       grab a coffee ☕"

       [15 stay-in-touch messages]

       Which ones should I send for you?

You: Send the stay-in-touch ones, I'll do Sarah and James myself

Agent: ✅ Sent to Alex
       ✅ Sent to Priya
       ...
       📝 Sarah and James drafts ready for you to copy
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

Compatible with [Claude Agent Skills](https://agentskills.io), [Claude Code](https://docs.anthropic.com/en/docs/claude-code), [OpenClaw](https://openclaw.ai), and any agent framework that supports the Agent Skills standard.

---

**Star ⭐ if this is useful! PRs welcome.**
