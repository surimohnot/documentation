## Privacy, Security, and Stored Data

Selfhost Podcasting stores podcast data in your WordPress site. Optional integrations may send data to third parties only when you enable and configure them.

## WordPress data stored by the plugin

The free plugin stores:

- Podcast records in `sh_podcasting_pod`.
- Episode records in `sh_podcasting_epi` or supported migrated source post types.
- Podcast metadata with `_shp_` prefixed post meta.
- Episode metadata with `_shp_` prefixed post meta.
- Podcast episode associations.
- Feed slugs and GUIDs.
- Integration settings.
- Feed settings.
- Background job queue and error log data.

## Episode post content

On first episode creation, the feed description is copied into the WordPress post content. After that, the feed description and website post content are separate.

This means privacy-sensitive text added to a website post is not automatically added to the feed description, and feed description changes are not automatically copied back into the public post content.

## REST access

The plugin restricts public REST API access to Selfhost podcast and episode endpoints. Administrators can still access and edit the content.

Private podcasting adds further guards for private podcast content and private episode access.

## S3-compatible storage data

If S3 storage is enabled, the plugin stores encrypted storage configuration and bucket media metadata. The configured provider may process:

- Uploaded audio files.
- Object names and paths.
- File metadata.
- Request logs.
- Account and credential-related operational data.

If WordPress salts change, encrypted storage credentials may need to be re-entered.

## Analytics prefix data

If you enable an analytics prefix, listener requests for media are routed through the analytics provider. The provider may process request metadata such as:

- Requested URL.
- Timestamp.
- User agent.
- IP-derived network or location data.
- Referrer.
- Range headers.

Review the analytics provider's privacy policy before enabling the prefix.

## Private podcasting data (Pro)

When private podcasting is enabled, the plugin may store:

- Subscriber name.
- Subscriber email.
- Email hash.
- WordPress user ID when applicable.
- Token selector.
- Hashed token secret.
- Encrypted token secret.
- Token status.
- Expiration date.
- Feed and episode usage counters.
- Grant records.
- Last-used timestamps.

Private feed URLs should be treated like passwords. Regenerate or revoke tokens if they are exposed.

## Email notifications (Pro)

Private podcasting can send notifications containing private feed links or token status changes using the site's WordPress mail configuration.

Check your email deliverability and privacy policy before sending subscriber links.

## Recommended privacy policy disclosures

Depending on your enabled features, disclose:

- That the site publishes podcast RSS feeds.
- Where audio files are hosted.
- Whether third-party analytics prefixes are used.
- Which storage provider is used for podcast media.
- Whether private podcast subscriber data is stored.
- How subscribers can request access, export, correction, or deletion.

## Security recommendations

- Use HTTPS.
- Restrict WordPress administrator accounts.
- Keep WordPress, plugins, and PHP updated.
- Use storage credentials with the least permissions needed.
- Rotate S3 credentials if exposed.
- Rotate private podcast tokens if exposed.
- Avoid public directories for private tokenized feeds.
- Back up the database and uploads before major migrations.
