# Voice Profile

This file captures the user's messaging style. It starts empty and evolves as the skill learns from the user's actual sent messages.

## How This Works
1. First use: the skill drafts messages in a warm, casual tone
2. User edits or rewrites the drafts, then sends their own version
3. The skill compares drafts vs actual and documents patterns below
4. Each event, the drafts get closer to the user's real voice

---

## Learned Patterns

<!-- The skill fills this section automatically after comparing drafts vs user's actual messages -->

### Collab Messages (people with specific follow-up)
<!-- Example patterns to learn:
- Does the user reference specific conversation topics?
- Do they offer value first?
- Do they add humor? What kind?
- Do they mention future touchpoints (events, trips)?
- How specific are their collab asks?
-->

### Stay-in-Touch Messages (casual connections)
<!-- Example patterns to learn:
- How long are these? (1-2 sentences? longer?)
- What's the greeting style? (Hey / Hi / hii / yo)
- Do they offer something? (events, resources, intros)
- What emoji do they use?
-->

### Tone & Style
<!-- Example patterns to learn:
- Formal vs casual?
- Emoji preferences (which ones, how often)
- Humor style (haha, lol, :D, jokes)
- Capitalization habits
- Punctuation quirks
-->

### Language Rules
<!-- Example patterns to learn:
- Do they switch languages for certain contacts?
- What triggers the switch? (contact's name, shared language, context)
- How does tone differ across languages?
-->

### What User Changed from Drafts
<!-- Log specific changes here after each event. Examples:
- Dropped [emoji] → uses [emoji] instead
- Added [phrase] that wasn't in draft
- Changed [generic phrase] to [specific reference]
- Switched language for [contact]
-->

### What User Kept from Drafts
<!-- Log what worked. Examples:
- Kept the joke about [topic]
- General structure for warm messages worked
- Coffee invite phrasing was good
-->

---

## Draft Quality Targets
- Collab messages: MUST ask user for conversation context first — never guess
- Warm messages: short, offer value, detect recipient's language
- Always personalize — never send something that could apply to anyone
