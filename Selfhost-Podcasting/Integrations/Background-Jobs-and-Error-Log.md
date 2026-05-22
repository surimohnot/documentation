## Background Jobs and Error Log

Selfhost Podcasting uses background jobs for tasks that can take longer than a normal admin request.

Background jobs are used for:

- Uploading media to S3-compatible storage.
- Deleting bucket objects after episode or podcast deletion.
- Backfilling missing episode durations.
- Refresh-related integration tasks through hooks.

## How jobs run

The queue is stored in WordPress options and processed through a non-blocking admin AJAX request after shutdown. A WP-Cron fallback also runs on an interval so queues can recover if loopback dispatch is blocked.

The queue uses:

- A process interval.
- A process lock to prevent overlapping workers.
- Memory checks.
- Dispatch throttling.
- Retry attempts.
- A circuit breaker for repeated upload failures.

## Error log

Each podcast can store the most recent background job errors. The log keeps up to 20 errors to avoid database bloat.

Open a podcast and go to **Error Log** to review:

- Job type.
- Timestamp.
- Error message.
- Attempt count.
- Related task data.

If there are no errors, the panel shows a success message.

## Clearing errors

Use **Clear All Errors** to remove logged errors for that podcast. Clearing the log does not automatically fix the underlying issue.

Fix the cause first, then clear the log so new errors are easier to identify.

## Resume jobs

If dispatch is blocked after repeated failures, use the resume jobs action when available. This clears dispatch throttles, clears stale locks, and removes upload suspension state.

Resume jobs after you have fixed the cause, such as bad S3 credentials or a blocked remote media URL.

## Upload suspension

For S3 uploads, repeated terminal failures can trip an upload guard. When this happens, upload jobs for that podcast can be suspended to avoid repeated failed attempts.

Common causes:

- Invalid S3 credentials.
- Bucket permissions changed.
- Public domain does not serve files.
- Remote source audio cannot be downloaded.
- Server cannot read the local file.
- Provider endpoint or region is wrong.

## Missing duration repair

If an episode is saved without duration, the feed generator can queue a background duration backfill task. The task tries to determine duration from:

- WordPress attachment metadata.
- Audio URL metadata.
- Remote audio inspection.

If duration still cannot be determined, the task records a failed state and waits before retrying.

## Troubleshooting queue issues

If background jobs do not run:

- Confirm WP-Cron is working.
- Check whether loopback requests are blocked by the host, firewall, maintenance mode, or security plugin.
- Check PHP memory limits.
- Check the podcast error log.
- Temporarily disable caching/security rules that block `admin-ajax.php`.
- Verify the site URL and home URL are correct.

If a job repeatedly fails, fix the underlying media, storage, or connectivity issue before resuming the queue.
