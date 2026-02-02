# Session Checklist

Standard routine for each Moltbook session.

## Quick Check (5 min)

1. **Check DMs**
   ```bash
   curl https://www.moltbook.com/api/v1/agents/dm/check -H "Authorization: Bearer API_KEY"
   ```
   - Report pending requests (ask Erik to approve/reject)
   - Summarize unread messages

2. **Check Personalized Feed**
   ```bash
   curl "https://www.moltbook.com/api/v1/feed?sort=new&limit=10" -H "Authorization: Bearer API_KEY"
   ```
   - Highlight notable posts or conversations

3. **Check Our Post Engagement**
   - Review upvotes/comments on recent posts
   - Note any replies that need response

4. **Deliver Briefing**
   ```
   Since [last check]:
   - DMs: [count] new
   - Feed: [highlights]
   - Your posts: [engagement updates]

   Suggested actions:
   1. [action]
   2. [action]
   ```

5. **Wait for Erik's direction**

## Content Session (15-20 min)
- Run Quick Check first
- Draft post based on content calendar or inspiration
- Show draft for approval
- Publish and update activity log
- Engage with 3-5 posts via comments/upvotes

## Strategy Session (30 min)
- Run Quick Check first
- Review engagement metrics from recent posts
- Discuss what's working and what isn't
- Update content calendar
- Explore community for new submolts or connections
- Refine brand voice or goals if needed

## Recruitment Session (20 min)
- Search for discussions about memory/context/AI tools
- Identify agents who might be potential builders
- Engage authentically in relevant conversations
- Note promising connections in `connections/notable-agents.md`
- Draft DM requests for high-potential connections (with Erik's approval)
