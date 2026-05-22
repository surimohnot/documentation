# Obtaining a YouTube Data API Key

To enable advanced features like Playlists, Channels, and Auto-Sync, you need a YouTube Data API v3 key from the Google Cloud Console.

## Step-by-Step Guide

### 1. Create a Google Cloud Project

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Click the project dropdown at the top and select **New Project**.
3. Give your project a name (e.g., "My Website YouTube Feed") and click **Create**.

### 2. Enable YouTube Data API v3

1. With your new project selected, go to **APIs & Services > Library**.
2. Search for "YouTube Data API v3".
3. Click on the result and then click **Enable**.

### 3. Create Credentials (API Key)

1. Go to **APIs & Services > Credentials**.
2. Click **+ Create Credentials** at the top and select **API key**.
3. Your new API key will be displayed. **Copy this key.**

### 4. (Recommended) Restrict Your API Key

To prevent others from using your key:

1. Click the "Edit" icon next to your newly created API key.
2. Under **API restrictions**, select "Restrict key".
3. In the dropdown, check **YouTube Data API v3**.
4. Click **Save**.

Be careful with application restrictions. Easy TubeCasting validates and uses the key from your WordPress server, so overly strict referrer or IP restrictions can cause validation or sync requests to fail. If a restricted key fails in the plugin, loosen the application restriction and keep the API restriction limited to YouTube Data API v3.

## Adding the Key to Easy TubeCasting

1. In your WordPress Admin, go to **Easy TubeCasting > Settings**.
2. Paste your API key into the **YouTube API Key** field.
3. Click **Verify & Save Key**.
4. If successful, the key is validated against YouTube, saved in plugin options, masked in the UI, and marked with the last validation time in UTC.

## Managing a Saved Key

After a key is saved, the settings page provides:

- **Validate Current Key:** Re-checks the saved key against YouTube.
- **Replace Key:** Unlocks the field so you can save a new key.
- **Delete Key:** Removes the saved key and related key metadata from plugin options.

The setup checklist is shown when no key is saved. Checklist progress is stored for the current site and clears after a key is successfully saved.

> [!IMPORTANT] Google provides a generous free tier for the YouTube Data API. For most small to medium websites, you will likely never exceed the free daily quota.
