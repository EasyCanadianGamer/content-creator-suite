---
name: youtube-manager
description: >
  Manage your YouTube channel directly — upload videos, write descriptions, manage titles, optimize
  SEO, read comments, and check channel performance. Use this skill whenever the user wants to interact
  with their YouTube channel or YouTube Studio programmatically. Trigger for: "post to YouTube",
  "upload my video", "write a YouTube description", "optimize my YouTube SEO", "read my YouTube comments",
  "reply to comments", "check my YouTube stats", "get my latest videos", "YouTube channel management",
  "update my video title", or any task that involves directly working with their YouTube account.
  Always use this skill when YouTube API access is needed — connects via YouTube Data API v3.
---

# YouTube Manager

Directly manage your YouTube channel: upload, optimize, monitor, and engage.

---

## Authentication Setup

YouTube connections require the YouTube Data API v3. When the user first uses this skill:

1. Check if they've connected YouTube via Claude's connectors (Settings → Connectors → YouTube)
2. If not connected, prompt: "To manage your YouTube channel, you'll need to connect it in Settings → Connectors. Once connected, come back and I can help you upload, optimize, and manage everything."

---

## Capabilities

### 📹 Video Management
- **Get channel videos** — list recent uploads with stats
- **Get video details** — title, description, tags, stats for a specific video
- **Update video metadata** — edit title, description, tags, category
- **Search your channel** — find specific videos

### 💬 Comments & Engagement
- **Read comments** — pull recent comments on a video
- **Reply to comments** — respond as the channel owner
- **Moderate comments** — approve, hold, or reject
- **Read comment threads** — full conversation context

### 📊 Analytics (via YouTube Reporting)
- **Channel stats** — subscribers, total views, watch time
- **Video performance** — views, likes, CTR, AVD per video
- **Audience insights** — demographics, traffic sources

### 🔍 SEO Optimization
- **Tag suggestions** — generate relevant tags from topic
- **Description templates** — structured, keyword-rich descriptions
- **Chapters** — format timestamps for video chapters

---

## Output Templates

### Video Description Template
```
[HOOK — 1–2 sentences summarizing the video value]

In this video, you'll learn:
✅ [Point 1]
✅ [Point 2]
✅ [Point 3]

⏱️ CHAPTERS
0:00 — Introduction
[Add timestamps]

🔗 LINKS & RESOURCES
[Add relevant links]

📱 FOLLOW ME
[Social links]

#[Tag1] #[Tag2] #[Tag3]
```

### Tags Strategy
- Mix of: broad keyword, niche keyword, topic variations, long-tail phrases
- Aim for 10–15 tags
- First tag = most important keyword
- Don't repeat words already in the title

---

## Common Workflows

### "Post a new video"
1. Confirm: title, description, tags, category, privacy setting (public/unlisted/private), scheduled time
2. If video file is uploaded, process upload via API
3. Apply metadata
4. Confirm live URL

### "Optimize an existing video"
1. Pull current title, description, tags
2. Analyze and suggest improvements
3. Apply changes with user confirmation

### "Check and reply to comments"
1. Pull latest N comments
2. Identify: questions, compliments, criticism, spam
3. Draft replies for questions and engaged comments
4. User approves → post replies

### "Get channel report"
1. Pull subscriber count, total views, recent video stats
2. Format as a quick performance summary
3. Flag any videos that are underperforming or overperforming vs. average

---

## Notes

- Always confirm changes before applying them (title edits, comment replies, etc.)
- Remind user that some YouTube API actions have daily quota limits
- For analytics deeper than what the API provides, direct to YouTube Studio
