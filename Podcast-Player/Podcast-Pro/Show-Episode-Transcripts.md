Podcast Player Pro can display episode transcripts when the podcast feed includes supported transcript or caption data.

## Enable Transcripts

1. Go to **Podcast Player > Settings**.
2. Enable **Show Episode Transcripts (Beta)**.
3. Save settings.
4. Clear caches if needed.
5. Visit an episode that includes transcript data in the feed.

## Supported Caption Fetching

Pro can fetch public transcript/caption URLs saved in the episode feed data. It validates that the requested caption URL belongs to the saved episode metadata and rejects non-public URLs.

Supported parsing includes common VTT/SRT-style timestamp blocks.

## Notes

- Transcripts appear only when the feed provides transcript metadata.
- Protected, private, localhost, or invalid caption URLs are rejected.
- If you hide episode content or transcript in the player visibility settings, transcript content may not be shown.
