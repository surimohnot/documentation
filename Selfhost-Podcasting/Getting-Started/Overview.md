Selfhost Podcasting is a WordPress podcast feed manager. It helps you create one or more podcast shows, enter show and episode metadata, and publish RSS feeds that podcast directories can read.

The plugin focuses on the feed and the publishing workflow. It does not move your podcast into a hosted SaaS account. Your podcast data remains in WordPress, and optional integrations can be enabled only when you need them.

Introductory video: https://youtu.be/IPdc4naKSaY

## What the plugin creates

Selfhost Podcasting registers two main content types:

- **Selfhost Podcast**: the show-level record. This stores the feed slug, show title, description, artwork, language, categories, owner details, feed settings, and integration settings.
- **Podcast Episode**: the episode-level record. This stores the media URL, title, description, publish date, duration, season, episode number, episode type, artwork, transcript details, and other episode metadata.

Each podcast receives its own feed URL. With pretty permalinks enabled, the feed normally looks like:

`https://example.com/feed/my-podcast-slug`

If pretty permalinks are disabled, WordPress serves the same feed through a query URL:

`https://example.com/?feed=my-podcast-slug`

## Main features

- Create and manage multiple podcast feeds from one WordPress dashboard.
- Add podcast-level metadata required by Apple Podcasts, Spotify, and other podcast apps.
- Add episode-level metadata including media URL, duration, publish date, explicit flag, season, episode number, episode type, artwork, and transcript data.
- Import episodes from an external RSS feed.
- Migrate shows from supported existing podcast plugins.
- Preview the feed in a browser-friendly page without changing the XML feed.
- Limit how many episodes appear in a feed.
- Connect Podcast Player for website playback.
- Add a third-party analytics prefix for services such as Podtrac, Blubrry, or OP3.
- Upload audio to Cloudflare R2, Amazon S3, Wasabi, or another supported S3-compatible provider through the S3 handler.
- View background job errors and resume interrupted jobs.
- Use private podcast feeds and subscriber tokens when the Pro module is available.

## Who should use it

Selfhost Podcasting is useful for:

- Independent creators who want their own RSS feed.
- Agencies managing podcasts for clients.
- Networks that need more than one show inside one WordPress site.
- Site owners migrating away from another WordPress podcast plugin.
- Developers who want podcast data stored in WordPress and exposed through predictable post/meta structures.
- Publishers who want optional private podcast access without handing the whole feed workflow to a hosted platform.

## What it does not do automatically

Selfhost Podcasting generates and manages the RSS feed, but podcast directories do not discover every new feed automatically. You still submit the feed URL to Apple Podcasts, Spotify for Podcasters, YouTube Music, Amazon Music, Pocket Casts, and any other directory where you want the show listed.

The plugin also does not guarantee that every remote audio URL can be inspected for duration or size. When possible, it reads metadata from WordPress attachments, remote headers, or remote files. If duration cannot be detected immediately, it can queue a background duration repair task.

## Requirements

- WordPress 6.0 or newer.
- PHP 7.4 or newer.
- A working WordPress cron or loopback request setup for background uploads and metadata repair.
- HTTPS is strongly recommended for public feeds and required by many directories.
- Large enough server upload, memory, and execution limits for your audio workflow.

Optional integrations have their own requirements:

- Podcast Player plugin must be installed and active for Podcast Player integration.
- A valid analytics prefix is required for third-party analytics.
- Valid object storage credentials are required for S3-compatible storage.
- Pro private podcasting requires the Pro module and, for automatic access, one of the supported commerce or membership plugins.
