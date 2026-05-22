# Installation Guide

Setting up Easy TubeCasting is straightforward and follows the standard WordPress plugin installation process.

## Prerequisites

- **WordPress Version:** 6.0 or higher.
- **PHP Version:** 7.4 or higher.
- **Editing Experience:** The supported publishing workflow uses the WordPress block editor.

## Option 1: Installation via WordPress Dashboard (Recommended)

1. Log in to your WordPress Admin area.
2. Navigate to **Plugins > Add New**.
3. Click the **Upload Plugin** button at the top.
4. Choose the `easy-tubecasting.zip` file from your computer.
5. Click **Install Now**.
6. Once the installation is complete, click **Activate Plugin**.

## Option 2: Manual Installation via FTP

1. Decompress the `easy-tubecasting.zip` file on your computer.
2. Connect to your web server using an FTP client (like FileZilla).
3. Upload the `easy-tubecasting` folder to the `/wp-content/plugins/` directory of your WordPress installation.
4. Go to **Plugins > Installed Plugins** in your WordPress dashboard.
5. Locate **Easy TubeCasting** in the list and click **Activate**.

## Post-Activation Steps

After activation, you will see a new menu item labeled **Easy TubeCasting** in your WordPress sidebar.

1. Go to **Easy TubeCasting > Settings**.
2. Add and validate a YouTube Data API v3 key if you want to display playlists, channels, usernames, or handles.
3. Open a page or post in the block editor.
4. Add the **Easy TubeCasting** block.
5. Paste a YouTube video, playlist, channel, username, or handle URL.
6. Adjust **Videos Per Batch**, **Theme Mode**, **Accent Color**, and **Display Style** as needed.

You can display a single video or comma-separated video URLs without saving an API key. Collection imports and sync require a key.
