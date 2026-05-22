## Third-Party Podcast Analytics

Selfhost Podcasting supports analytics services that use a redirect prefix. The plugin stores the prefix and applies it to episode audio URLs when feed output is generated.

Common prefix-based providers include:

- Podtrac.
- Blubrry.
- OP3.

## How an analytics prefix works

Without a prefix, an episode enclosure points directly to your media file:

`https://media.example.com/episode-1.mp3`

With an analytics prefix, the feed points to the analytics provider first:

`https://prefix.example/redirect/https://media.example.com/episode-1.mp3`

The provider logs the request and redirects the listener to the real file.

Exact prefix formatting depends on the provider. Always copy the prefix from the provider's own setup instructions.

## Configure an analytics prefix

1. Sign up with the analytics provider.
2. Copy the redirect prefix URL they provide.
3. Go to **Selfhost Podcasting**.
4. Open the podcast.
5. Go to **Connect Services**.
6. Open **Third Party Analytics**.
7. Paste the prefix in **Prefix URL for Analytics**.
8. Save the integration.

## Verify the prefix

1. Open the podcast feed URL.
2. View the feed source.
3. Find an episode `<enclosure>` tag.
4. Confirm the `url` starts with the analytics prefix.
5. Play or download an episode.
6. Check the analytics provider dashboard after its normal reporting delay.

Some services take 24 to 48 hours to show processed analytics.

## Important notes

- The prefix should be added before public directory submission when possible.
- If you add analytics later, directories and apps may take time to refresh cached enclosure URLs.
- Do not combine multiple analytics prefixes unless the providers explicitly support chaining.
- Test at least one episode in a podcast app after adding a prefix.
- If an analytics provider is down or misconfigured, media playback can fail even when your original audio host is working.

## Privacy impact

When you use an analytics prefix, listener requests pass through the analytics provider. Depending on the provider, it may process request metadata such as IP-derived location, user agent, requested URL, timestamp, referrer, and range headers.

Your privacy policy should identify the analytics provider if you enable one.

## Troubleshooting

**Enclosure URLs do not change**

Confirm the prefix was saved in the podcast's **Third Party Analytics** integration, then clear any feed/page cache.

**Playback breaks after adding the prefix**

Check the exact prefix format. Some providers require a trailing slash or a specific path such as `redirect.mp3`.

**Analytics do not appear**

Confirm the feed contains prefixed URLs, play an episode through a podcast app, and wait for the provider's reporting window.
