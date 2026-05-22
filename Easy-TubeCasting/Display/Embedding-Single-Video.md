# Embedding a Single Video

Embedding a single YouTube video is the simplest way to use Easy TubeCasting. This method does **not** require a YouTube API key.

## Steps to Embed

1. Open the page or post where you want to add the video.
2. Click the **(+) Add Block** button and search for "Easy TubeCasting".
3. Paste the video URL into the block URL field.
4. Paste the URL of your YouTube video.

- Supported formats:
- `https://www.youtube.com/watch?v=dQw4w9WgXcQ`
- `https://youtu.be/dQw4w9WgXcQ`
- `https://www.youtube.com/embed/dQw4w9WgXcQ`

1. Click **Show YouTube Video/ Playlist**.
2. The block will render a server-side preview in the editor and the Spotlight player on the frontend.

## Configuration Tips

- The current frontend display style is **Spotlight Player**.
- Set **Videos Per Batch** to `1` if you want the block to stay as a single-player experience even if you later add more video URLs.
- You can toggle between **Dark** and **Light** themes in the block settings to match your site's design.
- Use **Accent Color** to control the play badge and player accent color.
- The player is fully responsive and will adjust to the width of your content area.

> [!NOTE] Without an API key, single videos use YouTube oEmbed fallback data, so fields such as duration, publish date, and view count may be unavailable. If a valid API key is saved, the plugin can fetch richer video metadata.
