## Import Episodes from an RSS Feed

The episode importer copies selected episodes from an existing podcast RSS feed into a Selfhost Podcasting podcast.

This is different from the migration tools for PowerPress and Seriously Simple Podcasting. The RSS importer reads a feed URL; the migration tools read another WordPress plugin's local data.

## Import steps

1. Go to **Selfhost Podcasting**.
2. Open the destination podcast.
3. Go to **Manage Episodes**.
4. Choose **Import Episodes**.
5. Paste the source RSS feed URL.
6. Click **Show Episodes List**.
7. Select the episodes you want to import.
8. Click **Import Episodes**.
9. Review imported episodes and edit metadata if needed.

## What is imported

The importer attempts to map common RSS item data into Selfhost episode data:

- Episode title.
- Episode description.
- Publication date.
- Audio enclosure URL.
- File length and MIME type when available.
- Duration when available.
- Episode image when present.
- Episode author when present.
- GUID or an internally generated GUID.

The importer keeps the original media URL by default. It does not automatically download every remote audio file into your Media Library.

## Feed caching during import

When you fetch a source feed, the plugin stores the parsed feed data in a temporary cache for one hour. This lets you select episodes and run the import without re-fetching the remote feed on every step.

After a successful import, the cached feed data for that URL is deleted.

## Hosting options after import

You have three common options:

**Keep the original audio URL**

This is the simplest path. The feed points to the audio file on the original host. Use this only if you control that host or have permission to keep using those URLs.

**Move audio into WordPress**

Download the audio files, upload them to the WordPress Media Library, and replace the imported episode media URLs.

**Move audio to S3-compatible storage**

Configure S3 storage for the podcast, then upload or re-upload episode media through the plugin's bucket workflow.

## Large imports

For very large shows:

- Import in batches.
- Start with 20 to 50 episodes per batch if your server has strict limits.
- Run imports during low-traffic periods.
- Check the **Error Log** if background uploads or duration repair tasks fail.
- Confirm your host allows outbound HTTP requests to the source feed and media URLs.

## Common import problems

**The feed cannot be fetched**

Check that the URL is public, returns valid RSS XML, and is not blocked by a firewall, bot protection, or authentication requirement.

**No episodes appear**

The source feed may have no readable `<item>` entries, no enclosures, or unsupported formatting.

**Imported episodes have no duration**

Some feeds omit duration or use media URLs that cannot be inspected. The plugin may attempt a background duration repair, but some hosts block the required metadata checks.

**The audio URL works in a browser but not in podcast apps**

Make sure the URL points directly to an audio file and returns the correct content type. Avoid player pages, tracking pages that do not redirect correctly, and expiring signed URLs.
