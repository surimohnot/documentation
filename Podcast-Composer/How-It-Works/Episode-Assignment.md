Episode assignment controls which source episodes appear in an output feed.

## Add Episodes to an Output Feed

1. Open a project.
2. Open a source feed.
3. Go to the source `Episodes` tab.
4. Select the episodes you want to use.
5. Click `Add to Output`.
6. Choose the destination output feed.

The selected episodes are added to that output feed.

## Assign the Same Episode to Multiple Outputs

You can add the same source episode to more than one output feed.

Example:

- Add an episode to `main-show`.
- Add the same episode to `best-of-feed`.
- Add the same episode to `partner-feed`.

Each output feed can then use its own metadata and optional episode override.

## Search Episodes

Use the search box in the source `Episodes` tab to find episodes by title.

This is useful for large catalogs.

## Filter by Assignment Status

The source `Episodes` tab includes an assignment filter.

Use it to focus on:

- All episodes.
- Assigned episodes.
- Unassigned episodes.

This helps you avoid forgetting episodes when building a curated feed.

## View Output Membership

In the source episode list, assigned episodes can show output labels. These labels help you see where an episode is already used.

## Remove Episodes From an Output

1. Open an output feed.
2. Go to the `Episodes` tab.
3. Find the episode.
4. Click `Remove`.
5. Confirm the action.

This removes only the output assignment.

It does not:

- Delete the source episode.
- Delete the source feed.
- Change the original RSS feed.
- Remove the episode from other output feeds.

## Assignment Order

The plugin records a sort order when episodes are assigned, but generated feeds are sorted by the output feed's advanced sorting logic:

- `Newest first`
- `Oldest first`

Use the `Advanced` tab on the output feed to control final feed order.

## Orphaned Source Episodes

When a source sync runs, episodes that no longer appear in the source feed are marked as orphaned.

Orphaned episodes are excluded from generated output feeds.

If an episode disappears unexpectedly:

1. Check the original source RSS feed.
2. Sync the source again.
3. Confirm the episode still exists in the source feed with an enclosure URL.
