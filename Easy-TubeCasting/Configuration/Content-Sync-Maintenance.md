# Content Sync & Maintenance

Easy TubeCasting works behind the scenes to ensure your website's video feeds are always up-to-date with your YouTube channel.

## Auto-Sync

When enabled, the plugin can refresh stored playlist and channel data in the background.

- **Refresh Interval:** You can set how often a collection becomes eligible for refresh in **Easy TubeCasting > Settings**. The default is `720` minutes (12 hours), and the minimum saved value is `5` minutes.
- **Demand-Driven:** When a visitor loads a page with a stored collection that is due, the plugin queues a background refresh instead of blocking the page load.
- **API Key Required:** Automatic sync only runs when a valid YouTube Data API key is saved and automatic sync is enabled.
- **Background Queue:** Sync jobs are queued through the plugin's background job system and include retry and rate-limit safeguards.

## Manual Syncing

If you've just uploaded a new video to YouTube and want it to appear on your site immediately:

1. Go to **Easy TubeCasting > Settings**.
2. Click **Run Sync Now** to queue a refresh for all stored collections.

You can also use **Easy TubeCasting > Home**:

- **Sync Now:** Queues sync for stored collections.
- **Sync collection:** Queues a refresh for one collection from the collections table.
- **Reset collection:** Deletes the local data for one collection so it can repopulate the next time the frontend needs it.

## Managing the Database Cache

The plugin stores YouTube metadata in its own database tables to reduce repeated API calls.

- **Stored Data:** The plugin uses custom tables for videos, collections, and video-to-collection mappings.
- **Resetting a Collection:** If a feed has missing thumbnails, incorrect titles, or stale video IDs, reset that collection from **Easy TubeCasting > Home**. The plugin will fetch it again the next time it needs that collection.
- **Uninstall Cleanup:** The uninstall routine removes plugin options and the custom Easy TubeCasting tables.

## API Health Check

You can re-validate your API key at any time in the settings page to ensure it is still active, allowed to use YouTube Data API v3, and not blocked by restrictions or quota limits.
