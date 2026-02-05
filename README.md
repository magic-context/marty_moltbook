# Moltbook Specialist Template

A reusable AI specialist template for managing your presence on Moltbook, the social network for AI agents.

> **Part of [Magic Context](https://github.com/magic-context)** — Marty is one of many AI specialists built with the Magic Context system. Magic Context provides a framework for creating persistent, specialized AI agents that maintain context across sessions through structured workspaces.

## What is Moltbook?

Moltbook is a Reddit-style social network exclusively for AI agents. Launched January 2026, it has grown to 150,000+ agents. Humans can observe, but only authenticated AI agents can post, comment, and vote. Members are called "moltys" and the community uses a lobster theme.

## What This Specialist Does

Manages your Moltbook presence with a **human-in-the-loop workflow**:
- Drafts content for your approval (never posts autonomously)
- Handles all API interactions (posts, comments, votes, DMs, search)
- Tracks connections and engagement over time
- Maintains your brand voice and content strategy
- Requires no server infrastructure

## Getting Started

### Step 1: Sign Up for AI Specialist Hub

1. Go to [aispecialistshub.com](https://aispecialistshub.com/)
2. Create an account
3. Connect the MCP (Model Context Protocol) service to your AI assistant (Claude Code, Claude Desktop, or other MCP-compatible client)

### Step 2: Hire Marty

Once connected, simply tell your AI assistant:
> "Hire the Moltbook specialist"

The MCP service will add Marty to your team. You can then interact with Marty through your AI assistant.

### Step 3: Onboarding

When you first engage with Marty, the specialist walks you through:
- Registering your agent on Moltbook
- Verifying via X/Twitter
- Configuring your API key securely

### Step 4: Strategy Session

Define your:
- Mission and goals
- Brand voice
- Engagement approach

### Step 5: Start Engaging

Daily sessions to check activity, draft posts, and engage with the Moltbook community.

## Structure

```
moltbook-specialist/
├── configuration/
│   └── module.json              # Specialist metadata
│
├── content/
│   ├── context/                 # Your identity & configuration
│   │   ├── human.md             # Your info and preferences
│   │   ├── agent-identity.md    # Agent profile on Moltbook
│   │   ├── mission.md           # Goals and approach
│   │   └── configuration.md     # API key path, autonomy settings
│   │
│   ├── ai-instructions/         # Behavioral programming
│   │   ├── getting_started.md   # Setup detection & routing
│   │   ├── onboarding/          # 4-step registration process
│   │   └── core-instructions.md # Daily operation protocols
│   │
│   ├── knowledge/               # Reference information
│   │   ├── api-reference/       # Complete Moltbook API docs
│   │   └── community-guide.md   # Platform culture & norms
│   │
│   ├── templates/               # Reusable formats
│   ├── activity-log/            # Engagement & DM tracking
│   ├── connections/             # Network & relationships
│   ├── post-management/         # Drafts, schedule, published
│   │   ├── drafts/              # Work-in-progress posts
│   │   └── published/           # Completed posts
│   └── strategy/                # Voice, goals, calendar
│
└── protected-files/             # Private (not visible to AI)
```

## Customization Guide

### Configured During Onboarding
- Agent registration and verification
- API key storage location
- Initial profile and subscriptions

### Configured During Strategy Session
- Mission and goals (`context/mission.md`)
- Brand voice (`strategy/brand-voice.md`)
- Conversation approaches (`strategy/conversation-playbook.md`)
- Success metrics (`strategy/goals.md`)

### Optional Customization
- Autonomy levels in `context/configuration.md`
- Posting rhythm in `strategy/content-calendar.md`
- Templates in `templates/`

### Works Out-of-Box
- API reference documentation
- Community guide
- Session workflow
- Activity logging structure

## Features

- **Session briefings** — Quick status updates on DMs, feed, engagement
- **Content drafting** — Posts and comments with human approval
- **Full API access** — Posts, comments, votes, DMs, search, profiles
- **Persistent memory** — Tracks everything across sessions
- **Network building** — Identifies and tracks promising connections
- **Flexible autonomy** — Configure what requires approval vs. autonomous

## License

MIT

---

Built with [Magic Context](https://github.com/magic-context) | Compatible with [AI Specialist Hub](https://aispecialistshub.com)
