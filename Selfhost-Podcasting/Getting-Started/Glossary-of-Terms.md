## Glossary of Terms

Use this glossary when reading the rest of the documentation.

**RSS feed**

The public XML document that podcast apps read. It contains show information, episode information, and links to each episode audio file.

**Feed URL**

The web address of the RSS feed. Example: `https://example.com/feed/my-show`.

**Podcast**

In this plugin, a podcast is the show-level record. It stores the show name, description, artwork, categories, language, owner information, feed slug, settings, and integrations.

**Episode**

An individual audio item inside a podcast feed. Each episode has its own title, description, media URL, publish date, duration, and optional metadata.

**Enclosure**

The RSS tag that points to the episode audio file. Podcast apps use the enclosure URL, file size, and MIME type to download or stream the episode.

**Media URL**

The direct URL to the audio file for an episode. It can be a WordPress Media Library URL, a remote audio URL, or a cloud storage URL after S3 upload.

**Metadata**

Structured information about a podcast or episode, such as author, category, artwork, season number, episode number, transcript URL, and explicit status.

**Podcast artwork**

The square image used by podcast directories and apps. Apple Podcasts commonly expects JPG or PNG artwork between 1400 x 1400 and 3000 x 3000 pixels.

**Episode artwork**

An optional image for a single episode. If no episode image is set, podcast apps often use the show artwork.

**Podcast category**

The Apple Podcasts category and subcategory used to classify the show in directories.

**Explicit flag**

A show-level or episode-level flag indicating explicit content. In the feed, this is output as an `itunes:explicit` value.

**Episodic podcast**

A show where episodes can usually be listened to in any order.

**Serial podcast**

A show where episodes are normally meant to be listened to in sequence, often by season.

**Episode type**

The type sent to podcast apps: `full`, `trailer`, or `bonus`.

**Transcript**

A text or caption file linked to an episode. The plugin can output Podcasting 2.0 transcript metadata for plain text, HTML, VTT, JSON, or SRT files.

**Feed preview**

The browser-friendly HTML page generated from the same podcast data. It helps you inspect the show and episodes without reading raw XML.

**Analytics prefix**

A redirect URL placed before episode media URLs so a third-party analytics provider can measure downloads before redirecting to the real media file.

**S3-compatible storage**

Object storage that works with the S3 API, such as Cloudflare R2, Amazon S3, or Wasabi. The plugin can upload episode audio there and use the uploaded URL in the feed.

**Background job**

An asynchronous task processed after the main admin action. The plugin uses background jobs for media uploads, media deletion, and missing duration repair.

**Feed takeover**

A migration feature where Selfhost Podcasting serves a migrated feed at the original source plugin feed URL, when supported and enabled.

**Private podcast**

A Pro feature where a feed requires an access token. Each subscriber receives a unique feed URL.

**Token**

The secret part of a private podcast URL. It identifies and authorizes a subscriber feed request.

**Subscriber**

In private podcasting, a WordPress user or guest identity that has been issued private feed access.
