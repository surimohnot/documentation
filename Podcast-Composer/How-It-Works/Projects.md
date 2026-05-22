Projects organize your work in Podcast Composer.

## When to Create a Project

Create a project when you have a group of feeds that belong together.

Good examples:

- One client.
- One podcast network.
- One show with several alternate feeds.
- One campaign or content package.
- One archive you want to curate.

Avoid putting unrelated clients or unrelated shows in the same project unless you intentionally want to combine their episodes.

## Project Dashboard

The main `Manage Projects` screen shows project cards.

Each card can show:

- Project name.
- Project status.
- Number of source feeds.
- Number of output feeds.
- Number of indexed episodes.
- Last sync time.

Available actions include:

- `Manage` to open the project.
- `Sync` to sync all sources in the project.
- Delete project.

## Create a Project

1. Go to `Podcast Composer > Manage Projects`.
2. Click `Create First Project` or `Create Project`.
3. Open the new project.

If you do not enter a name, the plugin generates a name such as `Project 1`.

## Rename a Project

Inside the project workspace:

1. Click the rename control near the project title.
2. Enter the new project name.
3. Click `Rename Project`.

Renaming a project does not change feed URLs. Feed URLs are controlled by output feed slugs.

## Sync a Project

From the project card, click `Sync`.

This syncs all source feeds in the project. The result message reports how many source feeds synced and how many failed.

Use project sync when:

- You have several source feeds.
- You want to refresh all episode indexes.
- You recently changed several source feeds on the original host.

## Delete a Project

Deleting a project removes the project and related plugin data for that project, including:

- Sources in the project.
- Indexed episodes from those sources.
- Episode-to-output mappings.
- Output feeds in the project.

This does not delete or modify your original external podcast feeds or audio files.

Before deleting a project, make sure no one is using its output feed URLs.
