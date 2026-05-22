# Frontend Interactive Features

Easy TubeCasting is not just a static embed. It provides player controls and playlist tools for visitors. Playlist tools appear when the block has more than one video and **Videos Per Batch** is greater than `1`, whether those videos come from comma-separated URLs or an API-powered collection.

## 1. Real-time Search

At the top of the video list, users will find a search bar.

- **How it works:** As the user types, the list filters instantly to show matching titles or author names.
- **Clear Search:** A "Clear" button appears when searching, allowing users to quickly return to the full list.

## 2. Dynamic Sorting

Users can reorder the video list based on several criteria:

- **Default:** The order provided by YouTube (usually reverse chronological).
- **Newest/Oldest:** Sort by publication date.
- **Most Viewed:** Show the most popular content first.
- **Longest:** Sort by video duration.
- **A-Z:** Alphabetical sorting of titles.

## 3. "Load More" Pagination

- **Behavior:** After the initial batch of playlist items is displayed, a "Load More" button appears at the bottom.
- **Configuration:** You can change how many videos are shown each time with **Videos Per Batch** in the block editor settings.
- **Search Exception:** When a visitor searches, all matching results are shown instead of hiding matches behind Load More.

## 4. Responsive Player

- **Interactive Thumbnails:** Hovering over a thumbnail shows the video duration and a play icon.
- **Instant Play:** Clicking any video in the list starts playback immediately in the main player area without refreshing the page.
- **Custom Controls:** Visitors can play/pause, seek, go back 15 seconds, skip ahead 15 seconds, adjust volume, and use fullscreen.
- **Captions:** A captions button appears when the YouTube player reports caption tracks are available.
- **Single Active Player:** Starting playback in one Easy TubeCasting block pauses other initialized Easy TubeCasting players on the page.
