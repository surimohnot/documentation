Episode overrides let you change how an episode appears in one output feed without changing the source feed.

## When to Use Overrides

Use overrides when:

- A title should be different in a curated feed.
- A description needs to be shorter or more polished.
- An episode needs output-specific artwork.
- You want to add or replace transcript data.
- You want a different episode number or season number.
- You want to block one episode from Apple Podcasts in one output feed.

## Open the Episode Override Editor

1. Open a project.
2. Open an output feed.
3. Go to the output `Episodes` tab.
4. Find the episode.
5. Click `Edit Data`.

The modal shows editable fields for that episode in this output feed.

## Override Fields

The override editor supports:

- Title.
- Description.
- iTunes Summary.
- Author.
- DC Creator.
- Episode Link.
- Episode Image URL.
- Episode Number.
- Season Number.
- Episode Type.
- Block Episode.
- Transcript URL.
- Transcript Type.
- Transcript Language.
- Transcript Rel.

## Episode Type Values

Supported values are:

- `full`
- `trailer`
- `bonus`

Leave the field empty if you do not want to override the source value.

## Block Episode

The `Block Episode` setting controls the iTunes episode block tag for this output.

Values:

- Empty: no override.
- `yes`: block the episode.
- `no`: explicitly do not block the episode.

## Transcript Override

Transcript fields generate `podcast:transcript` metadata.

Common transcript MIME types:

```
text/plain
text/html
application/json
application/srt
text/vtt
```

Example:

```
Transcript URL: https://example.com/transcripts/episode-12.vtt
Transcript Type: text/vtt
Transcript Language: en
Transcript Rel: captions
```

## Saving Overrides

Click `Save Episode Data`.

The plugin saves only fields that differ from the original values or have actual override content.

Saving an override:

- Stores override data in the episode-output mapping.
- Clears the output feed XML cache.
- Refreshes validation status.

## Clearing an Override

To clear an override:

1. Open the episode override editor.
2. Remove the custom value.
3. Save.

If the form has no changes compared with the original source data, the plugin closes the modal and reports that there are no changes to save.

## What Overrides Do Not Change

Overrides do not change:

- The original podcast host.
- The source RSS feed.
- Other output feeds.
- The indexed source record itself.

Overrides are applied only when generating the specific output feed where the override was saved.
