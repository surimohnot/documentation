Podcast Composer keeps source feed data fresh and avoids regenerating feed XML more often than necessary.

## Source Sync

Source sync fetches a source RSS feed and updates the local WordPress episode index.

During sync, the plugin:

1. Fetches the source feed URL.
2. Parses XML.
3. Extracts channel metadata.
4. Extracts episode metadata.
5. Marks existing source episodes as orphaned.
6. Upserts current source episodes.
7. Marks current episodes as not orphaned.
8. Updates source status and last sync time.
9. Clears related output feed caches.
10. Refreshes output validation status.

## Manual Sync

Manual sync is available at two levels:

- Project sync: syncs all sources in a project.
- Source sync: syncs one source feed.

Use manual sync when you need an immediate update.

## Auto-Update Interval

Each source has an auto-update interval:

- Hourly.
- Twice Daily.
- Daily.

The plugin checks whether a source is due before syncing it in the background.

## Background Jobs

Podcast Composer includes its own background job queue.

It does not rely on WP-Cron for the main output-feed-triggered background sync behavior.

When someone requests an output feed URL, the feed generator can schedule a project source sync task. The background processor later checks which sources are due and syncs only those.

## Background Job Safeguards

The queue includes safeguards:

- Process lock to avoid overlapping runs.
- Dispatch interval throttling.
- Maximum dispatch count per window.
- Consecutive error blocking.
- Retry attempts for failed tasks.
- Memory limit checks.

## Feed XML Cache

Generated output feed XML is cached in a WordPress transient.

Default cache duration:

```
180 seconds
```

This keeps feed requests fast while still allowing changes to appear quickly.

## Cache Invalidation

The plugin clears output feed cache when you:

- Save output metadata.
- Save advanced settings.
- Add episodes to an output.
- Remove episodes from an output.
- Save episode overrides.
- Sync a source.
- Delete a source.
- Delete an output.

## Why a Feed May Not Update Instantly

If you open a feed immediately after a source host changes, there can be several layers of delay:

- The source feed may not have updated yet.
- The source sync interval may not be due.
- The output feed XML cache may still be active for up to 180 seconds.
- Podcast apps and directories often cache RSS feeds independently.

Use `Sync now` on the source and then reload the public output feed after a few minutes.

## If Background Jobs Stop

If background jobs appear stuck:

1. Try manually syncing the source.
2. Confirm `admin-ajax.php` is reachable.
3. Check for security plugins blocking internal admin AJAX requests.
4. Check PHP error logs.
5. Confirm your server can make HTTP requests to its own WordPress URL.
