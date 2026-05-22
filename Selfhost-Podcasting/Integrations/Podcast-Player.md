## Podcast Player Integration

Selfhost Podcasting can integrate with the **Podcast Player** WordPress plugin. When Podcast Player is active, Selfhost can register the podcast feed with Podcast Player and optionally insert a player into newly created episode posts.

## Requirements

- The Podcast Player plugin must be installed and active.
- The podcast must be public. Private podcasts are skipped by the Podcast Player integration because private tokenized feeds should not be registered as public player sources.

## Open the settings

1. Go to **Selfhost Podcasting**.
2. Open a podcast.
3. Go to **Connect Services**.
4. Open **Podcast Player**.

If Podcast Player is not active, the settings area shows an install/activate notice instead of player options.

## Available settings

**Automatically add podcast player to newly created episode post**

When enabled, newly created episode posts receive a Podcast Player embed in the post content.

**Share show details with Podcast Player**

Lets Podcast Player use Selfhost show artwork, episode count, style, and subscribe links as fallback values while Podcast Player's own configured defaults still take priority.

**Method to insert podcast player**

Choose the insert method:

- **Editor Block**
- **Shortcode**

**Podcast Player default display style**

Choose the player style where supported. The available values are controlled by the installed Podcast Player version.

**Podcast Player accent color**

Set a hex color such as `#d9480f`.

**Hide Episode Download Button**

Hides the download control in the player.

**Hide Social Sharing Button**

Hides player social sharing controls.

## How syncing works

Selfhost Podcasting listens for podcast, episode, media, migration, privacy, and takeover changes. When relevant data changes, it can refresh the Podcast Player feed source.

The integration can:

- Register a Selfhost feed with Podcast Player.
- Update the registered feed URL when feed takeover changes the public URL.
- Refresh Podcast Player data after an episode is saved or deleted.
- Refresh after media is moved to bucket storage.
- Hand off migrated feeds to an existing Podcast Player feed entry when a matching source feed URL exists.
- Delete managed player assets when the podcast is deleted.

## Private podcast behavior

When a podcast is private, Selfhost deletes or skips managed Podcast Player assets for that podcast and records a skipped private status internally. Private tokenized feeds should be shared through the private podcasting tools, not through a public feed player registration.

## Troubleshooting

**The settings are missing**

Install and activate Podcast Player, then reload the Selfhost podcast screen.

**The player does not appear in old episode posts**

Automatic insertion applies to newly created episode posts. Existing posts may need manual editing or a manual Podcast Player block/shortcode.

**The player uses an old feed**

Save the podcast or integration settings again, then check whether a caching plugin or Podcast Player cache needs refreshing.

**Private podcasts are skipped**

This is expected. Use private podcast feed shortcodes or subscriber URLs instead.
