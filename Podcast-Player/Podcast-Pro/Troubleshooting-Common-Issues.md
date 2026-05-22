Use this checklist when Podcast Player Pro features do not behave as expected.

## Pro Tools Are Missing

1. Confirm **Podcast Player Pro** is active.
2. Confirm the free **Podcast Player** plugin is active.
3. Confirm the free plugin is version `8.2.0` or higher.
4. Reload **Podcast Player** in the admin menu.

## Latest Episodes Are Missing

1. Go to **Podcast Player > Toolkit**.
2. Update the stored podcast feed data if the Feed Update tool is available.
3. Check **Podcast update interval** in settings.
4. Clear site, object, and CDN caches.
5. Confirm the RSS feed itself contains the new episode.

## Player Does Not Appear

1. Confirm the shortcode, block, or widget has a valid source.
2. For feed players, verify the RSS feed URL is public.
3. For post players, verify selected posts contain valid audio or video.
4. For single media players, verify the media URL is valid.
5. Check the browser console for JavaScript errors from the theme or other plugins.

## Imported Episodes Do Not Show Players

1. Open **Toolkit > Feed Import**.
2. Check the player placement setting.
3. Confirm the episode post has `pp_import_data` metadata by reimporting or updating the episode.
4. If placement is **Manual**, check the post content for the inserted player block.

## Statistics Are Empty

1. Enable **Collect Podcast Player Stats (Beta)**.
2. Confirm the play threshold is not too high.
3. Play an episode past the threshold.
4. Reopen the admin stats view after aggregation runs.

## Transcripts Are Missing

1. Enable **Show Episode Transcripts (Beta)**.
2. Confirm the feed includes transcript/caption metadata.
3. Confirm the caption URL is public and has an allowed content type.
4. Confirm player visibility settings do not hide episode content or transcript.
