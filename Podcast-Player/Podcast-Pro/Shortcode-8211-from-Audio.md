**Note:** The Podcast Player plugin now includes a [Shortcode Generator](https://easypodcastpro.com/docs/shortcode-generator/), offering a faster and more convenient way to create shortcodes. We recommend using this new method instead of manually writing traditional shortcodes.

In addition to the shortcode features in the free plugin, pro plugin also support many other features and styling options. Instructions to use the podcast player is already explained in the **Display Podcast > Shortcode** section. We need slight variation in shortcode to display single podcast player from audio URL.

An example of the shortcode to display podcast player from audio URL is as follows,

```
[[podcastplayer fetch_method="link" mediasrc="url_of_media_file"]]
```

We can add a few more attribute to customize the player,

```
[[podcastplayer fetch_method="link" mediasrc="url_of_media_file" episodetitle="title_for_the_episode" episodelink="episode_link_for_sharing"]]
```

For advanced setup, there are many shortcode parameters you can use to customise display of your podcast player. Shortcode parameters mentioned in above example is just for demonstration purpose. **You need not use all of the parameters mentioned in below table, just use whatever is required to achieve a particular customization.**

Complete list of parameters is as below,

#### Required Attributes

| Attribute | Description | Default Value |
| --- | --- | --- |
| fetch_method | How to fetch podcast episodes.Options:feed (fetch from feed url)post (fetch from post or post type)link (fetch from audio or video URL) | 'feed' |
| mediasrc | Audio or Video media URL (i.e., mp3, mp4 etc. file url). | '' |

#### Customize Podcast Content

Podcast player automatically fetch content from your feed URL, however, you can modify some of the content using the following attributes,

| Attribute | Description | Default Value |
| --- | --- | --- |
| episodetitle | Title of the episode | '' |
| episodelink | Link of the epsiode for social sharing (optional) | '' |
| cover_image_url | Your Podcast’s cover image url | '' |
| podcast_menu | Any WordPress menu’s name, ID OR slug | '' |
| main_menu_items | Number of subscription badges or buttons to be displayed. | 0 |
| number | Number of podcasts episodes to be displayed at a time | 10 |
| excerpt_length | Excerpt length (only with default and premium display style) | 18 |

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
| hide_download | Show/ Hide podcast episode download link | false |
| hide_social | Show/ Hide podcast episode social sharing links | false |

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

#### Custom Audio Messgaes

| Attribute | Description | Default Value |
| --- | --- | --- |
| audio_msg | URL of mp3 audio file which is to be played before, after or during podcast episodes. | '' |
| play_freq | After how many episodes the audio should be replayed. | 0 |
| msg_start | When to start playing the audio message. Possible values are:start (Play at the beginning of the episode.)end (Play at the end of the episode.)custom (Play at any given custom time. Check below mentioned ‘msg_time’ option below) | ‘start’ |
| msg_time | Required only if above msg_start is set as ‘custom’. Enter time at which the audio should be played in hh:mm:ss format. | ’00:00:00′ |
| msg_text | Message text to be displayed while playing audio. | '' |
