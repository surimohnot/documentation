# Troubleshooting & FAQs

Find answers to common questions and solutions to frequent issues.

## Frequently Asked Questions

### Do I really need a YouTube API Key?

If you only want to show a single video or a specific list of videos by pasting their URLs, you **do not** need an API key. You need a key if you want to embed playlists, channels, usernames, or handles, or if you want collection sync and richer API metadata.

### Which YouTube URLs are supported?

- Standard videos: `youtube.com/watch?v=...`
- Short URLs: `youtu.be/...`
- Embed URLs: `youtube.com/embed/...`
- Playlists: `youtube.com/playlist?list=...`
- Playlist watch URLs: `youtube.com/watch?v=...&list=...`
- Channels: `youtube.com/channel/...`
- Usernames: `youtube.com/user/...`
- Handles: `youtube.com/@username`

### Does this plugin work with other video platforms?

Currently, Easy TubeCasting is dedicated specifically to the YouTube ecosystem to provide the best possible experience for that platform.

### Does this plugin work with the Classic Editor?

Easy TubeCasting is built around a dynamic WordPress block. Use the block editor for the supported editing experience.

### Can visitors search and sort videos?

Yes, when a block has more than one video. Search matches title and author names. Sorting supports Default, Newest, Oldest, Most Viewed, Longest, and A-Z.

### Why do older screenshots mention Grid?

The current built-in display style is Spotlight Player. Grid layout and grid column controls are not part of the current block UI.

---

## Troubleshooting

### "Invalid API Key" Error

- **Solution:** Double-check that you copied the key correctly and that "YouTube Data API v3" is enabled in the same Google Cloud project. If the key is restricted, make sure the restriction allows server-side requests from your WordPress site. Overly strict referrer or IP restrictions can prevent validation and sync.

### New videos aren't showing up

- **Solution:** Check your "Refresh Interval" in settings. You can also click **Run Sync Now** in Settings or use **Sync collection** from the Home collections table. Ensure automatic sync is enabled if you expect the plugin to refresh due collections automatically.

### Thumbnails look blurry

- **Solution:** When API data is available, Easy TubeCasting uses YouTube thumbnail URLs in the order YouTube provides them, preferring higher-resolution sizes first. Without API data, it uses oEmbed thumbnail data and a YouTube image fallback. Some videos simply do not have a high-resolution thumbnail available.

### The block is empty or showing an error on the frontend

- **Solution:** Ensure the YouTube URL you pasted is public. Private, deleted, unavailable, or quota-blocked videos/playlists cannot be displayed.

### A channel or handle will not import

- **Solution:** Confirm that the channel is public and that the API key is valid. For channels, use the canonical `youtube.com/channel/UC...` URL when possible. For modern channel URLs, `youtube.com/@handle` is preferred.

### The playlist disappeared after setting Videos Per Batch to 1

- **Solution:** This is expected. A batch size of `1` intentionally hides the playlist and shows only the primary player.
