Use this topic when you want one player to look different, show different podcast details, show subscription links, or hide parts of the player. These controls are available in the Shortcode Generator, editor block, widget, and podcast-specific Defaults tool where the current source and style support them.

## Open the Player Settings

Choose the place where the player is configured:

- **Shortcode Generator**: Go to **Podcast Player > Shortcode**, create or load a saved shortcode, then open the relevant option groups.
- **Editor block**: Edit a post or page, select the **Podcast Player** block, then use the block sidebar panels.
- **Widget**: Go to **Appearance > Widgets**, open the Podcast Player widget, then expand the option sections.
- **Defaults tool**: Go to **Podcast Player > Toolkit > Defaults** to save reusable feed-level defaults.

## Customize Podcast Content

Use **Customize Podcast Content** for feed and post players.

Available controls include:

- **Podcast Cover Image**: Upload or choose a Media Library image to override feed artwork.
- **External Cover Image URL**: Available in direct shortcode/default fields when an external image URL is preferred.
- **Brief Description**: Override the podcast description shown in the header.
- **Episodes to show at a time**: Sets the initial batch size and load-more step.
- **Episodes to skip from the beginning**: Skips the first matching episodes after sorting/filtering.
- **Show initial loaded episodes without scrolling**: Applies to the default and modern mini-player style.
- **Teaser Text**: Show excerpt, show full content, or hide teaser text.
- **Excerpt Length** and **Excerpt Length Unit**: Control excerpt size by words or characters.

Single audio/video players use a smaller content set:

- **Episode Title**
- **Episode link for social sharing**
- Optional cover image and style controls

## Choose Layout and Style

Open **Podcast Player Styling** or the block style controls.

Main controls:

- **Podcast Player Display Style**
- **Accent Color**
- **Player Background Color**
- **Text Color Scheme**
- **Select Google Font**
- **Thumbnail Cropping**
- **Thumbnail Cropping Position**
- **Maximum Grid Columns**

Pro layout values include:

- `lv1`: List - Normal
- `lv2`: List - Small
- `lv3`: List - Minimal
- `lv4`: List - Individual
- `gv1`: Grid - Normal
- `gv2`: Grid - Cards

Some style controls appear only when the selected layout supports them. For example, grid columns appear for grid styles, thumbnail cropping appears for thumbnail-based styles, and text color scheme appears only for supported list/grid styles.

## Manual Style Shortcode Example

```
[[podcastplayer feed_url="https://example.com/feed.xml" display_style="gv1" grid_columns="3" accent_color="#1488cc" bgcolor="#ffffff" txtcolor="" font_family="Roboto" aspect_ratio="squr" crop_method="centercrop"]]
```

## Add Subscription Links

Podcast Player can show subscription links in two ways.

Use individual service links:

1. Open **Subscription Button Links**.
2. Add URLs for the platforms you want to show.
3. Leave unused services empty.
4. Save the player.

Supported service fields include Apple, Google, Spotify, Amazon, Overcast, Pocket Casts, Podcast Addict, Podchaser, RadioPublic, SoundCloud, Stitcher, TuneIn, YouTube, Bullhorn, Podbean, Player FM, and the other services exposed by the plugin service list.

Use a WordPress menu:

1. Go to **Appearance > Menus** and create a menu of subscription links.
2. Edit the player.
3. Select the menu under **Subscription menu**.
4. Set **Number of primary subscription links** if some links should appear before the grouped menu.
5. Save.

Manual subscription shortcode example:

```
[[podcastplayer feed_url="https://example.com/feed.xml" spotify_sub="https://open.spotify.com/show/example" apple_sub="https://podcasts.apple.com/example"]]
```

## Show or Hide Player Items

Open **Show/Hide Player Items**.

Common controls:

- **Show podcast header by default**
- **Show episode list by default on mini player**
- **Hide podcast header information**
- **Hide cover image**
- **Hide podcast title**
- **Hide podcast description**
- **Hide custom menu**
- **Hide podcast search**
- **Hide episode author or podcaster name**
- **Hide episode text content or transcript**
- **Hide load more episodes button**
- **Hide episode download link**
- **Hide social share links**
- **Hide episode featured images**

Manual shortcode example:

```
[[podcastplayer feed_url="https://example.com/feed.xml" hide_header="true" hide_search="true" hide_download="true" hide_social="true"]]
```

If **Hide podcast header information** is enabled in the Shortcode Generator, its child header controls are hidden because the whole header is already hidden.

## Show or Hide Items for Single Audio/Video Players

For **From Audio/Video Link**, the Shortcode Generator and widget show a source-specific **Show/Hide Player Items** group with:

- **Hide Episode Download Link**
- **Hide Social Share Links**

Search, author, episode content, and load more are automatically hidden for single media players.

## Select Episodes, Seasons, and Categories

Episode selection is part of sorting and filtering, but it affects what content appears and often belongs in the same setup pass as visibility.

For feed players, the block, Shortcode Generator, and widget can show:

- **Select Seasons to be displayed**
- **Select Categories to be displayed**
- **Select Episodes to be displayed**
- **Show/Hide selected episodes**

For post players, the block, Shortcode Generator, and widget can show:

- **Select Post Type**
- **Get Episodes by Taxonomy**
- **Select Terms**
- **Select Episodes to be displayed**
- **Show/Hide selected episodes**

Use How to Sort and Filter Episodes for the full selection workflow and shortcode attribute details.
