---
name: video-scriptwriter
description: >
  Use this skill whenever a user wants to write, draft, or create a script for any type of video content.
  Trigger for: YouTube videos, TikToks, Reels, Shorts, explainer videos, educational content, ads, commercials,
  product demos, brand videos, vlogs, documentaries, video essays, or any spoken/visual content meant to be filmed
  or recorded. Also trigger when a user says things like "write me a script", "I need a video script", "help me
  plan a video", "script for my channel", "write a TikTok", "ad script", or "YouTube video on [topic]".
  Always use this skill when video scripting is involved — don't just wing it. This skill produces both a
  formatted .docx script file AND a chat preview.
---

# Video Scriptwriter

Produces polished, ready-to-shoot video scripts for any format, length, or tone. Always outputs both a **chat preview** and a **downloadable .docx file**.

---

## Step 1: Gather Info

Before writing, confirm you have these four inputs. If any are missing, ask the user:

| Input | Why it matters |
|---|---|
| **Topic / brief** | What the video is about |
| **Target audience** | Who will watch it |
| **Tone** | Funny, serious, educational, hype, conversational, etc. |
| **Desired length** | Duration or rough word count (see table below) |

**Length guide:**
| Format | Duration | ~Word count |
|---|---|---|
| Short-form (TikTok/Reels/Shorts) | 15–60s | 50–150 words |
| Mid-form | 2–5 min | 300–750 words |
| Long-form (YouTube) | 8–20 min | 1,200–3,000 words |
| Ad / commercial | 15–60s | 40–120 words |

---

## Step 2: Choose the Right Structure

Pick the structure that fits the content type. You can mix structures or adapt them — be flexible.

### A. Hook / Body / CTA (best for short-form, ads, and most YouTube)
```
[HOOK]       — First 3–10 seconds. Stop the scroll. Open a loop or make a bold claim.
[BODY]       — Deliver the value, story, or argument.
[CTA]        — Clear call to action: subscribe, buy, comment, follow, etc.
```

### B. Scene-by-Scene (best for narrative, brand, or cinematic content)
```
[SCENE 1: Setup]
[SCENE 2: Conflict or tension]
[SCENE 3: Resolution / payoff]
[SCENE N: ...]
```

### C. Voiceover + Visuals (best for explainers, educational, ads)
```
Two-column format:
| VOICEOVER (what's said) | VISUALS (what's shown) |
```

### D. Frameworks to suggest (lightly, not enforce)
- **AIDA** – Attention → Interest → Desire → Action (great for ads)
- **PAS** – Problem → Agitate → Solution (great for educational / pain-point content)
- **Story Arc** – Setup → Rising tension → Climax → Resolution (narrative content)
- **Listicle** – Numbered tips or steps (YouTube "X ways to..." videos)

When in doubt, ask the user if they have a preferred structure or suggest one based on their brief.

---

## Step 3: Write the Script

### Formatting rules
- **Short-form**: Write tight. Every word earns its place. Use punchy sentences. No fluff.
- **Long-form**: Vary sentence length. Use signposting ("Here's the thing...", "But wait —"). Write like you talk.
- **Ads**: Lead with the problem or hook immediately. Be direct.
- **Explainers**: Break down complex ideas. Use analogies. Signpost sections clearly.

### Always include
- **[HOOK]** label at the start (even for long-form — the first 30s matters most)
- **[CTA]** at the end
- Speaker directions in *italics* or [brackets] where useful (e.g., *pause for effect*, [cut to product])
- Scene or section labels to help with production

### Tone guidance
- **Funny**: Use callbacks, subverted expectations, punchy timing cues
- **Serious / emotional**: Slow down, use short sentences, let moments breathe
- **Hype / energetic**: Short punchy lines, exclamation, momentum-building pacing
- **Educational**: Clear, confident, structured — "First... then... finally..."
- **Conversational**: Write like speaking to one person, use contractions, ask questions

---

## Step 4: Output — Chat Preview

Show the full script in chat first, formatted clearly:

```
🎬 VIDEO SCRIPT: [Title]
Format: [YouTube Long-form / TikTok / Ad / etc.]
Estimated length: [X min / X sec]
Tone: [Tone]
Audience: [Audience]

---

[HOOK]
...

[BODY / SCENE 1 / etc.]
...

[CTA]
...
```

Then say: *"I'm also generating a .docx file for you — one moment!"*

---

## Step 5: Output — .docx File

After showing the chat preview, generate a formatted Word document using the docx skill.

Read `/mnt/skills/public/docx/SKILL.md` for full docx generation instructions.

### Document structure for the .docx:
1. **Cover section**: Title, format, tone, audience, estimated length
2. **Script body**: Full script with proper section labels
3. **Two-column table** (for voiceover/visuals format if applicable):
   - Left column: VOICEOVER
   - Right column: VISUALS / DIRECTION
4. **Production notes** (optional): Any notes on music, pacing, B-roll suggestions

### Styling guidelines for the .docx:
- Title: Heading 1, bold
- Section labels ([HOOK], [SCENE 1], [CTA], etc.): Heading 2 or bold + colored text
- Script body: Normal text, 12pt, readable line spacing (1.15 or 1.5)
- Stage directions / visual notes: Italicized or in a shaded text box
- Use US Letter page size (12240 x 15840 DXA)
- Keep it clean and production-ready — this is a working document

---

## Tips & Edge Cases

- **User gives a vague brief**: Write a short script and offer to adjust tone/length/structure after.
- **Very short scripts (TikTok/Reels)**: Still show section labels, just compressed. Don't skip the hook.
- **User wants multiple versions**: Offer an A/B version with different hooks or CTAs.
- **User has an existing script to improve**: Read it, identify weak spots (usually the hook and CTA), and rewrite with notes explaining changes.
- **Series / episodic content**: Maintain consistent style and sign-off across episodes.
- **Multilingual**: If the user specifies a language, write in that language and note any localization considerations.
