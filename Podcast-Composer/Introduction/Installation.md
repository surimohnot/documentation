This guide explains how to install Podcast Composer and confirm that it is ready to use.

## Requirements

Before installing, make sure your site has:

- WordPress 6.0 or newer.
- PHP 7.4 or newer.
- Administrator access to WordPress.
- A working WordPress site URL.
- Publicly accessible source podcast RSS feed URLs.

Podcast Composer reads podcast RSS feeds from other hosts. The source feed must be reachable by your WordPress server over HTTP or HTTPS.

## Install From a ZIP File

1. Log in to WordPress as an administrator.
2. Go to `Plugins > Add New`.
3. Click `Upload Plugin`.
4. Choose the Podcast Composer ZIP file.
5. Click `Install Now`.
6. Click `Activate Plugin`.

After activation, WordPress adds a `Podcast Composer` menu item in the admin sidebar.

## Install by Uploading the Plugin Folder

If you are installing manually:

1. Upload the `podcast-composer` folder to `wp-content/plugins/`.
2. Log in to WordPress as an administrator.
3. Go to `Plugins > Installed Plugins`.
4. Find `Podcast Composer`.
5. Click `Activate`.

## What Happens on Activation

On activation, the plugin:

- Registers private internal post types for projects and output feeds.
- Creates custom database tables for sources, indexed episodes, and output episode mappings.
- Registers custom feed endpoints for output feeds.
- Flushes rewrite rules so WordPress can recognize new feed URLs.

The custom tables are:

- `{prefix}_pc_sources`
- `{prefix}_pc_episodes`
- `{prefix}_pc_episode_output`

Your WordPress database prefix may be `wp_`, but many sites use a different prefix.

## Recommended WordPress Settings

Go to `Settings > Permalinks` and save your permalink settings once after activation.

This helps WordPress refresh feed rewrite rules. With pretty permalinks enabled, output feed URLs look like:

```
https://example.com/feed/my-podcast-feed
```

If pretty permalinks are disabled, WordPress can use:

```
https://example.com/?feed=my-podcast-feed
```

## First Access

After activation:

1. Go to `Podcast Composer > Manage Projects`.
2. If no projects exist, click `Create First Project`.
3. Continue with Getting Started.

## Uninstall Considerations

This codebase does not include a dedicated uninstall routine. Deactivating the plugin stops the admin screens and feed generation, but it does not automatically remove plugin database tables or saved project data.

If you need a full cleanup, back up your site first and have a developer remove the plugin tables and related private post type data manually.
