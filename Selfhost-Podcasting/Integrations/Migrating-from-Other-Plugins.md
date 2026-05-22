## Migrating from Other Podcast Plugins

Selfhost Podcasting includes migration tooling for supported WordPress podcast plugins. This is separate from the RSS episode importer.

Supported migration providers in the plugin code are:

- PowerPress.
- Seriously Simple Podcasting.

## What migration does

The migration tools detect source feeds, create corresponding Selfhost podcasts, map show metadata, attach or copy episodes, and store source metadata so the relationship remains traceable.

Depending on the source plugin and feed structure, migration can:

- Create a Selfhost podcast for a source feed.
- Import or link source episodes.
- Preserve source feed slugs.
- Track source plugin, source post ID, source feed slug, and migration batch ID.
- Detect conflicts where one source post appears in multiple feeds with different podcast-critical metadata.
- Enable feed takeover when it is safe.

## PowerPress migration behavior

PowerPress migration can detect:

- The default `podcast` feed.
- Custom feeds.
- Post type podcasting feeds.

Unsupported or special PowerPress modes can be detected and reported, including:

- Category podcasting.
- Taxonomy podcasting.
- Legacy PodPress processing.

When one post appears in more than one PowerPress feed, the migration analyzes whether the episode metadata is identical or conflicting.

Conflict handling options include:

- **Skip conflicts**: do not import conflicting shared posts into the conflicting feed.
- **Duplicate conflicts**: create a separate episode copy for conflicting metadata.

Premium PowerPress feeds are not taken over because serving them publicly could expose protected content.

## Seriously Simple Podcasting migration behavior

Seriously Simple Podcasting migration detects series feeds and creates Selfhost podcasts from them.

SSP migration generally copies each source episode into a Selfhost-managed episode for the target podcast. Shared source posts are not treated the same way as PowerPress conflicts because SSP series migration copies episodes per target podcast.

Feed takeover can be blocked if the source SSP feed uses private, password-protected, redirected, or passthrough behavior that Selfhost should not replace without equivalent access behavior.

## Feed takeover

Feed takeover means Selfhost Podcasting serves the migrated Selfhost feed at the original source feed URL.

This helps preserve:

- Existing directory submissions.
- Existing subscriber feed URLs.
- Podcast Player source URLs.
- External links to the old feed.

Takeover is only enabled when the plugin considers it safe.

Do not enable takeover if:

- The source feed is premium or protected.
- Another Selfhost podcast is already controlling that source feed URL.
- You still need the source plugin to serve that feed.
- You do not understand how the original feed URL is being used.

## After migration

After migration:

1. Open the new Selfhost podcast.
2. Review podcast information.
3. Review imported episodes.
4. Check episode media URLs.
5. Open the native Selfhost feed URL.
6. Open the source-compatible URL if takeover is enabled.
7. Check the preview page.
8. Confirm directories and players are reading the expected URL.

## Removing a migrated Selfhost podcast

The migration manager includes a remove action for migrated Selfhost podcasts. This removes the Selfhost migration result without intentionally deleting the original source plugin data.

Back up before removing migrated podcasts, especially if you edited migrated episode records after migration.

## Migration vs RSS import

Use migration when:

- The source podcast is in the same WordPress site.
- You use PowerPress or Seriously Simple Podcasting.
- You want source-aware feed URL continuity.

Use RSS import when:

- The source podcast is on another site.
- You only have a feed URL.
- You do not need source plugin metadata or feed takeover.
