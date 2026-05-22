# Embedding Multiple Specific Videos

If you want to showcase a hand-picked selection of videos together in one player, you can use the multiple video embedding method. This method does **not** require a YouTube API key.

## Steps to Embed

1. Insert the **Easy TubeCasting** block into your editor.
2. Paste multiple YouTube video URLs, separated by commas.

- **Example:** `https://youtu.be/video1, https://youtu.be/video2, https://youtu.be/video3`

1. Click **Show YouTube Video/ Playlist**.
2. The plugin will collect those videos and display them in the Spotlight player with an interactive video list.

## Why use this instead of a Playlist?

- **Curation:** You can mix and match videos from different channels or playlists.
- **Control:** You decide the exact order and selection of videos without needing to manage a YouTube playlist on the Google platform.
- **Simplicity:** No API key is needed for this method.

## Best Practices

- **Order:** The videos appear in the order you paste them.
- **Batch Size:** **Videos Per Batch** controls how many video-list items are visible at first and how many additional items are revealed with each **Load More** click.
- **Single-Player Mode:** Set **Videos Per Batch** to `1` to hide the playlist and show only the primary player.
- **Visitor Tools:** Multi-video blocks include search, sorting, and Load More controls when the playlist is visible.
- **Metadata:** Without an API key, the plugin uses YouTube oEmbed fallback data. With a saved API key, richer metadata such as duration, publish date, and views may be available.
