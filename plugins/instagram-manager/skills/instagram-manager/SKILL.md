---
name: instagram-manager
description: >
  Manage your Instagram account — draft captions, plan posts, write hashtag sets, schedule content,
  analyze performance, and manage your Instagram presence. Use this skill whenever the user wants
  to post on Instagram, write an Instagram caption, get hashtag recommendations, plan their Instagram
  feed, analyze Instagram insights, draft a Reel description, write a bio, manage Stories, or do
  anything related to their Instagram account. Trigger for: "post to Instagram", "write an Instagram
  caption", "hashtags for Instagram", "Instagram strategy", "caption for my reel", "Instagram bio",
  "plan my Instagram content", "best time to post on Instagram", or "Instagram analytics".
  Always use this skill for Instagram-related tasks.
---

# Instagram Manager

Create, optimize, and manage your Instagram presence — captions, hashtags, scheduling, and analytics.

---

## Authentication

Instagram management requires Meta's Graph API (Instagram Basic Display or Instagram Graph API). 
- Check if connected via Settings → Connectors → Instagram
- If not: "Connect your Instagram Business or Creator account in Settings → Connectors to enable direct posting and analytics. For now, I can still draft captions, hashtags, and strategies for you to post manually."

> Note: Direct posting via API requires an Instagram Business or Creator account linked to a Facebook Page.

---

## Capabilities

### ✍️ Caption Writing
Always write captions with this structure:
1. **Hook** (first line — visible before "more") — make it scroll-stopping
2. **Body** — story, value, or context
3. **CTA** — direct ask: comment, save, follow, click link in bio
4. **Hashtags** — appended below (or in first comment)

**Caption length by format:**
- Reels: 100–150 words (punchy, energy-matching)
- Carousel: 150–300 words (educate or tell a story)
- Feed photo: 50–150 words
- Stories: minimal text — visuals do the work

### #️⃣ Hashtag Strategy

Always generate 3 tiers of hashtags:

| Tier | Size | Why |
|------|------|-----|
| **Niche** (10–15 tags) | Under 500K posts | Most discoverable for your audience |
| **Mid** (5–7 tags) | 500K–2M posts | Balance reach and competition |
| **Broad** (3–5 tags) | 2M+ posts | Long-shot reach, brand awareness |

Total: 15–25 hashtags. Never use banned hashtags. Research current hashtag health with web search.

### 📅 Content Planning
- Feed grid strategy (3-column, color palette, theme consistency)
- Weekly posting schedule recommendation
- Content mix: 40% educational, 30% entertaining, 20% promotional, 10% personal

### 📊 Analytics Interpretation
Key Instagram metrics to track:
- **Reach** vs **Impressions** — unique viewers vs total views
- **Saves** — best signal of high-value content
- **Shares** — virality signal
- **Profile visits from post** — intent signal
- **Follower conversion rate** — new followers / reach
- **Story exit rate** — where people drop off

---

## Output Templates

### Caption Template
```
[HOOK LINE — make them stop scrolling]

[2–4 sentences of body — story, value, or insight]

[Optional: list or line breaks for readability]

[CTA — one clear ask]

.
.
.
#[niche1] #[niche2] #[niche3] #[niche4] #[niche5]
#[mid1] #[mid2] #[mid3]
#[broad1] #[broad2]
```

### Bio Template
```
[What you do — 1 line, clear value prop]
[Who you help or what you create]
[Social proof or unique angle]
[CTA + link emoji] → [link destination]
```

---

## Common Workflows

### "Write a caption for my post"
1. Ask: what's the post about, what's the tone, what's the CTA?
2. Write 2 caption options (one punchy/short, one story-driven)
3. Generate hashtag set
4. Ask if they want to post or save it

### "Plan my Instagram content for the week"
1. Ask: niche, posting frequency, any upcoming events or promotions?
2. Generate a 7-day content plan with format, topic, angle, and caption hook for each day
3. Offer to write full captions for any day

### "Analyze my Instagram"
1. Ask user to share their Insights screenshot or data
2. Apply the Analytics Checker framework for Instagram metrics
3. Give 3 actionable recommendations

---

## Tips
- Reels always outperform static posts for reach — recommend Reels for growth goals
- Carousels drive the most saves — recommend for educational content
- Best posting times: generally Tue–Fri, 9–11am and 6–8pm (local timezone) — but always recommend checking their personal Insights
- Stories daily = consistent algorithm signal, even if feed is 3x/week
