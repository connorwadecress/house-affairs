---
created: 2026-07-01
type: workflow
status: active
---

# YouTube Capture Workflow

## Purpose

Create repeatable public YouTube snapshots so House Affairs can learn from channel growth, video performance, public comments, requests, and feedback over time.

## Cadence

- Run after every new public upload.
- Run once per week while sessions are being published weekly.
- Run before and after major campaign/event pushes.

## Public Capture Command

Use this from the repository root:

```powershell
yt-dlp --flat-playlist --dump-single-json "https://www.youtube.com/@house.affairs"
```

For video details and comments:

```powershell
yt-dlp --skip-download --write-comments --dump-json "https://www.youtube.com/watch?v=VIDEO_ID"
```

## Fields To Capture

- Capture date/time and timezone.
- Tool and version.
- Channel URL, channel ID, handle, public subscriber count.
- Public About/description summary.
- Visible videos.
- Per-video URL, title, publish date, duration, views, likes, comment count, category, location if shown.
- Public comments and replies as feedback signals.
- Actionable requests.
- General audience sentiment.
- Production issues.
- Opportunities for future content.

## Storage Pattern

- Dated snapshot: `wiki/04 - Content & Media/YouTube Snapshot - YYYY-MM-DD.md`
- Channel current state: `wiki/04 - Content & Media/YouTube Channel.md`
- Audience feedback rollup: `wiki/03 - Audience & Community/Public Feedback Log.md`
- Per-session notes: `wiki/04 - Content & Media/Sessions/`
- Source index: `wiki/00 - Meta/Source Materials.md`
- Tasks: `wiki/07 - Operations/Task Board.md`

## Validation Limits

Public extraction does not provide:

- Impressions.
- Click-through rate.
- Watch time.
- Audience retention.
- Returning viewers.
- Private subscriber changes.
- Copyright status.
- Monetization status.

Use YouTube Studio exports or screenshots for those, and store only privacy-safe summaries.
