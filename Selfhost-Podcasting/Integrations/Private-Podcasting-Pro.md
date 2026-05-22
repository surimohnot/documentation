## Private Podcasting (Pro)

Private podcasting is available when the Pro module is present. It lets you protect a podcast feed with subscriber-specific tokens instead of publishing one public feed URL for everyone.

## What private podcasting adds

The Pro module adds:

- Public or private podcast status.
- Tokenized private feed URLs.
- Manual subscriber token generation.
- Guest subscriber support.
- WordPress user subscriber support.
- Token revoke, regenerate, reactivate, delete, and bulk rotation actions.
- Feed access limits.
- Episode/audio access limits.
- Private audio proxy endpoint.
- Private feed shortcodes.
- Optional e-commerce and membership access integrations.

## Enable private status

1. Open the podcast in **Selfhost Podcasting**.
2. Go to the private podcasting or manager section.
3. Set **Privacy Status** to **Private**.
4. Configure access limits if needed.
5. Save options.

When a podcast is private, the admin-friendly private route is:

`https://example.com/shp-private-podcast/podcast-slug`

Subscriber URLs include a token:

`https://example.com/shp-private-podcast/podcast-slug/selector.secret`

## Access settings

**Access Expiry (days)**

Set how many days a generated token remains valid. Use `0` for no expiry.

**Feed Use Limit**

Maximum allowed feed fetches per token. Use `0` for unlimited.

**Episode Use Limit**

Maximum allowed episode/audio fetches per token. Use `0` for unlimited.

**Active Subscribers**

Shows the current number of active, non-revoked tokens for the feed.

## Manual subscriber access

Admins can generate access for:

- A WordPress user.
- A guest subscriber by name and email.

When a token is generated, the plugin can send a notification with the private feed URL.

## Token actions

Available token actions include:

- **Revoke**: disables the current token.
- **Regenerate**: creates a new secret for the subscriber.
- **Reactivate**: reactivates a revoked or expired token when allowed.
- **Delete**: removes the token row.
- **Rotate all active tokens**: regenerates active tokens for a feed.

Use token rotation if private feed URLs were exposed or shared too widely.

## Private audio proxy

The Pro module registers:

`https://example.com/shp-audio-proxy/`

The proxy verifies signed requests, validates the token, checks episode ownership, supports local file range streaming, and redirects to remote media when appropriate.

This helps protect episode audio URLs for private feeds.

## Shortcodes

### Single private feed

Use:

`[shp_private_feed feed_id="123"]`

If `feed_id` is omitted, the shortcode uses the first private podcast it can resolve.

Logged-in users can view their private feed URL, open the browser preview, use app links, scan a QR code, and regenerate their own feed URL once every 24 hours.

### All private subscriptions

Use:

`[shp_private_subscriptions]`

This lists private subscriptions for the logged-in user.

## Important limitations

- Public podcast directories generally should not receive private tokenized feeds.
- Spotify does not support direct private feed deep-links in the shortcode UI. Users should copy the feed URL manually where supported.
- A private feed URL should be treated like a password.
- If a token is compromised, revoke or regenerate it.

## Troubleshooting

**Private feed says unauthorized**

Check that the token belongs to the correct podcast, is active, has not expired, and has not exceeded usage limits.

**Audio does not play**

Check the audio proxy URL, token validity, episode association, source media URL, and whether the server supports range requests for local files.

**A logged-in user cannot see a feed**

Confirm the podcast is private and the shortcode uses the correct `feed_id`.

**Regeneration is blocked**

Front-end regeneration is rate-limited to once every 24 hours per user and feed.
