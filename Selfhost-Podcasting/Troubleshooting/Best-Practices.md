## Best Practices

These recommendations help keep podcast feeds stable, valid, and easy to maintain.

## Keep feed URLs stable

Choose the podcast slug carefully before submitting the show to directories. Changing the slug changes the native feed URL.

If you must move a feed, use a planned migration path and keep the old feed available long enough for directories and subscribers to update.

## Use reliable media URLs

Podcast apps need direct audio URLs. Avoid:

- Temporary signed URLs that expire quickly.
- Webpage URLs that contain a player.
- URLs blocked by hotlink protection.
- Redirect chains that fail in podcast apps.
- Hosts that do not support range requests.

## Complete required metadata before submission

Before submitting a feed, complete:

- Show title.
- Description.
- Artwork.
- Website.
- Language.
- Category.
- Author.
- At least one published episode.

Incomplete feeds are more likely to be rejected or displayed poorly.

## Use clean feed descriptions

Podcast apps vary in how they render HTML. Keep feed descriptions focused and simple.

Use the WordPress episode post content for richer website-only content such as embedded videos, forms, complex blocks, and extended transcripts.

## Configure storage early

If you plan to use S3-compatible storage, configure it before importing or publishing many episodes. Moving a large archive later is possible but takes more time and increases the chance of background job failures on limited hosting.

## Test after enabling analytics

After adding an analytics prefix:

1. Open the feed source.
2. Confirm enclosure URLs are prefixed.
3. Play an episode.
4. Confirm the media still plays.
5. Wait for the analytics provider to process data.

## Monitor background job errors

Check the **Error Log** after:

- Large imports.
- S3 uploads.
- Media replacements.
- Podcast deletion with bucket cleanup.
- Server migrations.

Clear old errors only after the underlying issue is fixed.

## Back up before migrations

Before migrating from another plugin:

- Back up the database.
- Back up media files.
- Record current source feed URLs.
- Test migration on staging if possible.
- Confirm whether feed takeover should be enabled.

## Treat private feed URLs like passwords

For Pro private podcasting:

- Do not post private URLs publicly.
- Revoke or regenerate exposed tokens.
- Use access expiry and usage limits when appropriate.
- Keep subscriber email records accurate.
- Test access after membership or product changes.

## Keep integrations intentional

Only enable integrations you actively use. Each integration adds a dependency:

- Analytics prefixes depend on the analytics provider.
- S3 URLs depend on the storage provider and bucket permissions.
- Podcast Player sync depends on Podcast Player.
- Private access integrations depend on the commerce or membership plugin.
