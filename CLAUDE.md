# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Project Is

A Claude AI plugin marketplace suite — 9 skills for content creators covering scripting, ideation, optimization, analytics, and platform management (YouTube, TikTok, Instagram, LinkedIn, Twitter/X). There is no build step, no runtime, and no dependencies. All content is declarative Markdown.

## No Build/Test Commands

This is a pure Markdown + JSON project. There is nothing to install, build, lint, or test. Skills are `.skill` files compiled from `SKILL.md` for distribution, but the source files are the Markdown files in this repo.

## Plugin Structure

Every plugin follows the same layout:

```
plugins/<plugin-name>/
├── .claude-plugin/
│   └── plugin.json      # Plugin metadata (name, description, version, triggers)
└── skills/
    └── <plugin-name>/
        └── SKILL.md     # The full skill instructions consumed by Claude
```

The root `.claude-plugin/marketplace.json` is the manifest that registers all 9 plugins with their `source` paths, categories, and tags.

## How Skills Work

Skills are instruction sets that Claude activates based on user intent. Each `SKILL.md` defines:
- **Trigger phrases** — the keywords/patterns that activate the skill
- **Workflow steps** — what Claude should do when activated
- **Output format** — the structure of the response (e.g., 5 titles with CTR scores, a thumbnail design brief, a full script)
- **Platform rules** — platform-specific algorithm knowledge baked into the instructions

Skills work in two modes:
- **Drafting mode** — no API connection required; Claude generates content locally
- **Connected mode** — with Claude Connectors (Claude.ai) or MCP servers (Claude Code), skills can read/post to live platforms

## Plugin Categories

| Category | Plugins |
|----------|---------|
| Content Creation | `video-scriptwriter`, `content-ideas`, `thumbnail-title-optimizer` |
| Analytics | `analytics-checker` |
| Platform Management | `youtube-manager`, `instagram-manager`, `tiktok-manager`, `linkedin-manager`, `twitter-manager` |

## Making Changes

When editing a skill, the only file that matters is the `SKILL.md`. The `plugin.json` only needs updating if you're changing the plugin's name, description, version, or trigger metadata. After editing, the root `marketplace.json` does not need to change unless adding or removing a plugin entirely.

When adding a new plugin, register it in `.claude-plugin/marketplace.json` under the `plugins` array with a `source` path pointing to the new plugin directory.
