# Display Methods Overview

Easy TubeCasting offers three main ways to display YouTube content. Choosing the right method depends on whether you are showing specific videos or asking YouTube to provide all videos from a collection.

---

### 1. Single YouTube Video

Ideal for highlighting a specific video in a post or page.

- **URL Format:** `https://www.youtube.com/watch?v=VIDEO_ID`, `https://youtu.be/VIDEO_ID`, or `https://www.youtube.com/embed/VIDEO_ID`
- **API Key Required:** No (uses basic oEmbed data).
- **Features:** Shows the video in the Spotlight player. If an API key is saved, richer metadata may be used when available.

### 2. Multiple Specific Videos

Perfect for creating a custom gallery of selected videos that aren't necessarily in the same playlist.

- **URL Format:** Comma-separated URLs, e.g., `url1, url2, url3`
- **API Key Required:** No (uses basic oEmbed data).
- **Features:** Renders all specific videos in the Spotlight player with an interactive video list, search, sorting, and Load More controls when the playlist is visible.

### 3. Collections (Playlists, Channels, Usernames, Handles)

The most powerful method for recurring content or large libraries.

- **URL Format:**
- Playlist: `https://www.youtube.com/playlist?list=PLAYLIST_ID`
- Playlist from watch URL: `https://www.youtube.com/watch?v=VIDEO_ID&list=PLAYLIST_ID`
- Channel: `https://www.youtube.com/channel/CHANNEL_ID`
- Username: `https://www.youtube.com/user/USERNAME`
- Handle: `https://www.youtube.com/@USERNAME`
- **API Key Required:** **Yes**. A valid YouTube Data API v3 key is required to fetch the list of videos and metadata.
- **Features:** Local collection cache, richer metadata, frontend search and sorting, Load More, manual sync, single-collection sync, and optional automatic sync.

---

| Feature | Single Video | Multiple Videos | Collections |
| --- | --- | --- | --- |
| No API Key Needed | Yes | Yes | No |
| Auto-Syncing | No | No | Yes |
| Frontend Search | No | Yes, with visible playlist | Yes, with visible playlist |
| Frontend Sorting | No | Yes, with visible playlist | Yes, with visible playlist |
| Load More | No | Yes, with visible playlist | Yes, with visible playlist |
| Metadata Without API Key | Basic | Basic | Not available |
| Metadata With API Key | Richer | Richer | Full collection metadata |
| Display Style | Spotlight | Spotlight | Spotlight |
