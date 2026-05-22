## What does Podcast Composer do?

It reads existing podcast RSS feeds, indexes their episodes in WordPress, and lets you generate new custom podcast RSS feeds from those episodes.

## Does it host my audio files?

No. Audio and video files stay on your original podcast host or media server.

## Does it change my original feed?

No. Source feeds are read-only from Podcast Composer's point of view.

## Can I merge multiple podcasts into one feed?

Yes. Add multiple source feeds to one project, create one output feed, and assign episodes from all sources to that output.

## Can I split one podcast into multiple feeds?

Yes. Add one source feed, create several output feeds, and assign different episodes to each output.

## Can one episode appear in multiple output feeds?

Yes. Assign the same source episode to multiple outputs.

## Can I edit episode titles and descriptions?

Yes. Open an output feed, go to `Episodes`, and click `Edit Data` for the episode. The change applies only to that output feed.

## Can I create a private paid podcast feed?

The plugin can generate a separate feed URL, but it does not include payments, access control, member authentication, or tokenized private feeds.

Use a separate membership or access-control system if you need a protected feed.

## Does it submit my feed to Apple Podcasts or Spotify?

No. You submit the generated feed URL manually.

## What is the best GUID policy?

For most new output feeds, use `Rewrite per output feed`.

Use `Preserve original source GUID` only if you intentionally want to preserve source feed identity, such as during a migration.

## Why are episodes skipped during sync?

The parser skips feed items that do not have a usable audio or video enclosure.

## How often are source feeds refreshed?

Each source can be set to hourly, twice daily, or daily. You can also click `Sync now`.

## Does it use WP-Cron?

The plugin has its own async background queue for output-feed-triggered source sync checks. Manual sync actions run through admin AJAX.

## Who can manage Podcast Composer?

Only users with the WordPress `manage_options` capability, normally administrators.

## Can visitors see my projects or source feeds?

No. Projects and outputs are stored as private internal post types. Public visitors can access generated output RSS feed URLs.

## Why does my feed look like a normal web page in the browser?

The plugin attaches an XSL stylesheet to make RSS feeds readable in browsers. Podcast apps still consume the XML.

## Can I change a feed slug after publishing?

The current admin flow creates a slug when the output feed is created. Avoid changing feed URLs after publishing because subscribers and podcast directories depend on stable URLs.
