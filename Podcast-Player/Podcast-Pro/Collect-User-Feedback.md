Podcast Player Pro can show a feedback prompt after a listener has played an episode for a configured amount of time.

## Enable Feedback for a Player

1. Edit the player in the Shortcode Generator, block, widget, or Defaults tool.
2. Open **User Feedback**.
3. Enable **User Feedback**.
4. Set **Show feedback after this many seconds**.
5. Enter the feedback question.
6. Enter the positive feedback response.
7. Optionally enter a positive feedback URL.
8. Enter the negative feedback response.
9. Choose whether to show the negative feedback form.
10. Save and test.

## Manual Shortcode Example

```
[podcastplayer feed_url="https://example.com/feed.xml" feedback="yes" show_form_time="60" feedback_text="Are you enjoying this episode?"]
```

## Email Behavior

When the negative feedback form is enabled, listener messages are sent to the WordPress admin email address using `wp_mail()`.

## Stats Requirement

Feedback counting is tied to the Pro stats setting. Enable **Collect Podcast Player Stats (Beta)** if feedback events should be recorded.
