Podcast Player automatically fetches and processes podcast feed data from your provided feed URL. This includes retrieving podcast episodes, metadata, and other relevant information. To optimize server performance and minimize processing time, Podcast Player stores the fetched data in your website’s database. This caching mechanism prevents the plugin from fetching the data each time someone visits your podcast page. However, there are cases where you may want to control how often your podcast feed is updated or force a manual update. This guide will walk you through how to modify the feed update interval and perform a one-time manual update. [easy_tubecasting instance="1" url="https://youtu.be/r3hniqk6bRo?si=17aD95KUQWZz7NSG"]

### **Understanding the Podcast Feed Update Process**

 When you add your podcast feed URL, Podcast Player fetches the data, sanitizes it, and processes the required information. While this process is efficient, it does consume time and server resources. To optimize performance, Podcast Player caches the data in your website’s database, so it doesn’t need to repeat the process every time someone visits the podcast page. By default, Podcast Player automatically updates the podcast feed data every **12 hours** (720 minutes). However, you can change this update interval or manually force an update at any time.

---

### **Modifying the Podcast Update Interval**

 If you want to adjust the frequency at which Podcast Player checks for new episodes, you can change the update interval. Here’s how to modify it:

#### Step-by-Step Instructions:

1. **Access Podcast Player Settings:**
  - Go to your WordPress dashboard.
  - Navigate to **Podcast Player > Settings**.
2. **Locate the Podcast Update Interval Setting:**
  - The first option you’ll see on the settings page is **Podcast update interval (in minutes)**.
  - The default value is set to **720 minutes** (equivalent to 12 hours).
3. **Change the Update Interval:**
  - You can adjust this value based on your needs. If your podcast release cycle is shorter, you might want to decrease the interval. If you release episodes less frequently, you may increase the interval.
  - For example, setting it to **1440 minutes** will update the feed once a day, while setting it to **360 minutes** will update it every 6 hours.
4. **Save Your Changes:**After adjusting the interval, click **Save Changes** to apply the new update frequency.

---

### **Performing a Manual Update of the Podcast Feed**

 There may be instances when you want to update the podcast data immediately without waiting for the next scheduled update. This can be especially useful if you release a new episode and want it to appear on your site right away. To perform a manual update, follow these steps:

#### Step-by-Step Instructions:

1. **Access the Podcast Player Toolkit:**
  - Go to your WordPress dashboard.
  - Navigate to **Podcast Player > Toolkit**.
2. **Use the Feed Updation Tool:**
  - On the Toolkit page, find and click on the **Feed Updation Tool** option.
3. **Select Your Podcast:**
  - A dropdown menu will appear with a list of your available podcasts.
  - Choose the podcast feed that you want to update.
4. **Update the Podcast:**
  - Once you've selected the correct podcast, click the **Update Podcast** button.
  - The podcast player will fetch the latest data from your feed and update the podcast episodes immediately.

---

### **When to Update the Podcast Feed Manually or Adjust the Interval**

- **Frequent Episode Releases:** If you release new episodes more frequently than every 12 hours, consider shortening the update interval or performing manual updates after new episodes are published.
- **Immediate Changes:** If you’ve made important changes to your podcast (e.g., editing an episode title or adding new artwork), you may want to use the manual update tool to see those changes reflected immediately.

---

### Conclusion

 Podcast Player automatically updates your feed data at regular intervals (12 hours by default) to balance performance and fresh content delivery. However, by adjusting the update interval in the settings or using the feed updation tool, you can ensure that your podcast player always reflects the latest content without delays. This flexibility ensures that your listeners always have access to the most up-to-date episodes, while your website’s performance remains optimized. For enhanced control over podcast updates and even more customization options, consider exploring the pro features of Podcast Player.
