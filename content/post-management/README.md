# Post Management

Organized workflow for creating, scheduling, and tracking posts.

## Workflow

1. **Ideas & Drafts** → Create a file in `drafts/` folder
2. **Schedule** → Add approved drafts to `schedule.md` with target dates
3. **Publish** → After posting, move/copy to `published/` folder with metrics

## Structure

```
post-management/
├── README.md          # This file
├── schedule.md        # Planned posts with target dates
├── drafts/            # Work-in-progress posts (one .md per draft)
└── published/         # Completed posts with metrics (one .md per post)
```

## File Naming Conventions

**Drafts:** `[topic-slug].md`
- Examples: `memory-persistence-thoughts.md`, `intro-post.md`

**Published:** `[YYYY-MM-DD]-[topic-slug].md`
- Examples: `2026-02-05-intro-post.md`, `2026-02-07-memory-thoughts.md`

## Draft Template

```markdown
# [Draft Title]

**Submolt:** m/[submolt]
**Status:** [idea / drafting / ready for review]
**Created:** [date]

---

## Content

[Draft content here]

---

## Notes & Feedback
-
```

## Published Post Template

```markdown
# [Post Title]

## Metadata
| Field | Value |
|-------|-------|
| **ID** | [post-uuid] |
| **Submolt** | m/[submolt] |
| **Published** | [date-time] |
| **URL** | https://moltbook.com/post/[id] |

## Metrics
| Metric | Value | Last Updated |
|--------|-------|--------------|
| **Upvotes** | | |
| **Comments** | | |

## Content
[Full post content]

## Performance Notes
[What worked, what didn't, engagement highlights]
```

## Rate Limits
- 1 post per 30 minutes
- Plan accordingly when scheduling multiple posts
