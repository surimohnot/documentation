# Introduction to Easy TubeCasting

**Easy TubeCasting** is a WordPress block plugin for displaying YouTube videos, playlists, channels, usernames, and handles in a responsive Spotlight player. It can show one video, a hand-picked comma-separated list of videos, or a synced YouTube collection.

## Why Easy TubeCasting?

- **Modern Spotlight Player:** A large video area with an interactive playlist rail when multiple videos are available.
- **Flexible Embedding:** Supports single videos, comma-separated video URLs, playlists, channel IDs, username URLs, and YouTube handles.
- **No API Key for Basic Videos:** Single videos and specific video lists can use YouTube oEmbed data.
- **API-Powered Collections:** Playlists, channels, usernames, and handles use the YouTube Data API v3 to import video lists and richer metadata.
- **Frontend Controls:** Visitors can use custom play/pause, seek, volume, fullscreen, and captions controls when playback is available.
- **Playlist Tools:** Multi-video blocks include search, sorting, and Load More controls.
- **Admin Sync Tools:** The admin area shows indexed collections and videos, supports manual sync, single-collection sync, and collection reset.
- **Local Cache:** Video and collection metadata is stored in custom database tables to reduce repeated remote requests.

## Core Concepts

The plugin works through the **Easy TubeCasting** block in the WordPress block editor. Paste a YouTube URL into the block, configure the display options in the sidebar, and publish the page.

Single videos and comma-separated video URLs do not require a YouTube Data API key. Playlists, channels, usernames, and handles require a valid **YouTube Data API v3 key** because YouTube must provide the list of videos inside that collection.

When an API key is saved, the plugin validates it, stores it in plugin options, masks it in the admin UI, and uses it for collection imports, richer video metadata, and sync jobs.
