## Podcast Episode Custom Posts

Selfhost Podcasting stores new manually created episodes as WordPress posts in a dedicated custom post type named `sh_podcasting_epi`.

This gives every episode a WordPress post URL while keeping podcast feed metadata separate from normal blog posts.

## How episode posts are created

When you create an episode in Selfhost Podcasting:

- The episode title becomes the WordPress post title.
- The episode description is copied into the post content only when the episode is first created.
- The feed metadata is stored separately in post meta.
- The post is assigned to the podcast's Selfhost category term when possible.
- Episode artwork is set as the featured image when an attachment ID is available.

## Feed description and post content are separate

The plugin intentionally separates:

- **Episode description**: used in the podcast RSS feed.
- **WordPress post content**: used on your website.

On first creation, the same text is copied into both places. After that, editing one does not automatically rewrite the other.

This lets you keep podcast feed descriptions clean while making richer website posts.

For example, the website post can contain:

- Full transcripts.
- YouTube embeds.
- Newsletter signup forms.
- Product links.
- Sponsor blocks.
- Related posts.
- Custom block layouts.

These may not be suitable for RSS feed descriptions or podcast apps.

## Custom post type details

The plugin registers:

- Post type: `sh_podcasting_epi`
- Taxonomy: `sh_podcasting_cats`
- Supported post features: title, editor, thumbnail, excerpt
- REST visibility: enabled for administrators, with additional privacy safeguards
- Tags: WordPress `post_tag` support is enabled

The plugin also registers a hidden podcast post type:

- Post type: `sh_podcasting_pod`

This stores show-level podcast records and is managed through the Selfhost Podcasting admin screens.

## Selfhost categories

When an episode is created, the plugin creates or finds a term in `sh_podcasting_cats` using the podcast slug and assigns the episode to it.

This makes it easier to:

- Group episodes by podcast.
- Build custom templates.
- Query episodes from one show.
- Display archive pages for one podcast.

## Migrated episodes can use other post types

When the plugin migrates content from another podcast plugin, it may keep an existing source post type instead of converting the post into `sh_podcasting_epi`. This is intentional.

For example:

- A PowerPress migration can attach Selfhost podcast metadata to existing source posts when there is no conflict.
- A Seriously Simple Podcasting migration can copy source episodes into Selfhost-managed episode records.

When editing an existing migrated episode, the plugin keeps the current post type if it still exists.

## REST and privacy behavior

Selfhost episode data is visible in the WordPress editor for administrators. The plugin restricts public REST access to Selfhost podcast and episode endpoints, and Pro private podcasting adds additional guards for private episode content.

If a podcast is private, do not rely only on hiding links. Use the private podcasting features so feed and audio access are token-protected.
