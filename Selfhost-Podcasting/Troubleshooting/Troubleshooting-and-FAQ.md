## Troubleshooting and FAQ

Use this guide when a feed, episode, import, preview, storage integration, or private podcast does not work as expected.

## Feed URL returns 404

Try:

1. Go to **Settings > Permalinks**.
2. Click **Save Changes**.
3. Reopen the feed URL.

Also check:

- The podcast still exists.
- The podcast slug is not empty.
- Another plugin is not taking over the same feed slug.
- A migrated source-compatible URL is not being confused with the native Selfhost URL.

## Feed loads but has no episodes

Check:

- Episodes are published, not scheduled or draft.
- Episodes are attached to the correct podcast.
- **Maximum number of episodes in the feed** is not set incorrectly.
- Episode media URLs are valid.
- Migrated episodes were not detached from the podcast.

## Feed XML shows warnings or broken markup

Podcast feeds must be clean XML. PHP warnings, notices, or HTML before the XML can break directory validation.

Check:

- WordPress debug display settings.
- Theme or plugin output on feed requests.
- Custom feed hooks.
- Invalid characters in descriptions.
- Caching or optimization plugins that alter XML responses.

## Artwork is rejected by directories

Use artwork that is:

- Square.
- JPG or PNG.
- At least 1400 x 1400 pixels.
- No larger than the directory's maximum.
- Publicly accessible over HTTPS.

Avoid transparent PNGs if a directory rejects them.

## Episode audio does not play

Check:

- The URL points directly to an audio file.
- The server returns the correct MIME type.
- The file is publicly accessible unless it is a private podcast proxy URL.
- The URL does not expire quickly.
- The URL supports range requests for better podcast app playback.
- Analytics prefixes or redirects are correctly formatted.

## Duration is missing

The plugin attempts to detect duration from media metadata and can queue a background repair task. Duration may remain missing if:

- The remote host blocks metadata requests.
- The file does not expose readable duration data.
- The background queue is blocked.
- The source URL is not a direct audio file.

Check the podcast **Error Log** for duration backfill errors.

## Import feed cannot be fetched

Check:

- The source URL returns valid RSS XML.
- The feed is public.
- The host is not blocking your WordPress server.
- The feed contains `<item>` entries with audio enclosures.
- Server outbound HTTP requests are allowed.

## S3 upload fails

Check:

- Provider selection.
- Access key and secret key.
- Bucket name.
- Region.
- Endpoint.
- Public resource domain.
- Bucket permissions.
- Whether the source media URL can be downloaded by the server.

If repeated failures suspended uploads, fix the storage issue and resume jobs.

## Podcast Player does not appear

Check:

- Podcast Player is installed and active.
- The podcast is public.
- Automatic insertion is enabled before creating new episode posts.
- The selected insertion method is supported by the installed Podcast Player version.
- Existing posts may need manual player insertion.

## Analytics are not counted

Check:

- The analytics prefix is saved.
- The feed enclosure URLs start with the prefix.
- A podcast app has requested the episode after the prefix was added.
- The provider's reporting delay has passed.
- The provider prefix redirects correctly to the original media URL.

## Private feed unauthorized (Pro)

Check:

- The podcast is private.
- The URL includes the correct token.
- The token is active.
- The token has not expired.
- Usage limits have not been exceeded.
- The token belongs to the requested podcast.

## Private audio does not play (Pro)

Check:

- The private audio proxy URL includes a valid signature.
- The token is valid for episode access.
- The episode belongs to the requested podcast.
- The source media URL exists.
- Local files are readable by PHP.
- Remote files can be redirected to safely.

## Frequently asked questions

**Can I create more than one podcast?**

Yes. Each podcast has its own feed URL, settings, integrations, and episode list.

**Can I use WordPress Media Library audio?**

Yes. You can select or paste a Media Library audio URL.

**Can I use external audio hosting?**

Yes, as long as the URL points directly to a playable audio file.

**Can I move audio to Cloudflare R2 or S3 later?**

Yes. Configure S3-compatible storage and upload or re-upload episode media through the plugin workflow.

**Can I import from another RSS feed?**

Yes. Use **Import Episodes** from the podcast episode management screen.

**Can I migrate from PowerPress or Seriously Simple Podcasting?**

Yes, when those source plugins or their data are detected.

**Will changing post content update the feed description?**

No. After the first episode creation, post content and feed description are independent.

**Should private feeds be submitted to Apple or Spotify?**

Usually no. Private feeds are intended for authorized subscribers. Public directories generally expect public feeds.
