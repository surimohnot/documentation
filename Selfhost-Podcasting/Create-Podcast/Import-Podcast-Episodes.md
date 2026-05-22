The Import Episodes feature lets you quickly copy episodes from an existing podcast RSS feed into a new or existing podcast in your site. Below is a comprehensive guide covering steps, what gets imported, tips, and troubleshooting.

---

## Quick steps

1. Open the **Selfhost Podcasting** menu in your WordPress dashboard and go to the podcast you want to add episodes to.
2. Click the **Import Episodes** button.
3. Paste the RSS feed URL of the podcast you want to import from and click **Show Episodes List**.
4. The plugin will fetch and display available episodes from that feed. Use the checkboxes to select specific episodes or click the checkbox in the header to select all.
5. Click the **Import Episodes** button to start importing the selected episodes.
6. When the import finishes, go to the podcast’s **Episodes** tab to view and edit any imported episode.

---

## What the importer brings across

When the plugin imports an episode it will attempt to map the common RSS fields into the episode record:

- Episode title
- Episode description
- Publication date
- Audio file enclosure URL (the original audio URL from the feed)
- Episode image if present in the item or the feed-level image
- Episode author information if present
- Duration if present in the feed

Note: The imported episode will reference the original audio URL by default. If you want the audio file hosted in your WordPress Media Library, you will need to download the audio and upload it, then update the episode’s audio URL in the editor.

## Import behavior and hosting options

- By default the importer keeps the source audio URL as the episode’s enclosure. This preserves original hosting and avoids transferring large files.
- If you want local hosting:
  - Download the audio files from the original host.
  - Upload audio into WordPress Media Library.
  - Edit the imported episode and replace the audio URL with the Media Library URL.
- Hosting audio locally increases disk and bandwidth usage on your server. Check your hosting quotas before migrating large shows.

## Progress, large imports, and performance tips

- For a small number of episodes the import completes quickly. For large shows (hundreds of episodes) the process may take longer or hit server limits. If you see timeouts:
  - Import in smaller batches by selecting fewer episodes at a time.
  - Check your PHP settings (max_execution_time and memory_limit) or run imports during low-traffic periods.
  - If your host limits long-running requests, import 20 to 50 episodes per batch.
