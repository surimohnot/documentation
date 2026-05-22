## Developer Hooks and Extension Points

Selfhost Podcasting exposes WordPress filters and actions for developers who need to adjust forms, feed output, migration behavior, storage behavior, background processing, or private podcasting.

Use these hooks in a small custom plugin or theme functionality plugin. Avoid editing Selfhost Podcasting plugin files directly.

## Admin and form hooks

**`sh_podcasting_form_fields`**

Filters podcast information fields.

**`sh_podcasting_epi_form_fields`**

Filters episode information fields.

**`sh_podcasting_settings_form_fields`**

Filters feed settings fields.

**`sh_podcasting_integrations_form_fields`**

Filters integration fields.

**`sh_podcasting_manage_form_fields`**

Filters management fields. The Pro module uses this to add private podcasting settings.

**`sh_podcasting_settings_field_markup`**

Filters custom field markup for settings and management forms.

**`sh_podcasting_admin_submenu_pages`**

Filters Selfhost admin submenu pages.

**`sh_podcasting_admin_podcast_section_labels`**

Filters labels used for podcast management sections.

## Validation and sanitization hooks

**`sh_podcasting_pod_sanitization_methods`**

Filters podcast and settings sanitization callbacks.

**`sh_podcasting_epi_sanitization_methods`**

Filters episode sanitization callbacks.

**`sh_podcasting_integration_sanitization_methods`**

Filters integration sanitization callbacks.

## Feed output hooks

**`sh_podcasting_pod_feed_data`**

Filters the full prepared podcast feed data before markup arrays are generated.

**`sh_podcasting_feed_generator`**

Filters the class name used to generate feeds. The Pro module uses this to swap in its feed generator.

**`sh_podcasting_feed_podcast_id`**

Overrides the podcast ID resolved from a feed key. Migration feed takeover uses this pattern while serving source-compatible URLs.

**`sh_podcasting_should_register_feed`**

Controls whether a feed should be registered for a podcast.

**`sh_podcasting_channel_markup_array`**

Filters channel-level feed tags.

**`sh_podcasting_item_markup_array`**

Filters item-level feed tags.

**`sh_podcasting_namespaces`**

Filters RSS namespace declarations.

**`sh_podcasting_pod_escape_methods`**

Filters channel data escaping callbacks.

**`sh_podcasting_epi_escape_methods`**

Filters episode data escaping callbacks.

**`sh_podcasting_pod_excerpt_length`**

Filters podcast summary excerpt length.

**`sh_podcasting_epi_excerpt_length`**

Filters episode summary excerpt length.

**`sh_podcasting_episode_permalink`**

Filters episode links in the feed.

**`sh_podcasting_preview_audio_url`**

Filters audio URLs used by the browser preview.

## Save and lifecycle actions

**`selfhost_podcasting_podcast_created`**

Runs after a podcast is created.

**`selfhost_podcasting_podcast_saved`**

Runs after podcast data, settings, or management options are saved.

**`selfhost_podcasting_feed_settings_saved`**

Runs after feed settings are saved.

**`selfhost_podcasting_integration_saved`**

Runs after an integration is saved.

**`selfhost_podcasting_privacy_status_changed`**

Runs when podcast privacy status changes.

**`selfhost_podcasting_podcast_deleted`**

Runs when a podcast is deleted or a migrated podcast is removed.

**`selfhost_podcasting_episode_saved`**

Runs after an episode is saved or imported.

**`selfhost_podcasting_episode_deleted`**

Runs after an episode is detached or deleted from a podcast.

**`selfhost_podcasting_media_migrated`**

Runs after media is moved through the integration media migration flow.

## Background job hooks

The background queue identifier is `sh_podcasting_bg_jobs`. Several dynamic filters are built from it:

- `sh_podcasting_bg_jobs_process_interval`
- `sh_podcasting_bg_jobs_lock_timeout`
- `sh_podcasting_bg_jobs_max_dispatches`
- `sh_podcasting_bg_jobs_dispatch_window`
- `sh_podcasting_bg_jobs_max_consecutive_errors`
- `sh_podcasting_bg_jobs_enabled`
- `sh_podcasting_bg_jobs_max_upload_items_per_task`
- `sh_podcasting_bg_jobs_upload_circuit_window`
- `sh_podcasting_bg_jobs_upload_circuit_max_failures`
- `sh_podcasting_bg_jobs_query_args`
- `sh_podcasting_bg_jobs_query_url`
- `sh_podcasting_bg_jobs_post_args`
- `sh_podcasting_bg_jobs_memory_exceeded`
- `sh_podcasting_bg_jobs_queue_lock_time`

Task handlers use:

`sh_podcasting_bg_task_{$task_type}`

Built-in task types include `upload_media`, `delete_media`, and `backfill_duration`.

## S3 storage hooks

Storage-related filters include:

- `sh_podcasting_s3_multipart_threshold`
- `sh_podcasting_s3_multipart_part_size`
- `sh_podcasting_s3_max_remote_download_size`
- `sh_podcasting_s3_temp_space_buffer`
- `sh_podcasting_s3_verify_object_attempts`
- `sh_podcasting_s3_verify_delivery_url`

Use these only if you understand your provider's upload and delivery behavior.

## Migration hooks

**`sh_podcasting_migration_providers`**

Filters available migration providers.

**`selfhost_podcasting_migration_completed`**

Runs after migration completes.

**`selfhost_podcasting_takeover_status_changed`**

Runs when source feed takeover is enabled or disabled.

## Podcast Player hooks

**`selfhost_podcasting_podcast_player_validate_migration`**

Controls validation for Podcast Player migration handoff.

The integration also uses Podcast Player's external defaults filter when the installed Podcast Player version supports it.

## Pro private podcasting hooks

Private podcasting exposes filters including:

- `shp_private_podcasting_supported_integrations`
- `shp_private_feed_qr_url`
- `shp_private_token_email_subject`
- `shp_private_token_email_message`
- `shp_private_token_email_enabled`
- `shp_private_episode_access_min_range_bytes`

Use these to customize supported access providers, QR image generation, notification emails, and private episode access behavior.

## Compatibility advice

- Prefer filters over directly editing plugin metadata.
- Keep custom feed tags valid XML.
- Test feed output after changing markup hooks.
- Avoid expensive database queries inside feed filters.
- Be careful with private feed hooks because token validation and audio protection depend on predictable URLs and ownership checks.
