## Quick Start: Publish Your First Feed

This guide takes you from a blank installation to a working podcast feed.

## 1. Create a podcast

1. Go to **WordPress admin > Selfhost Podcasting**.
2. Click **Create New Podcast**.
3. Enter the podcast name.
4. Enter a slug or leave it blank to generate one from the name.
5. Create the podcast.

The slug becomes part of the feed URL. For example, a slug of `weekly-update` usually creates:

`https://example.com/feed/weekly-update`

Choose the slug carefully before submitting the feed to directories.

## 2. Complete required show information

Open the podcast and go to **Podcast Information**.

Fill in the required fields:

- Podcast name.
- Podcast description.
- Podcast cover art.
- Podcast website.
- Language.
- Apple Podcasts categories.
- Podcast author.

Save the podcast information.

## 3. Add the first episode

Go to **Manage Episodes** and create a new episode.

At minimum, add:

- Audio or media URL.
- Episode title.
- Episode description.
- Episode publish date.

The audio URL must point directly to an audio file, not to a webpage containing an audio player.

## 4. Check the feed preview

Return to the podcast overview and open the preview URL. The preview page should show:

- Podcast artwork.
- Podcast title and description.
- Episode list.
- Audio player controls for each episode.
- Feed URL, if enabled in feed settings.

The preview is for humans. Podcast apps read the XML feed.

## 5. Check the XML feed

Open the feed URL in a browser. You should see RSS XML or a browser-rendered feed stylesheet.

Look for:

- A `<channel>` section with show details.
- At least one `<item>` for the episode.
- An `<enclosure>` tag with a valid audio URL.
- A publish date.
- Podcast artwork.

If the feed URL returns a 404, save WordPress permalinks again from **Settings > Permalinks**.

## 6. Submit the feed

After the feed is complete, submit it to your chosen podcast directories. Common destinations include:

- Apple Podcasts.
- Spotify for Podcasters.
- YouTube Music.
- Amazon Music.
- Pocket Casts.
- Podcast Index.

Each directory has its own review process. Keep the feed URL stable after submission.

## Recommended next steps

- Configure **Feed Settings** to decide how many episodes appear and what the preview shows.
- Configure **Podcast Player** if you want automatic website playback.
- Configure an **analytics prefix** if you use external podcast analytics.
- Configure **S3 storage** before adding many episodes if WordPress storage or bandwidth is limited.
