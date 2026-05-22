A **Podcast Feed URL** is a web address (typically an RSS feed) that contains all the details about your podcast episodes — including titles, descriptions, episode dates, and links to your audio files. It’s the primary way podcast apps (like Apple Podcasts, Spotify, and Google Podcasts) access and display your content. Without a valid podcast feed, your podcast won’t appear in podcast directories, and your podcast player plugin won’t be able to display your episodes on your website.

---

## What Does a Podcast Feed Do?

Here’s why the feed URL is important:

- It acts as the central source of truth for your podcast.
- Podcast directories “subscribe” to it and automatically pull in new episodes.
- Your podcast player plugin uses it to fetch and display episodes on your site.

Whenever you publish a new episode, it’s added to this feed — no need to manually update each platform.

---

## How to Find Your Podcast Feed URL

### If You Use a Podcast Hosting Platform

Most podcast hosting platforms (like Buzzsprout, Libsyn, Podbean, Anchor/Spotify for Podcasters, etc.) provide you with a feed URL when you create your podcast. It’s usually found in your account dashboard or podcast settings.

### Platform-specific Tips

- **Apple Podcasts**: Your Apple Podcasts page URL is not your RSS feed. Log in to your Apple Podcasts Connect account and go to your show details — your original RSS feed should be listed there. If not, check your hosting platform instead.
- **Spotify for Podcasters**: If you originally submitted your podcast to Spotify using an RSS feed, it should still be listed in your Spotify for Podcasters dashboard. If Spotify is hosting your podcast directly, the feed might not be publicly available.
- **Using Podcast Lookup Tools**: If you're unsure where your podcast is hosted or can't find your RSS feed, try using online tools such as:
  - [GetRSSFeed](https://getrssfeed.com/)
  - [Castos Feed Finder](https://castos.com/tools/find-podcast-rss-feed/)

These tools let you search by podcast name and often return the feed URL.

---

## What Does a Podcast Feed URL Look Like?

Here are a few examples of what a feed might look like:

- [https://yourdomain.com/podcast/feed/](https://yourdomain.com/podcast/feed/)
- [https://feeds.buzzsprout.com/123456.rss](https://feeds.buzzsprout.com/123456.rss)
- [https://anchor.fm/s/abcd1234/podcast/rss](https://anchor.fm/s/abcd1234/podcast/rss)

If your link opens a page full of code or XML text, that’s normal — it means you’ve found the correct feed URL.

---

## Validating Your Podcast Feed URL

If you paste the wrong URL into the Podcast Player settings, you may see an error like:

```
“RSS Error: StartTag: invalid element name”
```

This usually means the link is not a valid RSS feed. To check your feed before using it, try these validator tools:

- [Cast Feed Validator](https://www.castfeedvalidator.com/)
- [RSS Board Validator](https://www.rssboard.org/rss-validator/)

These tools confirm if your feed follows podcasting standards and will work correctly with apps and plugins.

---

## How to Use a Podcast Feed to Display the Podcast Player?

Once you have your podcast feed URL, you’re ready to display your podcast using the Podcast Player plugin.

Refer to the **Display Podcast** section of this documentation to know how to use podcast feed to show the podcast player. There, you’ll find all the instructions.

There are many ways to display your podcast. You can choose any of the available methods and use your podcast feed URL to display your podcast.

---

## Common Problems and How to Fix Them

### Problem 1: “I copied the URL from Apple Podcasts, but it doesn’t work.”

**Solution**: Apple Podcasts does not use the feed itself — it displays your content that’s already in a feed. You need to get the feed from your podcast host instead.

### Problem 2: “The feed URL opens a weird code page — is that wrong?”

**Solution**: That’s expected. RSS feeds are written in XML, which looks like code. If the URL returns that kind of page, you probably have the right feed.

### Problem 3: “I don’t know who hosts my podcast.”

**Solution**: Use [Castos’ tool](https://castos.com/tools/find-podcast-rss-feed/) or [GetRSSFeed](https://getrssfeed.com/) to search using your podcast name.

---

## Final Tips

- Always get your feed directly from your podcast host.
- Double-check that the feed is public and accessible.
- If your podcast is new, it might take a few hours for your feed to appear in directories or validate correctly.
- Once you have a working feed URL, you can paste it into the Podcast Player plugin to display your episodes on your website.
