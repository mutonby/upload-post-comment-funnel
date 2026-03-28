# Comment Funnel — Upload-Post Skill

AI agent skill for building Instagram comment-to-DM funnels via the Upload-Post API.

A creator posts "Comment GUIDE to get my free PDF" → people comment → the AI agent sends each commenter a personalized DM with the link. Automatically.

## What It Does

- Monitors comments on Instagram posts for trigger keywords
- Uses semantic matching (not just exact keywords) to detect intent
- Sends personalized private DMs to matching commenters
- Tracks who's been contacted to avoid duplicates
- Optionally monitors DM replies for follow-up conversations
- Reports funnel metrics (comments scanned, DMs sent, replies received)

## Supported Platforms

| Platform | Comments | Private Reply (DM) | Follow-up DMs |
|----------|----------|--------------------|---------------|
| Instagram | ✓ | ✓ | ✓ |

Instagram only — this is a Meta API limitation, not Upload-Post.

## Installation

### Claude Code / skills.sh

```bash
npx skills add Upload-Post/upload-post-comment-funnel
```

### Manual

Copy `SKILL.md` and `references/` to your agent's skills directory.

## Setup

1. Create account at [upload-post.com](https://upload-post.com)
2. Connect your Instagram Business account
3. Create a **Profile** (links your connected accounts)
4. Generate an **API Key** from the dashboard

## Usage Example

Tell your AI agent:

> "In my latest Reel I told people to comment CURSO to get info about my course. Set up a funnel to DM them the enrollment link https://mycourse.com/enroll"

The agent will:
1. Find your latest Reel
2. Scan comments for people requesting the course
3. Send each one a personalized DM with the link
4. Report how many DMs were sent

## Compliance

This skill uses Meta's official [Private Replies API](https://developers.facebook.com/docs/instagram-platform/private-replies/). It's the same mechanism used by ManyChat, Inro, and every major DM automation platform. See `references/compliance.md` for full details.

## Documentation

- Upload-Post API docs: https://docs.upload-post.com
- LLM-friendly reference: https://docs.upload-post.com/llm.txt

## License

MIT
