Install Selfhost Podcasting like any other WordPress plugin. After activation, a **Selfhost Podcasting** menu appears in the WordPress admin sidebar.

## Before installing

Check the basic requirements:

- WordPress 6.0 or newer.
- PHP 7.4 or newer.
- Administrator access to WordPress.
- HTTPS on the public site, especially before submitting feeds to podcast directories.
- Enough server storage and bandwidth if you plan to host audio in the WordPress Media Library.

For large audio files, confirm these PHP and server limits with your host:

- `upload_max_filesize`
- `post_max_size`
- `memory_limit`
- `max_execution_time`
- WordPress loopback requests and WP-Cron

These limits matter most when uploading media, importing many episodes, or moving media to S3-compatible storage.

## Install from WordPress.org

1. Log in to WordPress as an administrator.
2. Go to **Plugins > Add New**.
3. Search for **Selfhost Podcasting**.
4. Click **Install Now**.
5. Click **Activate**.
6. Open **Selfhost Podcasting** from the admin menu.

## Install from a ZIP file

1. Download the plugin ZIP file.
2. In WordPress admin, go to **Plugins > Add New**.
3. Click **Upload Plugin**.
4. Choose the ZIP file.
5. Click **Install Now**.
6. Click **Activate Plugin**.
7. Open **Selfhost Podcasting** from the admin menu.

## After activation

After activation, the plugin registers:

- The admin menu for managing podcasts.
- The podcast and episode post types.
- Feed routes for each podcast you create.
- Background job handling for media uploads, deletion tasks, and missing duration repair.
- Optional Pro routes if the Pro module is present.

If your feed URL returns a 404 after creating a podcast, go to **Settings > Permalinks** and click **Save Changes**. This refreshes WordPress rewrite rules.

## Recommended first configuration

1. Create your first podcast.
2. Fill in the required podcast information.
3. Add at least one episode with a valid audio file.
4. Open the feed preview and confirm the episode appears.
5. Open the XML feed URL and confirm the feed loads.
6. Submit the feed URL to podcast directories only after the feed has complete show artwork, language, category, author, and at least one published episode.

## Updating the plugin

Before updating a live podcast site:

- Back up the database and `wp-content/uploads`.
- Confirm any custom code that uses plugin filters or actions still works after staging tests.
- If you use S3 storage, keep a copy of current object storage credentials.
- If you use private podcasting, test one subscriber feed URL after the update.

Plugin updates do not require recreating podcasts or resubmitting unchanged feed URLs.
