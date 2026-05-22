**Note:** The Podcast Player plugin now includes a [Shortcode Generator](https://easypodcastpro.com/docs/shortcode-generator/), offering a faster and more convenient way to create shortcodes. We recommend using this new method instead of manually writing traditional shortcodes.

In addition to the shortcode features in the free plugin, pro plugin also support many other features and styling options. Instructions to use the podcast player is already explained in the **Display Podcast > Shortcode** section. We need slight variation in shortcode to display podcast player from wordpress posts.

An example of the shortcode to display podcast player from wordpress posts is as follows,

```
[[podcastplayer fetch_method="post" post_type="post OR any_custom_post_type"]]
```

We can also filter posts by taxonomy terms. The shortcode will look something like the following,

```
[[podcastplayer fetch_method="post" post_type="post OR any_custom_post_type" taxonomy="category/tag OR any_custom_taxonomy" terms="comma_separated_list_of_terms"]]
```

For advanced setup, there are many shortcode parameters you can use to customise display of your podcast player. Shortcode parameters mentioned in above example is just for demonstration purpose. **You need not use all of the parameters mentioned in below table, just use whatever is required to achieve a particular customization.**

Complete list of parameters is as below,

#### Requried Attribute

| Attribute | Description | Default Value |
| --- | --- | --- |
| fetch_method | How to fetch podcast episodes.Options:feed (fetch from feed url)post (fetch from post or post type)link (fetch from audio or video URL) | 'feed' |
| post_type | Enter post or post type from which episodes are to be fetched. | 'post' |

#### Get Required Content

| Attribute | Description | Default Value |
| --- | --- | --- |
| taxonomy | Select taxonomy to filter episodes list. | '' |
| terms | comma separated list of taxonomy terms from which episodes are to be fetched. | '' |

#### Customize Podcast Content

Podcast player automatically fetch content from your feed URL, however, you can modify some of the content using the following attributes,

| Attribute | Description | Default Value |
| --- | --- | --- |
| cover_image_url | Your Podcast’s cover image url | '' |
| podcast_menu | Any WordPress menu’s name, ID OR slug | '' |
| main_menu_items | Number of subscription badges or buttons to be displayed. | 0 |
| number | Number of podcasts episodes to be displayed at a time | 10 |
| excerpt_length | Excerpt length (only with default and premium display style) | 18 |

#### Style Player

| Attribute | Description | Default Value |
| --- | --- | --- |
| accent_color | Podcast player’s accent color hexcode | #65b84f |
| display_style | Podcast player display style.Available Options:'' (For default Layout)'modern' (for Modern Layout)'legacy' (for Legacy Layout)'gv1' (for Grid View)'gv2' (for Material design grid view)'lv1' (for list view)'lv2' (for small list view)'lv3' (for minimalist list view)'lv4' (for individual list view) | '' |
| bgcolor | Background Color hex code (i.e., #262626). | '' |
| txtcolor | Make light text color for grid and list view (use txtcolor=”ltext”). | '' |
| aspect_ratio | Featured image aspect ratio (only with grid view and list view display style).Options:land1 (for landscape 4:3)land2 (for landscape 3:2)port1 (for portrait 3:4)port2 (for portrait 2:3)wdscrn (for widescreen 16:9)squr (for square 1:1) | 'squr' |
| crop_method | Featured image crop method (only with grid view and list view display style).Options: topleftcrop, topcentercrop, centercrop, bottomleftcrop, bottomcentercrop | ‘centercrop’ |
| grid_columns | Number of grid columns (only with grid view display style) | 3 |
| font_family | Name of google font to be loaded. | '' |

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
| hide_download | Show/ Hide podcast episode download link | false |
| hide_social | Show/ Hide podcast episode social sharing links | false |
| hide_featured | Hide podcast episode featured image (Value: true OR false) | false |

#### Sort & Filter

| Attribute | Description | Default Value |
| --- | --- | --- |
| sortby | Sort episodesAvailable OptionsSort by Date (Latest Episode First) - sort_date_descSort by Date (Earliest Episode First) - sort_date_ascSort by Title (Z to A) - sort_title_descSort by Title (A to Z) - sort_title_asc | sort_date_desc |
| filterby | Filter by any string in the episode title | '' (None) |
| seasons | Comma separated iTunes season numbers from which episodes to be displayed. | '' |
| episodes | Comma separated iTunes episode numbers. If you are using seasons, please use season-episode format (i.e, for season 2 episode 6, use 2-6) otherwise just enter episode number. | '' |
| categories | Comma separated iTunes categories from which episodes to be displayed. | '' |

#### Custom Audio Messgaes

| Attribute | Description | Default Value |
| --- | --- | --- |
| audio_msg | URL of mp3 audio file which is to be played before, after or during podcast episodes. | '' |
| play_freq | After how many episodes the audio should be replayed. | 0 |
| msg_start | When to start playing the audio message. Possible values are:start (Play at the beginning of the episode.)end (Play at the end of the episode.)custom (Play at any given custom time. Check below mentioned ‘msg_time’ option below) | ‘start’ |
| msg_time | Required only if above msg_start is set as ‘custom’. Enter time at which the audio should be played in hh:mm:ss format. | ’00:00:00′ |
| msg_text | Message text to be displayed while playing audio. | '' |
