## Publishing to Podcast Directories

Selfhost Podcasting creates the RSS feed. Podcast directories still require you to submit that feed URL through their own publisher portals.

## Before submitting

Complete this checklist first:

- The site uses HTTPS.
- The feed URL opens publicly.
- The show has title, description, artwork, website, language, category, and author.
- Artwork is square and at least 1400 x 1400 pixels.
- At least one episode is published.
- Each episode has a direct audio enclosure URL.
- The media URL does not require a logged-in browser session unless using a private podcast workflow.
- The feed has no visible PHP warnings or HTML before the XML.
- The browser preview looks correct.

## Where to submit

Common directories include:

- Apple Podcasts Connect.
- Spotify for Podcasters.
- YouTube Music / YouTube Studio podcast tools.
- Amazon Music for Podcasters.
- Podcast Index.
- Pocket Casts.
- Overcast and other apps that read open RSS feeds.

Each service has its own account, verification, review, and approval process.

## Keep the feed URL stable

After a directory accepts the feed, avoid changing the podcast slug unless you know how to redirect or migrate the feed.

If you must move the show to a new feed URL, use the **iTunes New Feed URL** field and keep the old feed available long enough for subscribers and directories to pick up the change.

## Directory approval delays

Some directories show changes quickly. Others can take hours or days to refresh metadata, artwork, or episode lists.

If Selfhost Podcasting shows the correct feed but a directory does not, check:

- Whether the directory has refreshed the feed.
- Whether the directory cached old artwork.
- Whether the new episode publish date is in the future.
- Whether the directory rejected an audio URL, image size, or required field.

## Public feeds and private feeds

Public directories generally expect public feeds. A Pro private feed with a tokenized URL should be shared only with authorized subscribers and is not normally submitted to open public directories.
