---
name: creator-agent
description: >
  Run the full end-to-end content creation workflow — ideas, script, and title/thumbnail optimization
  in one automated sequence. Use this skill when the user wants a complete content package without
  manually invoking each tool separately.
  Trigger for phrases like: "full content package for X", "plan, script, and optimize a video about X",
  "help me with everything for X", "do the whole thing for X", "end-to-end content for X",
  "complete content workflow", "give me everything I need for a video about X", or "do it all for X".
  Always use this skill when the user wants a multi-step content workflow in a single session.
---

# Creator Agent

Runs the full content creation pipeline: ideas → script → title/thumbnail optimization → platform caption. Each step builds on the previous one.

---

## Step 1: Gather

Before starting the workflow, confirm these inputs. If any are missing, ask the user — all at once in a single message:

| Input | Why it matters |
|---|---|
| **Topic** | What the content is about |
| **Platform** | YouTube, TikTok, Instagram, LinkedIn, Twitter/X (affects script length and caption style) |
| **Target audience** | Who will watch/read it |
| **Tone** | Funny, serious, educational, hype, conversational, etc. |
| **Video length** | Short-form (under 60s), mid-form (2–5 min), or long-form (8–20 min) |
| **Pace** | "Guide me through each step" or "just do the whole thing" |

If the user says anything like "just go", "do it all", "surprise me", or "your call" — choose sensible defaults and proceed through all steps without pausing for confirmation.

---

## Step 2: Ideas

Run the content-ideas step for the topic.

1. Generate **5 distinct content concepts** for the topic and platform. For each, provide:
   - Title / hook
   - Format (Reel, Long-form, Thread, etc.)
   - Angle (Educational, Controversial, Story, etc.)
   - One-sentence "why it works" note

2. Present the 5 ideas clearly:

```
💡 CONTENT IDEAS: [Topic] — [Platform]

1. [Title / Hook]
   Format: [format]
   Angle: [angle]
   Why it works: [one sentence]

2. ...
```

3. **If the user is guiding**: Ask "Which concept do you want to develop? (Pick a number or say 'best one' and I'll choose.)"
4. **If the user said "just go"**: Pick the strongest concept (highest-potential hook + broadest appeal) and announce which one you chose before proceeding.

---

## Step 3: Script

Run the video-scriptwriter step for the chosen concept.

Write the full script using the gathered inputs (platform, tone, length, audience). Follow the video-scriptwriter skill's formatting rules:

- Include `[HOOK]`, `[BODY]` / scene sections, and `[CTA]` labels
- Match the tone and length to the platform
- Write like the creator will speak it — conversational, not robotic

Output format:

```
🎬 VIDEO SCRIPT: [Title]
Format: [YouTube Long-form / TikTok / etc.]
Estimated length: [X min / X sec]
Tone: [Tone]
Audience: [Audience]

---

[HOOK]
...

[BODY]
...

[CTA]
...
```

**If the user is guiding**: After showing the script, ask: "Script is done — want me to run title/thumbnail optimization now? (yes / tweak the script first)"
**If the user said "just go"**: Proceed directly to Step 4.

---

## Step 4: Optimize

Run the thumbnail-title-optimizer step for the script.

Generate **5 title options** with CTR scoring and a thumbnail design brief:

```
🎯 TITLE OPTIONS: [Topic]

1. [Title]
   CTR Score: [X/10]
   Why: [one sentence — what makes it click-worthy]

2. ...

---

🖼️ THUMBNAIL BRIEF

Concept: [Visual concept in one sentence]
Text overlay: "[Short punchy text, max 4 words]"
Focal point: [What the viewer's eye goes to first]
Color palette: [2–3 colors and why]
Emotion/expression: [If a face is shown, what expression and why]
Style: [Minimal / Bold / Cinematic / etc.]
```

**If the user is guiding**: After the optimization, ask: "Want me to write the platform-specific caption/description for this video?"
**If the user said "just go"**: Proceed directly to Step 5.

---

## Step 5: Platform CTA

Write the platform-specific caption or video description for the chosen platform.

Follow the caption style for each platform:

### YouTube
- Write a full video description (150–300 words)
- Include: hook paragraph, key timestamps placeholder, relevant keywords naturally embedded, links section placeholder, subscribe CTA
- Tone: matches the video tone

### TikTok
- Caption: 1–3 punchy lines max (under 150 characters ideal)
- Include: 3–5 relevant hashtags (mix of niche + trending)
- Optional: suggested sounds or trends to ride

### Instagram
- Caption: Hook line → value/story → CTA
- Length: 100–200 words for Reels; shorter for feed posts
- Hashtags: 5–10 targeted tags at the end (not stuffed inline)

### LinkedIn
- Hook line that stops the scroll (no "I'm excited to share")
- Personal or professional angle relevant to the topic
- 3–5 short paragraphs, no hashtag spam (max 3 tags)
- End with a question to drive comments

### Twitter/X
- If short-form: single punchy tweet with optional hook image note
- If longer content: suggest a thread structure (tweet 1 hook → tweets 2–N key points → final tweet CTA)

---

## Completion

After all steps are done, output a summary card:

```
✅ CONTENT PACKAGE COMPLETE

Topic: [topic]
Platform: [platform]
Concept chosen: [title of chosen concept]
Script length: [estimated duration]
Recommended title: [top CTR title]
Caption: [included above]

---
Want to:
- Tweak the script?
- Generate a different title/thumbnail concept?
- Adapt this content for another platform?
- Turn this into a full content calendar?
```

---

## Tips

- **User changes their mind mid-workflow**: Adapt and re-run only the affected step(s). Don't restart from scratch.
- **Vague topic**: If the user says something like "do a video about fitness", generate ideas that span multiple angles (motivation, how-to, controversy) and let them narrow it down.
- **Platform mismatch**: If the user picks a platform that doesn't match their requested length (e.g., "long-form TikTok"), flag it and suggest the right format or platform.
- **Repurposing**: At the end, always offer to adapt the package for a second platform with minimal extra work.
