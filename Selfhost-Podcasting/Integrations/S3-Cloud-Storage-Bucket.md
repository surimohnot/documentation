Selfhost Podcasting supports offloading your audio files to S3-compatible object storage (such as **Cloudflare R2**, **AWS S3**, or **Wasabi**). With this integration, the audio uploads and enclosure URLs are managed automatically, reducing load on your WordPress server.

## Why Use S3 / Object Storage?

- Offload storage and bandwidth from your WordPress server
- Benefit from scalability, redundancy, and cost-efficiency
- Leverage global storage networks or cheaper object storage
- Keep your site performance stable even with large audio archives

## Setup Guide (Step-by-Step)

Follow these steps to enable and configure S3 for a particular podcast.

### 1. Open S3 Settings

1. In your WordPress admin, go to **Selfhost Podcasting → Manage Podcast**
2. Choose the podcast you want to configure
3. Click the **Integrations** tab
4. Locate the **S3 Buckets** section

### 2. Enable Bucket Uploads

- Check the box labeled **“Use S3 Bucket to store your podcast”**
- Once checked, additional fields will appear

### 3. Select Your Provider

- Use the **Bucket Provider** dropdown to choose one of:
  - **Cloudflare R2**
  - **AWS S3**
  - **Wasabi**

Depending on your selection, relevant credential and configuration fields will show:

| Provider | Fields Required | Notes |
| --- | --- | --- |
| Cloudflare R2 | Account ID, Access Key, Secret Key, Bucket Name, API Endpoint, Public Domain for resources | R2 is fully S3-compatible and offers zero egress fees. |
| AWS S3 | Access Key, Secret Key, Bucket Name, Region | Standard AWS S3 |
| Wasabi | Access Key, Secret Key, Bucket Name, Region | Wasabi uses the same S3-compatible interface as AWS |

- *API Endpoint / Public Domain (Cloudflare only)*: For R2, you may need to enter the endpoint domain and optionally a public domain or custom domain to serve the files.
- *Region*: For AWS and Wasabi, select the correct region (e.g. `us-east-1`, `eu-west-1`, etc.)

### 4. Save / Update Integration

- After filling the required fields, click **Update Integration** or **Save Settings**
- The plugin will validate the credentials and connection
- If successful, all **newly uploaded** audio files for that podcast will be uploaded automatically to the S3 bucket
- The RSS feed enclosure URLs will be updated automatically to point to the S3 location instead of your local server

### 5. Migrating Existing Episodes (Pre-Integration)

If you already have episodes created before enabling the S3 integration:

- Go to the **Episodes** tab for that podcast
- For each episode, click the **Upload to Bucket** (or similar) button
- The plugin will upload that episode’s audio file to the configured bucket and update the enclosure URL
- Verify that the audio works from the new URL

## Testing & Verification

After setup, you should verify that the integration is working correctly. If any step fails (e.g. 403 Forbidden, audio not playing), double-check your credentials, bucket permissions, CORS settings, and endpoint formatting. You may contact us for any more help on this.
