The Feed Import tool creates WordPress posts from podcast feed episodes. Use it when each episode should have its own URL, post content, taxonomy terms, and optional single-episode player.

## Start Import Setup

1. Go to **Podcast Player > Toolkit > Feed Import**.
2. Select an existing saved podcast or enter a podcast feed URL.
3. Click **Start Import Setup**.
4. Wait for the episode list and import settings to load.

## Choose Episodes

1. Open **Episodes to Import**.
2. Select the episodes to import.
3. If all episodes are already imported, the tool shows that no new episodes are available.

## Configure Post Settings

1. Choose whether to use the episode image as the post featured image.
2. Choose the target post type.
3. Choose whether feed categories or tags should be imported.
4. Optionally assign existing site taxonomies to every imported episode.
5. Choose the post author.
6. Choose the post status:

- Publish
- Save as Draft

## Configure Player Placement

Choose where the single episode player should appear:

- Before post content.
- After post content.
- Manual placement using an editor block inserted into the content.
- Do not display a podcast audio player.

## Save and Import

1. Choose player style, subscription menu, colors, and visibility options.
2. Enable **Import future episodes automatically when this feed updates** if needed.
3. Click **Save Settings & Import Episodes** when episodes are selected.
4. If no episodes are selected, the button saves import settings only.

## View Imported Episodes

1. Go to **Podcast Player > Toolkit > Feed Import**.
2. Select the podcast.
3. Open **Imported Episodes**.
4. Review the imported episode list and linked WordPress posts.

## Update Imported Episodes

Use this when feed data has changed and imported posts should be refreshed.

1. Open **Imported Episodes**.
2. Select the imported episodes.
3. Click **Update**.
4. Wait for the success message.

Updating imported episodes refreshes the selected WordPress posts from the current stored podcast feed data.

## Delete Imported Episodes

Use this when imported episode posts should be removed from WordPress.

1. Open **Imported Episodes**.
2. Select the imported episodes.
3. Click **Delete**.
4. Confirm if prompted.
5. Wait for the success message.

Deleting imported episodes removes the related WordPress posts and clears their imported `post_id` reference in stored podcast data. It does not delete the original podcast feed.

## Notes

- Manual placement applies only to episodes imported after the setting is saved.
- Changing placement later does not move players already inserted into imported posts.
- Feed import settings and import history are stored against the podcast key.
- Deleting the stored podcast from the Feed Update tool also deletes import settings and import history for that podcast.
