**Note:** The Podcast Player plugin now includes a [Shortcode Generator](https://easypodcastpro.com/docs/shortcode-generator/), offering a faster and more convenient way to create shortcodes. We recommend using this new method instead of manually writing traditional shortcodes. Shortcodes offeres the most flexible way to add a podcast player almost anywhere on your website. You can insert the player in posts, pages, widgets, with any page builder, or even dynamically inside a template file. Shortcodes work seamlessly with both the modern block editor and the classic editor. All you need to do is add a simple piece of text to your content. [easy_tubecasting instance="1" url="https://youtu.be/MmNzWXkH5ro?si=HZe4IVTHnSRXmp7o"]

### Insert shortcode

 To display the podcast player, simply add the following shortcode to any text area where you want the player to appear.

```
[[podcastplayer feed_url="your-podcast-feed-url"]]
```

 Make sure to replace `"your-podcast-feed-url"` with your actual podcast feed URL. You can use this shortcode in:
- Posts, Pages or any Custom post types
- Text widget
- Page builders (like Elementor)
- Custom templates

### Customization

 [easy_tubecasting instance="1" url="https://youtu.be/y2o32-6h0x0?si=ZWOJmufN3JATfwvY"] To personalize your podcast player, you can use various attributes in the shortcode. These attributes allow you to adjust the player’s appearance and functionality to better fit your website’s design.

#### Examples of Customization Attributes:

 **Change the Player Style**:

```
[[podcastplayer feed_url="your-podcast-feed-url" display_style="modern"]]
```

 This will adjust the layout of the player to a more modern design. **Show / Hide Player Elements**

```
[[podcastplayer feed_url="your-podcast-feed-url" display_style="modern" hide_search="true"]]
```

 This will hide the search bar in the player for a cleaner look. **Add Subscription Buttons**

```
[[podcastplayer feed_url="your-podcast-feed-url" display_style="modern" apple_sub="https://podcasts.apple.com/your_url" hide_search="true"]]
```

 This will add an Apple Podcasts subscription button to your player, allowing listeners to easily subscribe. **Change the Accent Color**

```
[[podcastplayer feed_url="your-podcast-feed-url" accent_color="#ff6600"]]
```

 This will set the accent color of the player to match your branding, enhancing the visual appeal.

### Shortcode Attributes

 Here we provide a full list of shortcode attributes supported by the podcast player. Use required attributes to customize your player.

#### Required attribute

 In the free version, you must enter your podcast feed URL to display the podcast player.

| Attribute | Description | Default Value |
| --- | --- | --- |
| feed_url | Your podcast feed url | '' |

#### Customize Podcast Content

 Podcast player automatically fetch content from your feed URL, however, you can modify some of the content using the following attributes,

| Attribute | Description | Default Value |
| --- | --- | --- |
| cover_image_url | Your Podcast’s cover image url | '' |
| podcast_menu | Any WordPress menu’s name, ID OR slug | '' |
| main_menu_items | Number of subscription badges or buttons to be displayed. | 0 |
| number | Number of podcasts episodes to be displayed at a time | 10 |
| no_scroll | Show initial loaded episodes without scrolling. | '' |
| excerpt_length | Excerpt length (only with default and premium display style) | 18 |
| teaser_text | Show Excerpt or Full Content or None Value Description '' Show Excerpt full Show Full Content none Show None | '' |
| Value | Description |
| '' | Show Excerpt |
| full | Show Full Content |
| none | Show None |

#### Style Player

| Attribute | Description | Default Value |
| --- | --- | --- |
| accent_color | Podcast player’s accent color hexcode | #65b84f |
| display_style | Podcast player display style. Possible Values: Value Description '' For default Layout modern Modern Layout legacy Catalogue Layout Refer pro for more styling options | '' |
| Value | Description |
| '' | For default Layout |
| modern | Modern Layout |
| legacy | Catalogue Layout |

#### Subscription Badges

| Attribute | Description | Default Value |
| --- | --- | --- |
| apple_sub | Apple Badge | '' (None) |
| google_sub | Google Badge | '' (None) |
| spotify_sub | Spotify Badge | '' (None) |
| breaker_sub | Breaker Badge | '' (None) |
| castbox_sub | CastBox Badge | '' (None) |
| castro_sub | Castro Badge | '' (None) |
| iheart_sub | iHeart Badge | '' (None) |
| overcast_sub | OverCast Badge | '' (None) |
| pocketcasts_sub | Pocket Cast Badge | '' (None) |
| podcastaddict_sub | Podcast Addict Badge | '' (None) |
| podchaser_sub | Podchaser Badge | '' (None) |
| radiopublic_sub | Radio Public Badge | '' (None) |
| soundcloud_sub | Soundcloud Badge | '' (None) |
| stitcher_sub | Stitcher Badge | '' (None) |
| tunein_sub | TuneIn Badge | '' (None) |
| youtube_sub | YouTube Badge | '' (None) |
| bullhorn_sub | Bullhorn Badge | '' (None) |
| podbean_sub | Podbean Badge | '' (None) |
| playerfm_sub | PlayerFM Badge | '' (None) |

#### Show / Hide Player elements

| Attribute | Description | Default Value |
| --- | --- | --- |
| header_default | Show player header items by default | false |
| list_default | Display Episodes list by default on small screen | false |
| hide_header | Hide player header items | false |
| hide_title | Show / Hide podcast Title in header info section | false |
| hide_cover | Show / Hide podcast cover image | false |
| hide_description | Show / Hide podcast description | false |
| hide_subscribe | Show / Hide podcast subscribe button | false |
| hide_search | Show / Hide podcast search field | false |
| hide_author | Show / Hide author/podcaster’s name | false |
| hide_content | Show / Hide podcast episode’s content | false |
| hide_loadmore | Show / Hide podcast load more button | false |
| hide_download | Show/ Hide episode download link | false |
| hide_social | Show/ Hide podcast episode social sharing links | false |
| hide_featured | Hide podcast episode featured image | false |

#### Sort & Filter

| Attribute | Description | Default Value |
| --- | --- | --- |
| sortby | Sort episodes Possible Values: Value Description sort_date_desc Sort by Date (Latest Episode First) sort_date_asc Sort by Date (Earliest Episode First) sort_title_desc Sort by Title (Z to A) sort_title_asc Sort by Title (A to Z) | sort_date_desc |
| Value | Description |
| sort_date_desc | Sort by Date (Latest Episode First) |
| sort_date_asc | Sort by Date (Earliest Episode First) |
| sort_title_desc | Sort by Title (Z to A) |
| sort_title_asc | Sort by Title (A to Z) |
| filterby | Filter by any string in the episode title | '' (None) |
