## S3-Compatible Cloud Storage

Selfhost Podcasting can upload episode audio to S3-compatible object storage and use the stored object URL in the podcast feed.

Supported provider choices in the admin UI include:

- Cloudflare R2.
- Amazon S3.
- Wasabi.

The underlying S3 handler also normalizes endpoint-style settings for compatible providers.

## Why use object storage

Object storage is useful when:

- Your WordPress hosting plan has limited disk space.
- Podcast audio creates too much bandwidth for your web server.
- You want media files served from a storage provider or CDN-style domain.
- You manage a large archive and want storage separated from WordPress.

## Open the settings

1. Go to **Selfhost Podcasting**.
2. Open a podcast.
3. Go to **Connect Services**.
4. Open **S3 Buckets**.
5. Enable **Use S3 Bucket to store your podcast**.

## Common fields

**Provider**

Choose Cloudflare R2, Amazon S3, or Wasabi.

**Access Key**

The access key or key ID from your storage provider.

**Secret Key**

The secret access key from your storage provider.

**Bucket Name**

The exact bucket name.

**Region**

Required for Amazon S3 and Wasabi. Cloudflare R2 uses `auto` internally when no region is needed.

**API Endpoint**

Required or auto-generated depending on provider. For R2, this is usually based on the account ID.

**Public Domain for Resources**

Used for Cloudflare R2 public delivery. Enter the public/custom domain that should serve uploaded audio files.

**Delete audio after S3 upload**

When enabled, local WordPress media can be deleted after the object storage upload completes. Use this only when you are confident the bucket URL is public and stable.

## Cloudflare R2 notes

R2 needs:

- Account ID.
- Access key.
- Secret key.
- Bucket name.
- Endpoint.
- Public resource domain.

Make sure the public domain can serve the uploaded audio files. The S3 API endpoint is not always the same as the public delivery URL.

## Amazon S3 notes

S3 needs:

- Access key.
- Secret key.
- Bucket name.
- Region.

Bucket permissions, object ACL behavior, and public access settings must allow the final audio URLs to be served to podcast apps.

## Wasabi notes

Wasabi needs:

- Access key.
- Secret key.
- Bucket name.
- Region.

Use the correct Wasabi region endpoint for your bucket.

## How uploads happen

When S3 storage is enabled:

- New or changed episode media can be queued for upload.
- Existing episodes can be uploaded through the episode media workflow.
- Uploaded object information is stored on the episode as bucket media data.
- The feed uses the bucket URL when bucket media data exists.
- If an episode is deleted, the plugin can queue a delete task for the bucket object.

Uploads run through the plugin background job system. They may not finish instantly on large files or slow hosts.

## Credential storage

The plugin encrypts S3 credential configuration before saving it. Encryption uses WordPress keys and salts. If WordPress secret keys and salts are changed later, the plugin may be unable to decrypt existing S3 credentials and will require you to re-enter the storage configuration.

## Background job safeguards

The upload queue retries failed items. If upload failures become terminal, the plugin can trip an upload guard for that podcast and suspend additional upload jobs until the issue is corrected and jobs are resumed.

Check the podcast **Error Log** for exact failure messages.

## Testing

After saving storage settings:

1. Add or edit a test episode with a small audio file.
2. Wait for the background upload to finish.
3. Open the episode in the feed and confirm the enclosure URL points to the bucket/public domain.
4. Open the audio URL in a private browser window.
5. Play the episode in a podcast app or feed validator.

## Troubleshooting

**Bucket not accessible**

Check bucket name, region, endpoint, access key, secret key, and provider permissions.

**Uploaded audio returns 403**

The object or bucket is not publicly readable through the URL used in the feed.

**The feed still uses the local URL**

The background upload may not have completed, failed, or was not queued because S3 storage was disabled at the time.

**Uploads stop after errors**

Open the **Error Log**, fix the storage issue, then use the resume jobs action if available.

**Credentials stopped working after a server move**

If WordPress salts changed, re-enter the S3 configuration.
