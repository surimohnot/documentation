Use this guide when something does not work as expected.

## Source Feed Will Not Add

Possible causes:

- The URL is not valid HTTP or HTTPS.
- The feed is not publicly reachable.
- The server blocks WordPress HTTP requests.
- The feed returns invalid XML.
- The feed has no usable episode items.
- Episode items do not include audio or video enclosures.

What to try:

1. Open the source feed URL in a browser.
2. Confirm it shows RSS/XML content.
3. Confirm episodes have media enclosure URLs.
4. Try syncing again.
5. Check whether a firewall or security plugin blocks outbound requests.

## Source Sync Fails

Possible causes:

- Source host is down.
- Source host blocks your server.
- Feed XML is temporarily invalid.
- The request times out.
- The feed redirects to a blocked URL.

What to try:

1. Click `Sync now` again after a few minutes.
2. Check the source feed URL directly.
3. Contact the source host if the feed is unavailable.
4. Check server/PHP error logs.

The plugin uses a 10-second HTTP timeout when fetching source feeds.

## No Episodes Appear After Sync

Podcast Composer only indexes items with usable media.

Check whether the source feed episodes include:

- `<enclosure>` tags with audio/video URLs.
- Or Media RSS audio/video content.

If episodes are missing enclosures, the plugin skips them.

## Output Feed Shows Incomplete

Open the output `Validation` tab.

Common fixes:

- Add podcast metadata.
- Add artwork.
- Set explicit flag.
- Add a category.
- Assign at least one episode.
- Add missing episode description or title through an override.

## Output Feed URL Gives 404

Try these steps:

1. Go to `Settings > Permalinks`.
2. Click `Save Changes`.
3. Reload the output feed URL.
4. Confirm the output feed still exists.
5. Confirm the slug in the URL matches the output feed slug.

If pretty permalinks are disabled, try:

```
https://example.com/?feed=your-slug
```

## Output Feed Does Not Show New Episodes

Try:

1. Sync the source manually.
2. Confirm the new episode appears in the source `Episodes` tab.
3. Add the episode to the output feed.
4. Wait up to a few minutes for feed XML cache to clear.
5. Reload the public output feed URL.

Source sync does not automatically assign every new episode to every output feed in the current implementation. Add episodes to outputs manually unless your installed version provides automatic assignment behavior.

## Feed Opens as a Styled Page Instead of XML

This is expected. The plugin attaches an XSL stylesheet so humans can read the feed in a browser.

Podcast apps still read the XML.

Use browser view-source or a feed validator if you need to inspect raw XML.

## Podcast Directory Still Shows Old Data

Podcast apps and directories cache RSS feeds and artwork.

Try:

1. Confirm the output feed URL shows the new data.
2. Wait for the directory cache to refresh.
3. Use the directory's refresh tool if available.
4. For artwork changes, use a new image filename and URL.

## Episode Appears as New Again

This can happen if GUID behavior changes.

Avoid changing:

- GUID policy after publishing.
- Source GUIDs.
- Output feed slug.

Use `Rewrite per output feed` unless you have a specific migration reason to preserve original GUIDs.

## WordPress Admin AJAX Errors

The admin UI uses WordPress `admin-ajax.php`.

If actions fail:

1. Confirm you are logged in as an administrator.
2. Refresh the page to renew the nonce.
3. Check browser console errors.
4. Check security plugins or firewalls.
5. Check PHP error logs.
