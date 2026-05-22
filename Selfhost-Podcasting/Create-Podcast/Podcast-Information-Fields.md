## Podcast Information Fields

This article explains the podcast-level fields and how they appear in the RSS feed.

## Required fields

| Field | Used for | Feed output |
| --- | --- | --- |
| Podcast Name | Public show title | `<title>` |
| Podcast Description | Show description | `<description>`, `itunes:summary` excerpt |
| Podcast Cover Art | Show artwork | `itunes:image` |
| Podcast Website | Show website | `<link>` |
| Language | Show language | `<language>` |
| Apple Podcast Categories | Directory category | `itunes:category` |
| Podcast Author | Show author | `itunes:author` |

Required fields should be completed before submitting the feed to directories.

## Recommended fields

| Field | Used for | Feed output |
| --- | --- | --- |
| Episodic or Serial | Listening order style | `itunes:type` |
| Copyright | Show copyright | `<copyright>` |
| Owner Name | Directory contact | `itunes:owner/itunes:name` |
| Owner Email | Directory contact and locked owner | `itunes:owner/itunes:email`, `podcast:locked owner` |
| Funding URL | Support page | `podcast:funding url` |
| Funding Label | Support link text | `podcast:funding` value |

## Management fields

| Field | Used for | Feed output |
| --- | --- | --- |
| Explicit | Mark show explicit | `itunes:explicit` |
| Block from Apple Podcasts | Hide show in Apple Podcasts | `itunes:block` |
| Completed | Mark show complete | `itunes:complete` |
| Locked | Discourage unauthorized feed imports | `podcast:locked` |
| iTunes New Feed URL | Move subscribers to a new feed | `itunes:new-feed-url` |
| Apple verification token | Verify show ownership | `podcast:txt` and legacy Apple verification tag |

## Artwork guidance

Use show artwork that is:

- Square.
- JPG or PNG.
- At least 1400 x 1400 pixels.
- Ideally 3000 x 3000 pixels.
- Readable at small sizes.
- Not transparent if submitting to directories that reject transparent artwork.

The plugin validates square image dimensions in the admin experience.

## Category guidance

Choose the category that best describes the whole show, not only one episode. If a category has a subcategory, choose the closest available match.

Podcast directories may use the first category as the primary discovery category.

## When to use advanced fields

Use advanced fields only when needed:

- Use **Block** when deliberately removing the show from Apple Podcasts.
- Use **Complete** when no more episodes are expected.
- Use **New Feed URL** only for a permanent feed move.
- Use **Locked** when you want to signal feed ownership.
- Use **Apple verification** only with a token supplied by Apple.
