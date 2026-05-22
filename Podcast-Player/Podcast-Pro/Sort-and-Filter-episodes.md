Sorting and filtering determine which episodes are available to the player, the order in which they appear, and which episodes are available in the episode checkbox selector. These controls apply to **From Feed URL** and **From Posts** players. They do not apply to **From Audio/Video Link**, because that source has only one media item.

## Where the Controls Appear

 In the Shortcode Generator and widget, open **Sort & Filter Options**. In the editor block, select the **Podcast Player** block, then open **Sort & Filter Options** in the block sidebar. The controls are dynamic:
- Feed players load seasons, categories, and episode checkboxes from the feed URL.
- Post players load episode checkboxes from the selected post type, taxonomy, terms, sorting, and title filter.
- Changing a feed URL, post type, taxonomy, terms, season, category, sort option, or title filter refreshes the available episode checklist.

## Sort Episodes

 Choose **Sort Podcast Episodes By**. Available values:
- **Date Descending** (`sort_date_desc`): Newest first.
- **Date Ascending** (`sort_date_asc`): Oldest first.
- **Title Descending** (`sort_title_desc`): Z to A by title.
- **Title Ascending** (`sort_title_asc`): A to Z by title.
- **Do Not Sort** (`no_sort`): Keep the feed or query order.
- **Reverse Sort** (`reverse_sort`): Reverse the current feed/order result.

 Manual shortcode example:

```
[[podcastplayer feed_url="https://example.com/feed.xml" sortby="sort_date_desc" ]]
```

 For **From Posts**, sorting is applied to the WordPress query: title sort maps to post title, and date sort maps to post date.

## Filter by Title Text

 Use **Only show episodes whose title contains** or **Show episodes only if title contains following**. Manual shortcode example:

```
[[podcastplayer feed_url="https://example.com/feed.xml" filterby="interview"]]
```

 For feed players, this filters feed episode titles. Pro also improves front-end search with deeper matching. For post players, this narrows the post query by title and also affects the post episode checklist.

## Set Episode Count and Offset

 These are not inside the Sort & Filter group in every UI, but they affect the final displayed list.
- **Episodes to show at a time** (`number`): Initial episode count and load-more step.
- **Episodes to skip from the beginning** (`offset`): Skips matching episodes after the source query/filter order is prepared.

 Example:

```
[[podcastplayer feed_url="https://example.com/feed.xml" number="8" offset="2"]]
```

## Set Autoplay Behavior

 Use **Autoplay Behavior**.
- **Default (Follow visual list order)**: The player advances in the displayed order.
- **Reverse (Opposite of visual list order)**: The player advances opposite the displayed order.
- **Disabled (No autoplay)**: The player does not automatically continue to the next episode.

 Manual shortcode example:

```
[[podcastplayer feed_url="https://example.com/feed.xml" autoplay="disable"]]
```

## Filter Feed Players by Season

 For **From Feed URL** players, Pro can load season values from the feed. In the block:
1. Enter or select a feed URL.
2. Open **Sort & Filter Options**.
3. Use **Select Seasons to be displayed**.
4. Check one or more seasons, or keep **Show All Seasons** selected.

 In the Shortcode Generator or widget:
1. Select **Audio Source > From Feed URL**.
2. Enter or choose the feed URL.
3. Open **Sort & Filter Options**.
4. Use **Select seasons to be displayed**.
5. If **Show All Seasons** is checked, the individual season checkboxes are disabled. Uncheck it to choose specific seasons.

 Manual shortcode example:

```
[[podcastplayer feed_url="https://example.com/feed.xml" seasons="1,2"]]
```

 Internally, the shortcode maps `seasons` to the Pro season filter list.

## Filter Feed Players by Category

 For **From Feed URL** players, Pro can load category values from the feed. In the block:
1. Enter or select a feed URL.
2. Open **Sort & Filter Options**.
3. Use **Select Categories to be displayed**.
4. Check one or more categories, or keep **Show All Categories** selected.

 In the Shortcode Generator or widget:
1. Select **Audio Source > From Feed URL**.
2. Enter or choose the feed URL.
3. Open **Sort & Filter Options**.
4. Use **Select Categories to be displayed**.
5. If **Show All Categories** is checked, the individual category checkboxes are disabled. Uncheck it to choose specific categories.

 Manual shortcode example:

```
[[podcastplayer feed_url="https://example.com/feed.xml" categories="news,interviews"]]
```

 Internally, the shortcode maps `categories` to the Pro category filter list.

## Select Specific Feed Episodes

 Use this when a feed player should show only chosen episodes or hide chosen episodes. In the editor block:
1. Select **Audio Source > From Feed URL**.
2. Enter or select the feed URL.
3. Optional: choose seasons and categories first. The block refreshes the episode list using those filters.
4. Open **Sort & Filter Options**.
5. Use **Select Episodes to be displayed**.
6. Check the episodes you want to target.
7. Use **Show or Hide above selected episodes**:

- **Show above selected episodes** shows only the checked episodes.
- **Hide above selected episodes** removes the checked episodes from the otherwise matching list.

 In the Shortcode Generator or widget:
1. Select **Audio Source > From Feed URL**.
2. Enter or select the feed URL.
3. Open **Sort & Filter Options**.
4. Optional: choose season and category filters first.
5. Use **Select Episodes to be displayed**.
6. If **Show All Episodes** is checked, individual episode checkboxes are disabled. Uncheck it to choose specific episodes.
7. Select the episodes.
8. Use **What should happen to selected episodes?**:

- **Show selected episodes**
- **Hide selected episodes**

1. Save the player.

 Manual direct shortcode can show selected feed episode keys:

```
[[podcastplayer feed_url="https://example.com/feed.xml" elist="episode-key-1,episode-key-2"]]
```

 Direct shortcode supports showing selected `elist` episode keys. The **hide selected episodes** option in the Shortcode Generator, block, and widget is stored as `edisplay`; it is not exposed as a direct `[podcastplayer]` shortcode attribute in the current shortcode defaults.

## Filter Feed Episodes by RSS Episode Number

 Direct shortcodes also support the `episodes` attribute. This is separate from `elist`. Use `episodes` when the RSS feed stores episode numbers and you want to match those numbers:

```
[[podcastplayer feed_url="https://example.com/feed.xml" episodes="101,102,103"]]
```

 Use `elist` when you want to match Podcast Player's saved episode keys, usually chosen through the block, Shortcode Generator, or widget checkbox list.

## Filter Post Players by Post Type, Taxonomy, and Terms

 For **From Posts** players, Pro builds the episode list from WordPress content that contains valid audio or video. In the editor block:
1. Select **Audio Source > From Posts**.
2. Choose **Post Type**.
3. Choose a taxonomy if needed.
4. Select terms if needed.
5. Open **Sort & Filter Options**.
6. Choose sorting and title filtering.
7. The block refreshes **Select Episodes to be displayed** from the matching posts.

 In the Shortcode Generator or widget:
1. Select **Audio Source > From Posts**.
2. Choose **Select Post Type**.
3. Choose **Get Episodes by Taxonomy** if needed.
4. Choose **Select Terms** if needed.
5. Open **Sort & Filter Options**.
6. Set sorting and title filtering.
7. Use **Select Episodes to be displayed** if you want specific posts only.

 Manual shortcode example:

```
[[podcastplayer fetch_method="post" post_type="post" taxonomy="category" terms="interviews" sortby="sort_date_desc" filterby="bonus"]]
```

## Select Specific Post Episodes

 In the editor block, Shortcode Generator, or widget:
1. Configure **From Posts** source first.
2. Choose post type, taxonomy, terms, sorting, and title filter.
3. Open **Sort & Filter Options**.
4. Use **Select Episodes to be displayed**.
5. Check the posts you want to target.
6. Choose whether selected episodes should be shown or hidden.

 For post players, `elist` stores WordPress post IDs. Manual shortcode example to show specific post IDs:

```
[[podcastplayer fetch_method="post" elist="123,456,789"]]
```

 As with feed players, the direct shortcode can show the IDs in `elist`, while the UI-only `edisplay` control is needed for hiding selected items.

## Front-End Category and Season Filters

 Feed players also pass selected seasons and categories to the front-end Ajax loader. When visitors use front-end filtering or search, those selected season/category restrictions continue to apply.

## Selection Priority

 Filters combine in this order conceptually:
1. Source is chosen: feed, posts, or single media.
2. Feed/post source filters are applied: seasons, categories, post type, taxonomy, terms, and title filter.
3. Sort order is applied.
4. `offset` skips matching items.
5. `elist` shows or hides selected episodes depending on UI `edisplay`.
6. `number` controls the initial displayed count and load-more step.

## Troubleshooting

- If episode checkboxes do not appear, confirm the source is valid and saved/loaded in the Shortcode Generator, block, or widget.
- If feed episode checkboxes are disabled, uncheck **Show All Episodes**.
- If season or category choices are missing, confirm the feed actually includes season/category metadata.
- If post episode choices are missing, confirm the selected posts contain valid audio/video, PowerPress data, Seriously Simple Podcasting audio metadata, imported podcast metadata, or an audio/video embed in the content.
- If a direct shortcode needs the exact feed episode keys, use the Shortcode Generator or block to load the feed and identify the selectable episodes more safely.
