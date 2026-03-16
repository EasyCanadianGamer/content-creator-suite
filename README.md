# 🎬 Content Creator Suite — Claude Code Plugin Marketplace

A complete AI-powered toolkit for content creators. Nine skills covering every stage of the content workflow — from ideas to scripts, thumbnails to analytics, and full platform management for YouTube, TikTok, Instagram, LinkedIn, and Twitter/X.

Works in **Claude Code** (via `/plugin`) and **Claude.ai** (via `.skill` file upload in Settings → Skills).

---

## 🚀 Quick Install (Claude Code)

**Add the marketplace:**
```
/plugin marketplace add EasyCanadianGamer/content-creator-suite
```

**Install all 9 plugins at once:**
```
/plugin install video-scriptwriter
/plugin install content-ideas
/plugin install thumbnail-title-optimizer
/plugin install analytics-checker
/plugin install youtube-manager
/plugin install instagram-manager
/plugin install tiktok-manager
/plugin install linkedin-manager
/plugin install twitter-manager
```

Or install only the ones you need.

---

## 📦 Plugins

### ✍️ Content Creation

| Plugin | What it does |
|--------|-------------|
| **video-scriptwriter** | Full scripts for YouTube, TikTok, Reels, ads — with `.docx` export |
| **content-ideas** | Ideas, angles, hooks, and full content calendars for any niche/platform |
| **thumbnail-title-optimizer** | 5 title options with CTR scoring + thumbnail design briefs |

### 📊 Analytics

| Plugin | What it does |
|--------|-------------|
| **analytics-checker** | Paste your stats → get diagnosis + top 3 actionable recommendations |

### 📱 Platform Managers

| Plugin | What it does |
|--------|-------------|
| **youtube-manager** | Descriptions, tags, chapters, comment replies, channel reports |
| **instagram-manager** | Captions, 3-tier hashtag sets, bio writing, feed planning |
| **tiktok-manager** | Hooks, FYP optimization, trend research, completion-rate strategy |
| **linkedin-manager** | Thought leadership posts, profile optimization, outreach messages |
| **twitter-manager** | Tweets, threads, voice development, engagement strategy |

---

## 🔧 Manual Install (Claude.ai)

If you're using Claude.ai instead of Claude Code, you can install skills directly:

1. Go to **Settings → Skills → Upload Skill**
2. Upload any `.skill` file from the [`/releases`](../../releases) section of this repo

---

## 📁 Repo Structure

```
content-creator-suite/
├── .claude-plugin/
│   └── marketplace.json        # Marketplace manifest
├── plugins/
│   ├── video-scriptwriter/
│   │   ├── .claude-plugin/
│   │   │   └── plugin.json
│   │   └── skills/
│   │       └── video-scriptwriter/
│   │           └── SKILL.md
│   ├── content-ideas/          # same structure
│   ├── thumbnail-title-optimizer/
│   ├── analytics-checker/
│   ├── youtube-manager/
│   ├── instagram-manager/
│   ├── tiktok-manager/
│   ├── linkedin-manager/
│   └── twitter-manager/
└── README.md
```

---

## 🔌 Platform Connections

The platform manager skills (YouTube, Instagram, TikTok, LinkedIn, Twitter/X) are designed to work with Claude's connector system. To enable direct posting and analytics:

- **Claude.ai**: Go to Settings → Connectors and connect each platform
- **Claude Code**: Set up the relevant MCP servers for each platform

Even without connections, all skills work fully for drafting, planning, and strategy.

---

## 📝 Usage Examples

Once installed, just describe what you need:

```
"Give me 10 YouTube video ideas about personal finance for millennials"
→ content-ideas activates

"Write a script for a 10-minute video on budgeting basics"  
→ video-scriptwriter activates

"Create 3 title options and a thumbnail brief for my budgeting video"
→ thumbnail-title-optimizer activates

"My YouTube CTR dropped from 6% to 3% last month, what's wrong?"
→ analytics-checker activates

"Write me an Instagram caption and hashtags for my new reel"
→ instagram-manager activates
```

---

## 🤝 Contributing

Found a bug or want to improve a skill? Open an issue or PR. Skills are plain Markdown — easy to edit and improve.

---

## 📄 License

MIT — use freely, modify as needed, attribution appreciated.
