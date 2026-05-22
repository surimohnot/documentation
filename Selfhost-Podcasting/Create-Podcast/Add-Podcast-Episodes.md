## Add Podcast Episodes

Episodes are the items inside a podcast feed. Each episode needs a valid audio URL, title, description, and publish date.

## Create an episode

1. Go to **Selfhost Podcasting**.
2. Open the podcast you want to edit.
3. Go to **Manage Episodes**.
4. Click **Create New Episode**.
5. Fill in the required fields.
6. Save the episode.

The plugin creates or updates a WordPress post for the episode and stores podcast feed metadata in post meta.

## Required episode fields

**Podcast Episode Audio / Media URL**

The direct URL to the audio file. You can use a WordPress Media Library file or an external URL. The URL must point to an actual media file, not to a landing page.

When possible, the plugin detects and stores:

- File URL.
- File size.
- MIME type.
- File extension.
- Duration.

If duration cannot be detected in the browser or during save, the plugin can queue a background repair task.

**Has the episode media changed since the last upload?**

This field appears when S3 storage is enabled and the episode already has bucket media data. Check it only when you replaced the source media and want the plugin to upload the changed file again.

**Episode Title**

The title displayed in podcast apps and directories. The plugin stores it as the WordPress post title.

**Episode Description**

The description used in the RSS feed. On first creation, this is also copied into the WordPress episode post content. After that, the feed description and website post content are independent.

**Episode Publish Date**

The release date and time. Episodes are sorted newest first in the feed. If the date is in the future, WordPress can save the post as scheduled, and the feed only includes published episodes.

## Recommended episode fields

**Episode Art Image**

Optional episode-specific artwork. If set, it outputs an episode-level `itunes:image`. If not set, podcast apps usually use the show artwork.

**Episode Number**

The episode number sent to podcast apps through `itunes:episode` and Podcasting 2.0 episode metadata.

**Season Number**

The season number sent through `itunes:season`.

**Episode Author**

The host or author for this episode. It can differ from the show author.

**Type of Episode**

Choose one:

- **Full**: a normal episode.
- **Trailer**: a preview or promotional episode.
- **Bonus**: extra content outside the normal sequence.

## Situational episode fields

**Is Episode Explicit?**

Marks only this episode as explicit.

**Should Remove Episode From Apple Podcasts?**

Outputs `itunes:block` for this episode. Use only when you intentionally want Apple Podcasts to hide this episode.

**Podcast Transcript URL**

A URL to a transcript file for the episode.

**Podcast Transcript Type**

Supported values are plain text, HTML, VTT, JSON, and SRT.

**Transcript Language**

The language code for the transcript.

**Closed captions**

Enable this when the transcript file is a captions file, such as VTT or SRT.

## Editing an existing episode

When you edit an episode:

- The episode title updates the WordPress post title.
- The feed description updates the feed metadata.
- The existing WordPress post content is preserved.
- If the media URL changes, the plugin re-checks the media metadata.
- If S3 storage is enabled, changed media can be queued for upload.

## Deleting an episode

Deleting an episode removes it from the podcast feed. If S3 storage is enabled and bucket media data exists for that episode, the plugin queues a background task to remove the object from the bucket.

Migrated or shared source posts can be detached from a podcast instead of always being permanently deleted. The plugin keeps track of podcast associations so one source post can belong to more than one migrated feed when safe.
