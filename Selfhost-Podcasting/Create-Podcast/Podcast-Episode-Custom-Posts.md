Each time you create a new podcast episode using the **Selfhost Podcasting** plugin, a corresponding **WordPress custom post** is automatically created.
This helps you manage and display your episodes directly on your website while keeping them organized and distinct from your regular blog posts.

---

## How It Works

- When you **create a new podcast episode**, the plugin automatically generates a **custom post type entry** for that episode.
- The **episode title** becomes the post title.
- The **episode description** you entered during creation is copied as the post content for the first time only.

This means you instantly have a WordPress post that can be:

- Displayed on your site’s front end
- Shared on social media
- Enhanced with visuals, embeds, or additional content beyond what’s in your podcast feed

---

## One-Time Sync Behavior

It’s important to understand how synchronization works between the **podcast feed** and the **custom post**.

- When you first create an episode, its description is **copied** into the new WordPress post.
- After that, the two are **independent** — editing the description in your feed or in the WordPress post will **not** update the other.

This design choice differs from plugins such as *Seriously Simple Podcasting* or *Blubrry PowerPress*, which maintain live synchronization between feed data and posts.

We intentionally keep them separate to give you **more creative flexibility**.

For example, you can add:

- Embedded YouTube videos or reels
- Forms or calls-to-action
- Related links, transcripts, or extended notes
- Exclusive content meant for website visitors

These extras often don’t belong in your podcast feed description (or are not compatible with podcast feed formatting), so maintaining separation keeps your podcast feed clean and compliant.

---

## Custom Post Type and Structure

All podcast episode posts are stored in a **dedicated custom post type** created by the plugin.
This keeps them separate from your standard blog posts and makes them easier to manage.

Key points:

- The plugin creates a **custom taxonomy term (Selfhost Category)** for each podcast.
- Every episode post is automatically assigned to that category.
- This makes it simple to **filter or display** all episodes belonging to a single podcast.

You can query or display these posts on your site using WordPress loops, shortcodes, or block-based templates just like any other post type.

---

## Benefits of Custom Posts for Episodes

- **Better organization**: Episodes are neatly grouped under their own post type and category.
- **More flexibility**: Add custom HTML, media embeds, or integrations unique to your website.
- **Improved visibility**: Each episode gets its own URL, improving discoverability and SEO.
- **Freedom from feed limitations**: Feed descriptions remain clean and compatible with podcast apps, while your site version can include richer formatting.

---

## Example Workflow

1. Create a new podcast using the plugin.
2. Add a new episode under that podcast.
3. The plugin automatically creates a WordPress custom post for that episode.
4. Go to the post editor to customize it:
  - Add images, transcripts, or YouTube videos.
  - Include newsletter signup forms or links.
  - Format it for readers instead of podcast listeners.
