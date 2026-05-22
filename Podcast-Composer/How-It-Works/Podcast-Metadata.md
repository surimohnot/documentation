Podcast metadata controls the `<channel>` section of the generated RSS feed. This is the information podcast apps display for the show itself.

## Open Podcast Metadata

1. Open a project.
2. Open an output feed.
3. Click the `Podcast Metadata` tab.

## Import Metadata From a Source Feed

To save time:

1. Choose a source feed in `Import Podcast Metadata`.
2. Click `Fetch from Source`.
3. Review the imported values.
4. Edit anything that should differ in the output feed.
5. Click `Save podcast metadata`.

Importing metadata does not change the source feed. It copies channel information into the output feed settings.

## Fields Shown in the Admin UI

The current admin screen exposes these core fields:

| Field | Purpose |
| --- | --- |
| Feed title | The podcast title shown in apps. |
| Description | The main show description. |
| Channel Link | Website URL for the podcast or publisher. |
| Artwork | Podcast artwork URL. |
| Categories | Podcast category text. |
| Explicit flag | Whether the show contains explicit content. |
| Language | Language code, such as en-us. |
| Owner name | Podcast owner contact name. |
| Owner email | Podcast owner contact email. |

## Required Metadata for Most Directories

Before submitting a feed, make sure you have:

- Title.
- Description.
- Website link.
- Artwork.
- At least one category.
- Explicit or clean setting.
- Language.
- Author or publisher information.
- Owner name and owner email.
- At least one episode.

Podcast Composer's Validation tab checks the most important required fields.

## Artwork Guidelines

For broad podcast directory compatibility, use artwork that follows Apple Podcasts style requirements:

- Square image.
- JPEG or PNG.
- At least 1400 x 1400 pixels.
- No larger than 3000 x 3000 pixels.
- RGB color.
- Publicly reachable URL.

If you change artwork later, many podcast apps cache images. Use a new filename and URL when replacing artwork.

## Categories

The admin UI stores category text. Use podcast directory category names, separated clearly if you use more than one.

Examples:

```
Business
Education
Society & Culture
Technology
True Crime
```

If importing from a source feed, the plugin can preserve source categories. Some nested categories may appear as combined text such as:

```
Society & Culture > Documentary
```

## Explicit Flag

Set `Explicit flag` to:

- `No` for clean content.
- `Yes` for explicit content.

Do not leave this unset before submitting the feed.

## Language

Use a language code recognized by podcast directories.

Common examples:

```
en-us
en-gb
en-au
es
fr
de-de
hi
```

## Metadata Imported or Stored Behind the Scenes

The feed parser and generator support more channel fields than the current core UI exposes directly.

When imported from a source feed or stored programmatically, output feeds can include fields such as:

- iTunes summary.
- Copyright.
- iTunes author.
- Podcast type.
- iTunes block.
- iTunes complete.
- iTunes new-feed-url.
- Podcast GUID.
- Podcast TXT.
- Podcast locked.
- Podcast funding.

If you need to edit these fields manually and they are not visible in your admin UI, a developer can extend the admin interface using the plugin's data structures and filters.

## Saving Metadata

Click `Save podcast metadata` after editing.

Saving metadata:

- Sanitizes the values.
- Updates the output feed settings.
- Clears the generated feed cache.
- Refreshes output validation status.
