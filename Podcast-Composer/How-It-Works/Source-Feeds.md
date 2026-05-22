A source feed is an existing podcast RSS feed that Podcast Composer reads and indexes.

## Add a Source Feed

1. Open a project.
2. In the `Sources` panel, click `Add Source Feed`.
3. Paste the source RSS feed URL.
4. Submit the form.

The plugin validates the URL, fetches the feed, parses it, and stores episode data.

If the source feed cannot be fetched or has no usable episodes, the source is not created.

## What Makes a Good Source Feed

A source feed should:

- Be publicly reachable over HTTP or HTTPS.
- Return valid XML.
- Include RSS channel data.
- Include episode items.
- Include audio or video enclosure URLs.
- Use stable GUIDs when possible.
- Include publish dates.

Podcast Composer can read common podcast namespaces, including:

- RSS 2.0.
- iTunes podcast tags.
- Atom links and author data.
- Podcasting 2.0 transcript, locked, funding, GUID, and TXT data.
- Dublin Core creator.
- Media RSS audio/video content.

## Source Episodes

After syncing, open a source feed and use the `Episodes` tab.

You can:

- Search episodes.
- Filter by assignment status.
- Select episodes.
- Add selected episodes to an output feed.

The episode list is sorted newest first in the admin workspace.

## Source Settings

Open a source and go to the `Settings` tab.

This screen shows source channel data such as:

- Feed URL.
- Title.
- Description.
- Language.
- Author.
- Categories.

It also includes:

- `Auto-update interval`
- `Default destination for new episodes`
- `Sync now`

## Auto-Update Interval

The source auto-update interval controls how often the source is considered due for background sync.

Options:

- `Hourly`
- `Twice Daily`
- `Daily`

The default is `Twice Daily`.

Background sync checks can run when visitors request output feed URLs. If the interval has not elapsed, the source is skipped.

## Default Destination

The Source Settings screen includes `Default destination for new episodes`.

In the current implementation, episode assignment is still performed manually from the source `Episodes` tab by selecting episodes and using `Add to Output`. Treat the default destination setting as a saved preference/reserved workflow unless your installed version adds automatic assignment behavior.

## Manual Sync

Click `Sync now` to refresh one source immediately.

Manual sync is useful when:

- You just published a new episode on your original podcast host.
- A source feed previously failed.
- You changed source metadata and want the latest data available for import.

## Source Sync Results

When sync succeeds, the source status becomes active and the plugin reports how many episodes were indexed.

When sync fails, the source stores:

- Last HTTP response code.
- Last error message.
- Error status.

Existing indexed episodes are not automatically removed just because one sync fails.

## Delete a Source

Deleting a source removes:

- The source record.
- Episodes indexed from that source.
- Output feed mappings for those episodes.

It does not affect the original RSS feed or audio files on your podcast host.
