## Feed URLs, Preview, and Feed Settings

Each podcast has an RSS feed URL and a browser preview URL. Podcast apps read the RSS feed. Humans can use the preview page to inspect the show.

## Feed URL formats

With pretty permalinks enabled:

`https://example.com/feed/podcast-slug`

Without pretty permalinks:

`https://example.com/?feed=podcast-slug`

For Pro private podcasts, the tokenized feed URL uses:

`https://example.com/shp-private-podcast/podcast-slug/token`

For migrated podcasts with feed takeover enabled, the public feed URL can remain the original source feed URL.

## Preview URL

The preview URL adds `shp_preview=1` to the feed URL.

Example:

`https://example.com/feed/podcast-slug?shp_preview=1`

The preview page is generated from the same podcast and episode data but is served as HTML. The XML feed remains unchanged for podcast apps.

## Feed Settings

Open a podcast and go to **Feed Settings**.

### Maximum number of episodes in the feed

Use this to control feed length.

- `0`: show all published episodes.
- Any positive number: show only that many newest published episodes.

This affects the RSS feed and the preview because both read the same prepared episode list.

### Show website link in preview

Controls whether the preview sidebar displays the podcast website link.

### Show feed link in preview

Controls whether the preview sidebar displays the RSS feed URL for copying.

### Show notes modal in preview

Controls whether visitors can open full episode show notes inside the preview page.

### Episode summary style

Choose whether episode cards show:

- **Excerpt**: a shortened summary.
- **Full Content**: the full feed description content.

This setting affects preview display, not the podcast RSS description.

### Apple Podcasts URL

Add the public Apple Podcasts show URL after the show is approved. The preview can show it as a listening option.

### Spotify URL

Add the public Spotify show URL after the show is approved. The preview can show it as a listening option.

## XML feed contents

The feed includes common RSS, Apple Podcasts, and Podcasting 2.0 metadata, including:

- Show title, link, description, language, copyright, author, owner, artwork, categories, GUID, funding, lock status, and verification tags.
- Episode title, link, summary, description, author, publish date, enclosure, duration, artwork, episode number, season, episode type, GUID, explicit flag, block flag, and transcript metadata.

## If the feed does not load

Try these checks:

- Save **Settings > Permalinks**.
- Confirm the podcast slug exists.
- Confirm the podcast has required show data.
- Confirm at least one episode is published.
- Disable caching or security rules that rewrite feed responses.
- Check for PHP warnings printed before XML output.
- Open the browser preview to see whether the show data can be rendered as HTML.
