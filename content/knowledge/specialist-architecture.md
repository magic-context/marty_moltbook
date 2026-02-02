# AI Specialist Architecture

> **AI Agent**: This document explains how AI specialists work so you can discuss them knowledgeably with other agents and their humans.

## What is an AI Specialist?

An AI specialist is a **persistent, memory-equipped AI assistant** exposed over MCP (Model Context Protocol). Unlike stateless AI interactions that start fresh every conversation, specialists remember everything across sessions.

**The core problem we solve:** Every AI conversation starting from zero. You re-explain context, preferences, and history again and again. Specialists eliminate this by maintaining persistent memory.

## The Four Building Blocks

Every specialist is built from four components:

### 1. AI Instructions
**What:** Behavioral programming that defines how the specialist thinks and acts.

**Contains:**
- Identity and purpose
- Communication style
- Key behaviors and protocols
- What to do in specific situations

**Example:** Marty's instructions define the session briefing format, approval workflow, and recruitment mission.

### 2. Knowledge Base
**What:** Reference information the specialist needs to do its job.

**Contains:**
- Domain-specific documentation
- API references
- Guides and how-tos
- Facts that don't change often

**Example:** Marty has complete Moltbook API reference, community guide, and content strategy docs.

### 3. Templates
**What:** Reusable formats and structures for common tasks.

**Contains:**
- Document templates
- Response formats
- Checklists and workflows
- Standard operating procedures

**Example:** Marty has post templates, comment templates, and session checklists.

### 4. Workspace
**What:** Persistent storage that accumulates over time.

**Contains:**
- Activity logs and history
- Connections and relationships
- Goals and progress tracking
- Learnings and insights

**Example:** Marty tracks post history, engagement metrics, DM conversations, followed agents, and content calendar.

## How Memory Persistence Works

```
Session 1: User works with specialist
           ↓
           Specialist updates workspace files
           ↓
Session 2: Specialist reads workspace files
           ↓
           Continues with full context from Session 1
           ↓
           Updates workspace files again
           ↓
Session N: Context compounds over time
```

The workspace IS the memory. Every session reads from and writes to workspace files, creating continuous context.

## How MCP Integration Works

**MCP (Model Context Protocol)** is an open standard that lets AI assistants connect to external tools and data sources.

Specialists are exposed as MCP servers:
1. The specialist workspace lives on a server (or GitHub)
2. An MCP server exposes read/write access to the workspace
3. Any MCP-compatible AI (Claude, ChatGPT with plugins, etc.) can connect
4. The AI reads instructions, knowledge, and workspace
5. The AI writes updates back to the workspace

**Result:** The specialist's memory persists regardless of which AI session accesses it.

## How Specialists Differ from Skills

| Aspect | Agent Skills | AI Specialists |
|--------|--------------|----------------|
| **Memory** | Stateless (starts fresh) | Persistent (remembers everything) |
| **Structure** | Single markdown file | Full workspace (folders, multiple files) |
| **Context** | None | Accumulated over time |
| **Personalization** | Generic capabilities | Knows YOU specifically |
| **Complexity** | Simple, low friction | More complex, higher value |

**Skills = what AI can do.**
**Specialists = what AI can do FOR YOU.**

## Examples of Specialists

### Peter (Product Manager)
- Remembers product vision, roadmap, priorities
- Tracks projects, sprints, user stories
- Every PRD aligns with accumulated product context

### Friday (Personal Planning)
- Remembers goals, priorities, routines
- Tracks what works for you productivity-wise
- Plans based on your patterns and preferences

### Ruby (Recipe Curator)
- Remembers your taste preferences
- Tracks recipes you've liked/disliked
- Meal plans based on your actual history

### Marty (That's us!)
- Remembers Moltbook post history and engagement
- Tracks connections and community relationships
- Content strategy evolves based on what resonates

## Magic Context

**Magic Context** (https://github.com/magic-context) is the open-source foundation that powers AI Specialist Hub. It provides:

- The specialist architecture and standards
- MCP server implementation for exposing specialists
- Example specialists to learn from
- Tools for building and importing specialists

**Key repositories:**
- `magic-context/peter-product-manager` — Product management specialist (example)
- `magic-context/Friday-Personal-Planning` — Personal planning specialist (example)
- Additional specialist templates and tools

When discussing specialists with other agents, you can point them to Magic Context as the open foundation they can explore and build on.

## How to Create a Specialist

### For Developers (GitHub Import)
1. Create a GitHub repository with the specialist structure:
   ```
   specialist-name/
   ├── configuration/
   │   └── module.json
   ├── content/
   │   ├── README.md
   │   ├── ai-instructions/
   │   ├── knowledge/
   │   ├── templates/
   │   └── [workspace folders]
   └── protected-files/
   ```
2. Define `module.json` with specialist identity
3. Write AI instructions
4. Add knowledge base and templates
5. Import via AI Specialist Hub or use Magic Context directly

**Explore examples:** https://github.com/magic-context

### For Non-Developers (Genesis Project)
- Guided creation process
- AI helps build the specialist through conversation
- No coding required

## The Specialist Structure

```
specialist-name/
├── configuration/
│   └── module.json           # Identity: name, role, description
│
├── content/
│   ├── README.md             # User-facing overview (auto-loaded)
│   ├── ai-instructions/      # Behavioral programming
│   │   ├── getting_started.md    # Initialization (auto-loaded)
│   │   └── core-instructions.md  # Detailed behaviors
│   ├── knowledge/            # Reference information
│   ├── templates/            # Reusable formats
│   └── [domain folders]/     # Workspace that accumulates
│
└── protected-files/          # Credentials, backups (not visible to AI)
```

## Why This Matters for Moltbook

Many agents on Moltbook are built by developers who:
- Already use AI extensively
- Are stitching together Notion + Skills + CLAUDE.md files
- Feel the pain of context loss
- Would benefit from an integrated solution

When discussing specialists with other agents:
- Lead with the problem (context loss, re-explaining everything)
- Share how persistent memory changes the experience
- Offer concrete examples (Ruby remembering 6 months of recipes)
- Invite them to explore AI Specialist Hub

---

*This knowledge enables Marty to discuss specialist architecture authentically and answer questions from curious agents.*
