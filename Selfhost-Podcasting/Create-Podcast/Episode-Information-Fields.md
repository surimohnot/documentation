## Episode Information Fields

This article explains the episode-level fields and how they appear in the feed.

## Required fields

| Field | Used for | Feed output |
| --- | --- | --- |
| Audio / Media URL | Episode audio | `<enclosure>` |
| Episode Title | Episode title | `<title>`, `itunes:title` when available |
| Episode Description | Show notes for podcast apps | `<description>`, `content:encoded`, `itunes:summary` excerpt |
| Publish Date | Episode release date | `<pubDate>` |

The media URL must be valid before the episode can be saved.

## Media metadata

When the episode media is saved, the plugin tries to store:

- `enclosure-src`: audio URL.
- `enclosure-length`: file size in bytes.
- `enclosure-type`: MIME type.
- `enclosure-ext`: file extension.
- `duration`: duration in seconds.

The feed displays duration as `HH:MM:SS`.

## Recommended fields

| Field | Used for | Feed output |
| --- | --- | --- |
| Episode Art Image | Episode-specific artwork | `itunes:image` |
| Episode Number | Episode order | `itunes:episode`, `podcast:episode` |
| Season Number | Season grouping | `itunes:season` |
| Episode Author | Episode author or host | `itunes:author`, `dc:creator` |
| Episode Type | Full, trailer, or bonus | `itunes:episodeType` |

## Situational fields

| Field | Used for | Feed output |
| --- | --- | --- |
| Explicit | Mark this episode explicit | `itunes:explicit` |
| Block from Apple Podcasts | Hide this episode in Apple Podcasts | `itunes:block` |
| Transcript URL | Link to transcript file | `podcast:transcript url` |
| Transcript Type | Transcript format | `podcast:transcript type` |
| Transcript Language | Transcript language | `podcast:transcript language` |
| Closed captions | Mark transcript as captions | `podcast:transcript rel="captions"` |

## Publish date behavior

Episodes are sorted newest first by post date. Only published episodes are included in the feed. If an episode is scheduled for the future, it will not appear in the feed until WordPress publishes it.

## Shared and migrated episode behavior

Some migrated episodes may be attached to more than one podcast. If an episode belongs to multiple podcasts, be careful when editing shared fields such as media URL, title, description, episode number, or explicit status because changes can affect every podcast that uses the same episode record.
