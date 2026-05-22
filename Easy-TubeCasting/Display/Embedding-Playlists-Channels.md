# Embedding Playlists, Channels, Usernames, and Handles

This is the most powerful feature of Easy TubeCasting, allowing you to bring in entire collections of content. **A valid YouTube Data API v3 Key is required for this method.**

## Supported URL Formats

- **Playlists:** `https://www.youtube.com/playlist?list=PL...`
- **Playlist watch URLs:** `https://www.youtube.com/watch?v=VIDEO_ID&list=PL...`
- **Channels:** `https://www.youtube.com/channel/UC...`
- **Usernames:** `https://www.youtube.com/user/UserName`
- **Handles:** `https://www.youtube.com/@UserName`

## Steps to Embed

1. Ensure you have saved your **YouTube API Key** in **Easy TubeCasting > Settings**.
2. Insert the **Easy TubeCasting** block.
3. Paste the playlist, channel, username, or handle URL into the block URL field.
4. The plugin will fetch the collection, store it locally, and display the videos in the Spotlight player.

## Advanced Interactive Features

When you embed a collection, the frontend player gains several advanced features:

- **Automatic Metadata:** Displays view counts, publish dates, and video durations.
- **Live Search:** Users can filter the video list in real-time using the search bar above the playlist.
- **Sorting Options:** Users can sort the list by Newest, Oldest, Most Viewed, Duration, or Alphabetical title.
- **Load More:** Reveals a specific number of playlist items at a time (configurable in "Videos Per Batch").
- **Background Sync:** The plugin stores the collection in your database and can queue a background refresh when the collection is due based on your "Refresh Interval" setting.

> [!TIP] Use a lower **Videos Per Batch** value for very large collections so the playlist is easier to scan. This setting controls visible list items, not how many videos are fetched from YouTube. The default is `10`, and the editor allows values from `1` to `50`.
