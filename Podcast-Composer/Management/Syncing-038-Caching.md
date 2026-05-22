Synchronization is the backbone of Podcast Composer. It ensures that your distribution engine is always "listening" for new content.

### How Sync Works

The plugin uses a hybrid sync model:

1. **Background Cron**: WordPress runs a scheduled task (usually twice daily) to check all your sources for new episodes.
2. **Proactive Check**: Every time a listener or a podcast directory (like Apple) requests your **Output Feed**, the plugin performs a quick check to see if the sources haven't been synced recently.

### Sync Statuses

In your Sources manager, you will see different status indicators:

- **Active / Synced**: Everything is working perfectly.
- **Syncing...**: The plugin is currently fetching data in the background.
- **Error**: There was a problem reaching the source URL.
- **Paused**: Automatic sync has been disabled for this source.

### Troubleshooting Sync Errors

If a source shows an **Error** status:

1. **Check the URL**: Ensure the RSS URL is still valid and hasn't changed.
2. **HTTP Codes**: The plugin logs the "HTTP Code" (e.g., 404 Not Found, 500 Server Error). Check the source logs for details.
3. **Manual Sync**: Try clicking the **Sync Now** button to force a refresh.
4. **Server Block**: Some hosting providers block "Loopback Requests." If manual sync works but background sync doesn't, contact your host to ensure WordPress can "talk to itself."

### Understanding Caching

To keep your site fast, Podcast Composer caches your feeds.

- **Default Cache**: 3 hours (180 minutes).
- **Cache Invalidation**: The cache is automatically cleared whenever you:
- Map or unmap an episode.
- Save an override.
- Change show-level settings (Title/Artwork).
- Successfully sync a new episode from a source.

### Managing Large Databases

If you have dozens of sources with thousands of episodes, the database can grow large.

- **Orphaned Episodes**: When an episode is removed from a source feed, the plugin marks it as "Orphaned." You can safely delete these via bulk actions to save space.
- **Background Jobs**: The plugin processes large syncs in small batches to avoid timing out your server.
