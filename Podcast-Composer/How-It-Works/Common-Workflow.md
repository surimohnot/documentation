This section shows practical ways to use Podcast Composer.

## Merge Multiple Shows Into One Feed

Use this when you run a network or want one combined feed.

1. Create a project named `Network Feed`.
2. Add each show as a source feed.
3. Create one output feed named for the network.
4. Import metadata from one source or fill new network metadata.
5. Select episodes from each source.
6. Add them to the network output feed.
7. Set sorting to `Newest first`.
8. Validate and publish the output feed URL.

## Split One Show Into Multiple Feeds

Use this when one podcast should become several focused feeds.

1. Create a project for the show.
2. Add the original show RSS feed as the source.
3. Create multiple output feeds, such as:

- `Full Episodes`
- `Bonus Episodes`
- `Season 1 Archive`
- `Interviews Only`

1. Assign different episodes to each output.
2. Adjust metadata for each output.
3. Validate each output separately.

## Build a Best-Of Feed

1. Create or open a project.
2. Add the source feed or feeds.
3. Create an output feed named `Best Of`.
4. Search and select only the strongest episodes.
5. Add them to the output.
6. Use episode overrides to polish titles and descriptions.
7. Set episode limit if needed.
8. Validate and publish.

## Rebrand a Feed Without Moving Audio

1. Add the existing feed as a source.
2. Create a new output feed with the new brand name and slug.
3. Import source metadata.
4. Replace title, artwork, description, owner, and category as needed.
5. Assign episodes.
6. Use overrides for episodes that need new naming.
7. Validate the feed.

Audio files remain on the original host.

## Create a Partner or Syndication Feed

1. Create an output feed for the partner.
2. Use a partner-specific slug.
3. Assign only approved episodes.
4. Customize title, description, and artwork.
5. Use overrides where partner-specific wording is needed.
6. Share only that output feed URL with the partner.

## Create a Limited Archive Feed

1. Create an output feed.
2. Add all relevant archive episodes.
3. Open `Advanced`.
4. Set `Sorting logic` to `Oldest first` if the archive should play chronologically.
5. Set `Episode limit` if you want only the first N episodes.
6. Validate and publish.

## Premium and Public Feed Strategy

Podcast Composer can generate separate public and premium-style feeds if you have a separate system for controlling access to the feed URL.

Example:

- `public-show`: free promotional episodes.
- `subscriber-feed`: full or bonus catalog.

Important: this plugin does not include built-in subscription access control, tokenized feeds, payments, or private feed authentication.
