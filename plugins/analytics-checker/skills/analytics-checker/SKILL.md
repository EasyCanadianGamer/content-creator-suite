---
name: analytics-checker
description: >
  Analyze content performance data, interpret metrics, and give actionable recommendations for any platform.
  Use this skill whenever the user shares analytics data, screenshots, CSV exports, or asks about their
  performance metrics from YouTube Studio, TikTok Analytics, Instagram Insights, LinkedIn Analytics,
  or Twitter/X Analytics. Trigger for: "check my analytics", "why are my views down", "analyze my stats",
  "what do my metrics mean", "how is my channel performing", "my engagement dropped", "is my content
  working", "what should I change based on my data", "CTR analysis", "retention analysis", "growth
  analysis", or any mention of views, impressions, reach, engagement rate, watch time, CTR, or followers.
  Always use this skill when interpreting performance data — don't just respond generically.
---

# Analytics Checker

Interprets platform analytics data and turns numbers into clear, actionable recommendations.

---

## Step 1: Identify What Data You Have

Ask the user to share their analytics in one of these forms:
- **Screenshot or image** of their analytics dashboard
- **CSV/export file** from their platform
- **Pasted numbers** directly in chat
- **Verbal description** ("my views dropped 40% last month")

Also confirm:
- Which **platform** the data is from
- What **time period** it covers
- What their **goal** is (growth, engagement, monetization, sales)

---

## Step 2: Platform-Specific Metrics Guide

### YouTube
| Metric | What it means | Healthy benchmark |
|--------|--------------|-------------------|
| CTR (Click-Through Rate) | % who click after seeing thumbnail | 4–10% is good; 2–4% is average |
| Average View Duration | How long people watch | Aim for 40–60%+ of video length |
| Impressions | How often YouTube shows your video | Higher = algorithm is pushing it |
| Watch Time (hours) | Total hours watched | Key for monetization and ranking |
| Subscribers gained | Net new subs from video | Positive = video resonates with new audience |
| Revenue / RPM | Revenue per 1,000 views | Varies by niche: $2–$50 RPM |

**Key YouTube diagnostic questions:**
- Is CTR high but AVD low? → Hook is working, but content isn't delivering on the promise
- Is CTR low but AVD high? → Great content, weak thumbnail/title
- Are impressions low? → Algorithm isn't distributing the video — check SEO and watch time on recent uploads

### TikTok
| Metric | Benchmark | Notes |
|--------|-----------|-------|
| Views | N/A — highly variable | Don't compare to other creators |
| Watch time % | 70–100% = great | TikTok rewards completion rate |
| Shares | >1% of views = strong | Shares are the #1 growth signal |
| Profile visits | Indicates interest beyond the video | |
| Follower conversion | Views → Followers | |

**Key TikTok diagnostic questions:**
- Low completion rate? → Hook isn't holding. Restructure opening 3 seconds.
- High views but low follows? → Content is entertaining but not niche-clear
- Video stuck at ~300 views? → Initial engagement was too low — try posting at a different time

### Instagram
| Metric | Notes |
|--------|-------|
| Reach | Unique accounts who saw the post |
| Impressions | Total views (including repeat) |
| Engagement rate | (Likes+Comments+Saves+Shares) / Reach — aim for 3–6%+ |
| Saves | High saves = high-value content (algorithm loves this) |
| Shares | Virality signal |
| Story views / exits | Where people drop off in stories |
| Reel plays | Treated like TikTok — completion rate matters |

### LinkedIn
| Metric | Notes |
|--------|-------|
| Impressions | How many times shown |
| Reactions + Comments + Shares | Engagement indicators |
| Follower demographics | Are you reaching the right people? |
| CTR on links | If you post external links (usually lower reach) |

### Twitter/X
| Metric | Notes |
|--------|-------|
| Impressions | Total views |
| Engagements | Any interaction |
| Link clicks | Important if driving traffic |
| Profile visits | Intent signal |
| Retweets / Quotes | Amplification |

---

## Step 3: Diagnose the Data

For any analytics input, run through this diagnostic framework:

### The 3-Layer Diagnosis
1. **Discovery** — Is the platform showing your content to enough people?
   - Low impressions/reach? → Posting frequency, SEO, hashtags, posting time
2. **Click-through / Hook** — Are people choosing to engage with it?
   - Low CTR or low swipe-ups? → Thumbnail, title, hook text
3. **Retention / Completion** — Are people staying once they start?
   - High drop-off? → Content pacing, length, value delivery

---

## Step 4: Output Format

```
📊 ANALYTICS REPORT: [Platform] — [Period]

🔍 OVERVIEW
[2–3 sentence summary of overall performance]

📈 WHAT'S WORKING
- [Metric]: [Value] → [Why this is good and what it signals]
- ...

⚠️ AREAS TO IMPROVE
- [Metric]: [Value] → [What it indicates and why it matters]
- ...

🎯 TOP 3 RECOMMENDATIONS
1. [Specific action] — [Why it will help based on the data]
2. ...
3. ...

📅 WHAT TO TEST NEXT
[Suggest 1–2 experiments based on the data]
```

---

## Step 5: Trend Analysis

If the user has data over multiple periods:
- Identify **trends** (growing, declining, plateauing)
- Flag **anomalies** (sudden spikes or drops — what caused them?)
- Suggest **comparisons** ("your best-performing video did X — how does this differ?")

---

## Tips

- **No data yet**: If the user is just starting out, explain which metrics to watch first and how to read their platform's native dashboard.
- **CSV files**: Parse them, identify key columns, and summarize the top insights.
- **Screenshots**: Describe what you see and analyze it against benchmarks.
- **Overwhelmed users**: Focus on 2–3 actionable metrics, not everything at once.
- **Monetization questions**: Know CPM/RPM differences, YouTube Partner Program thresholds (1,000 subs + 4,000 watch hours or 10M Shorts views).
