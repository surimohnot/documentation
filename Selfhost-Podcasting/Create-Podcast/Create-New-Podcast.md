## Create a New Podcast

A podcast is the show-level record. It holds the feed slug, show metadata, settings, integrations, and the list of episodes that belong to the feed.

## Create the show

1. Go to **WordPress admin > Selfhost Podcasting**.
2. Click **Create New Podcast**.
3. Enter the podcast name.
4. Enter a custom slug if you want to control the feed URL. If you leave it blank, the plugin creates one from the podcast name.
5. Create the podcast.

The plugin stores the podcast as a `sh_podcasting_pod` post and saves the feed slug as podcast metadata.

## Understand the feed URL

The podcast slug becomes the feed key. With pretty permalinks enabled, the feed URL is usually:

`https://example.com/feed/podcast-slug`

Without pretty permalinks, WordPress uses:

`https://example.com/?feed=podcast-slug`

If the podcast was migrated from another supported plugin and feed takeover is enabled, the public feed URL may be the original source plugin feed URL instead. The native Selfhost URL still exists, but the migrated source-compatible URL is used for continuity.

## Fill in podcast information

After creating the podcast, open it and go to **Podcast Information**. The form is grouped by purpose:

- **Required Podcast Information**: required for a complete and valid podcast feed.
- **Recommended Information**: useful ownership, copyright, and funding details.
- **Podcast Management**: advanced Apple Podcasts and Podcasting 2.0 controls.

Save changes with **Update Podcast**.

## Required podcast fields

**Podcast Name**

The public title of the show. This appears in the RSS `<title>` tag and in podcast directories.

**Podcast Description**

The show description. The feed uses it in the RSS description and summary output. Keep it clear, useful, and free from layout-specific website content.

**Podcast Cover Art**

The show image. Use a square JPG or PNG. A practical target is 3000 x 3000 pixels, while 1400 x 1400 pixels is the common minimum expected by major directories.

**Podcast Website**

The main website associated with the podcast. This appears in the feed `<link>` tag and may appear in the preview sidebar.

**Language**

The primary language of the show. The plugin stores Apple-compatible language codes.

**Apple Podcast Categories**

One or more Apple Podcasts categories. These are output as `itunes:category` tags.

**Podcast Author**

The public author, host, company, or organization name. This is output as `itunes:author`.

## Recommended podcast fields

**Episodic or Serial**

Choose **Episodic** for standalone episodes. Choose **Serial** when episodes are intended to be consumed in order, often across seasons.

**Copyright**

The copyright statement for the show.

**Podcast Owner Name and Email**

Owner details can be used by Apple Podcasts for contact and verification. The owner email is also used as the owner attribute for the Podcasting 2.0 locked tag when podcast locking is enabled.

**Podcast Funding URL and Label**

Adds Podcasting 2.0 funding information to the feed. Use this for listener support, memberships, donations, or sponsorship pages.

## Advanced podcast management fields

**Is Podcast Explicit?**

Marks the show as explicit. Episode-level explicit flags can still be set separately.

**Should Remove Podcast From Apple Podcasts?**

Outputs `itunes:block` for the show. Use only when you intentionally want Apple Podcasts to stop showing the podcast.

**Is Podcast Completed?**

Outputs `itunes:complete`, which tells supported apps that the show is complete and no new episodes are expected.

**Is Podcast Locked?**

Outputs the Podcasting 2.0 `podcast:locked` tag. This can signal that the feed should not be imported elsewhere without owner control.

**iTunes New Feed URL**

Outputs `itunes:new-feed-url`. Use this only when permanently moving subscribers to another feed.

**Verify Apple Podcast Ownership**

Outputs Apple verification metadata in the feed. Use the token supplied by Apple when claiming or verifying the show.

## Before submitting a new podcast

Before sending the feed to directories, confirm:

- The feed URL opens.
- The browser preview looks correct.
- The show artwork is square and large enough.
- Required fields are complete.
- At least one published episode exists.
- Each episode has a valid enclosure URL, file length, type, and publish date.
- The site is served over HTTPS.
