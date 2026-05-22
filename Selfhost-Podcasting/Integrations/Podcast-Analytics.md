Selfhost Podcasting supports integration with third-party podcast analytics services by allowing you to specify an **analytics prefix URL** (also called a redirect prefix). Once configured, this prefix is prepended to each episode’s audio URL before being output in the RSS feed (and any embedded players). The analytics provider thus receives the download/stream request first, records metrics, and then redirects the request to the actual audio file.

This method is commonly used by services like **Podtrac**, **Blubrry**, and **OP3**. Below is the full workflow: registering with a service, configuring the prefix in Selfhost Podcasting, verifying it, and viewing analytics.

## Why Use a Prefix for Analytics?

Using a prefix has several benefits:

- It provides **independent measurement** of downloads/streams.
- It does not require hosting provider support (as you can control the feed output).
- It’s invisible to users: the redirection happens instantly, causing minimal latency.

In practice, when a podcast client or browser requests an episode, it hits the prefix URL first (which logs the request) and then immediately issues a redirect to the real URL, delivering the media file.

## Steps to Set Up Analytics Prefix in Selfhost Podcasting

Below is a user guide to integrate analytics with Selfhost Podcasting:

### 1. Register / Obtain your analytics prefix from the chosen service

You can visit anyone of the following free analytics services to register and get prefix URL.

- Podtrac: Visit podtrac documentation to register and get prefix URL, https://podtrac.freshdesk.com/support/solutions
- Blubrry: Blubrry analytics documentation is available at https://blubrry.com/support/statistics-documentation/
- OP3: OP3 documentation is available at https://op3.dev/setup

### 2. Enter the prefix in Selfhost Podcasting

1. In WordPress admin, go to **Selfhost Podcasting → Integrations** (or wherever you manage analytics settings).
2. Find the field labeled “Analytics Prefix / Redirect Prefix / External Analytics” (or similar).
3. Paste the analytics prefix URL you received (or selected) from the service.
4. Save or update the podcast settings.
5. After saving, the plugin will automatically prepend this prefix to each episode’s audio URL (enclosure) when generating the feed or embedding.

## Verification & Testing

Once the prefix is set, you should verify that it is applied correctly and that analytics are working.

- Open your podcast’s RSS in a browser, right click and select “View Page Source.”
- Check the `<enclosure>` tags of recent episodes. The `url` attribute should start with your analytics prefix, followed by the original audio path.

## Sample Workflow (User Journey)

1. Choose analytics provider (e.g. Podtrac) and sign up/account registration.
2. Copy your prefix URL from their dashboard (e.g. `https://dts.podtrac.com/redirect.mp3/`).
3. Go to Selfhost Podcasting > Integrations > Thrid Party Analytics. Paste the prefix. Save settings.
4. Verify by viewing your podcast RSS and inspecting enclosure URLs.
5. Request or listen to an episode to generate traffic.
6. After 24–48 hours, log into the analytics dashboard to see data.
7. Monitor and confirm download counts, listener geography, or other stats (depending on provider).
