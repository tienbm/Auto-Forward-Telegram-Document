---
icon: clock
---

# Schedule Telegram Message Posting Automatically

{% hint style="info" %}
This is a feature help you schedule auto post a last message from source to target on Auto Forward
{% endhint %}

{% hint style="success" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

If you’re looking to **schedule Telegram message posting** automatically, you’re in the right place. Whether you’re managing news updates, crypto alerts, or community broadcasts, this feature can save hours of manual work every week.\
\
With the **Auto Post Scheduler** in the [**Auto Forward Messages** ](http://t.me/Auto_Forward_Messages_Bot)bot, you can publish content using three powerful automation modes:

#### 1. **Interval Mode**

* Repost messages at fixed time intervals (minutes)
* Example: Repost every 15 minutes, 30 minutes, 1 hour, etc.

#### 2. **Fixed Time Mode**

* Repost messages at specific times
* Example: Post at 10:00 on December 25, 2025

#### 3. **Repeat Mode** ⭐

* Repost messages according to recurring schedules
* Supports daily, weekly, monthly, or custom repetition



This guide walks you through both scheduling methods in detail—helping you automate your Telegram workflow with precision and control. **Since this is a powerful feature with many flexible options, the article may be a bit long—but it’s well worth it if you want to master this tool like a pro.**

{% embed url="https://youtu.be/6dwzfSJwMZM" %}

***

**Why You Should Schedule Telegram Message Posting?**

Telegram currently doesn’t support automatic scheduling for forwarding messages between chats. In other words, if you want to schedule Telegram message posting—from one group, channel, or chat to another—you’d have to do it manually each time.\
\
That’s exactly when the **Auto Forward Messages bot** unleashes its full potential—empowering you to automate what Telegram alone cannot. It lets you:

* Automatically deliver selected messages without lifting a finger
* Loop important updates on a repeating schedule
* Fully control the timing, sequence, and delay between forwards

😉 **Imagine this:** you prepare a single message—or multiple messages—in advance and send them into your source chat. Then simply set the schedule for exactly midnight. When 00:00 arrives, the bot automatically posts your messages to your channels or groups. You don’t have to stay up or do anything manually—it all happens while you sleep.

***

### 🔁 Interval Mode – Schedule Telegram Message Posting Repeatedly

**What It Does?**

Interval Mode allows you to schedule Telegram message posting at fixed time intervals—such as every few minutes or hours. Once activated, it runs continuously until you manually stop the task.

This is ideal for reposting rotating content, automated reminders, or looping marketing messages without interruption.

**How to Set Up Interval Scheduling**

#### **1.** **Open Your Task**

Launch the Auto Forward for Telegram app and choose the task you want to automate.

#### **2.** **Scroll to Auto Post Scheduler**

Inside the task settings, tap on **“Auto Post Scheduler”**.<br>

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting1.webp" alt="schedule Telegram message posting" width="188"><figcaption></figcaption></figure>

#### **3.** **Enable Auto Posting Mode**

Switch the toggle **ON** to activate scheduled message posting.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting2.webp" alt="schedule Telegram message posting" width="188"><figcaption></figcaption></figure>

#### **4.** **Select Interval Mode**

From the dropdown menu, choose **“Interval”** mode to begin setting your repeated schedule.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting3.webp" alt="schedule Telegram message posting" width="188"><figcaption></figcaption></figure>

#### **5.** **Set Posting Frequency**

In the **“Post every”** field, enter how often the bot should send a message.

Example: Enter `1` to post every **1 minute**, or `5` to post every **5 minutes** to your target chats.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting4.webp" alt="" width="188"><figcaption></figcaption></figure>

#### 6. Schedule Start Time (Interval Mode)

**Schedule Start Time** allows users to set a specific future date and time when the interval-based auto-posting will begin. Before this time, the task remains inactive even if enabled.

<figure><img src="../.gitbook/assets/image (1).png" alt="" width="434"><figcaption></figcaption></figure>

**Key Features**

* Set future start date & time for interval mode
* Task waits until scheduled time before starting
* Stored as Unix timestamp (milliseconds)
* Optional feature - can be enabled/disabled

**Use Cases**

**Example 1: Launch Campaign at Specific Time**

```
Schedule Type: Interval (post every 15 minutes)
Start Time: Tomorrow 9:00 AM
→ Task activates tomorrow at 9:00 AM, then posts every 15 minutes
```

**Benefits**

* **Precision**: Exact time control for campaigns
* **Automation**: No manual activation needed
* **Flexibility**: Can be enabled/disabled anytime
* **Planning**: Schedule tasks in advance

#### **7.** **Enter Message IDs**

In the **“Message ID(s)”** field, specify the message(s) to be posted.\
You have several options:

* Enter a single ID (e.g., 3) to automatically post that message every (X) minutes
* Enter multiple message IDs separated by commas (e.g., 1,3,5) to randomly post one of them every (X) minutes — for example, one of those three will be picked and sent to your target chats at each interval.
* Enter **0** to automatically fetch and post the **latest message** from your source chat every (X) minutes.

**Tips:** To get a message ID, copy its Telegram link and use the number at the end of the URL.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting5.webp" alt="" width="188"><figcaption></figcaption></figure>

#### 8. **Posting Order**

The **Posting Order** setting controls how messages are selected when you have multiple Message IDs. This feature is **only available in Interval Mode**.

**All (Send All Messages at Once) ⭐**

* **All messages are posted at once** in a single posting cycle
* Each message is sent with a configurable **delay between messages** to avoid spam
* **Default delay**: 1 second (if not specified)
* **Use case**: When you want to broadcast multiple messages together as a batch
* **Example**: If you have Message IDs `100,200,300` with a 5-second delay:
  * 10:00:00 → Message 100 is posted
  * 10:00:05 → Message 200 is posted
  * 10:00:10 → Message 300 is posted

**Delay Between Messages** (All Mode Only):

* When using **All** posting order, an additional input field appears
* Enter the delay time in **seconds** between each message
* **Minimum**: 1 second (default if left empty)
* **Recommended**: 3-10 seconds to avoid Telegram rate limits
* This prevents your messages from being flagged as spam

**Random Order**

* Messages are posted in random sequence
* Each posting cycle selects a random message from your Message ID list
* **Use case**: Create variety and unpredictability in your posts
* **Example**: If you have Message IDs `100,200,300`, the posting sequence might be: 200 → 100 → 300 → 200 → 100...

**Sequential Order**

* Messages are posted in the exact order you entered them
* Cycles through the list from first to last, then repeats
* **Use case**: When message order matters (e.g., storytelling, tutorials, sequential announcements)
* **Example**: If you have Message IDs `100,200,300`, the posting sequence will always be: 100 → 200 → 300 → 100 → 200 → 300...

#### **9.** **Advanced Settings** (optional but recommended)

* **Pause Real-Time Forwarding** (Default: ON): When enabled, this setting pauses real-time message forwarding while scheduled posting is active. This prevents message duplication or overlap.
* **Delay Between Targets**: If your task is sending to multiple target chats, you can avoid spam detection by introducing a delay between each message. For example, setting 6 will pause **6 seconds** between messages sent to different target chats.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting6.webp" alt="" width="188"><figcaption></figcaption></figure>

#### **10. Save and Activate**

Once everything is set, tap **`Done`** to save your configuration. You’ll receive a confirmation, and the schedule will start running immediately.

#### **What to Expect**

The Auto Forward Messages bot will now schedule Telegram message posting based on the frequency and message IDs you configured. Messages will be delivered repeatedly—rotating as needed—until you turn off or modify the task.

### 🕰️ Fixed Time Mode – Schedule Telegram Message Posting at Exact Times

**What It Does?**

Fixed Time Mode allows you to schedule Telegram message posting at **specific hours and minutes**—with precision down to the second—on the current day or any future date. This is perfect for broadcasting messages that need to go out **on time**, such as breaking news, time-sensitive alerts, or coordinated campaign drops.

**How to Set Up Fixed-Time Scheduling**

#### **1. Switch to Fixed Time Mode**

Inside the Auto Post Scheduler, choose **“Fixed Time”** from the dropdown menu.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting7b.webp" alt="" width="188"><figcaption></figcaption></figure>

#### **2. Set Exact Time and Message ID**

For each time slot, define both:

* The exact time you want the message to post (e.g., 12:53 PM).
* ID `0` tells the bot to fetch the **latest** message from the source chat.
* Tap the **`Add Schedule`** to create one or more posting schedules.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting8b.webp" alt="schedule Telegram message posting" width="188"><figcaption></figcaption></figure>

#### **3.** **Add Scheduled Time Slots**

Example schedule:

**12:53 PM** → ID **0** (latest message)

**12:54 PM** → ID **3**

**12:55 PM** → ID **5**

**12:58 PM** → ID **7**\
\
Note:

**To edit** any existing time slot, simply tap on the time entry you want to modify.

**To delete** a scheduled time slot, tap the red remove icon at the end of the item.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting9.webp" alt="schedule Telegram message posting" width="188"><figcaption></figcaption></figure>

#### 3. **Posting Order**

The **Posting Order** setting controls how messages are selected when you have multiple Message IDs. This feature is **only available in Interval Mode**.

**All (Send All Messages at Once) ⭐**

* **All messages are posted at once** in a single posting cycle
* Each message is sent with a configurable **delay between messages** to avoid spam
* **Default delay**: 1 second (if not specified)
* **Use case**: When you want to broadcast multiple messages together as a batch
* **Example**: If you have Message IDs `100,200,300` with a 5-second delay:
  * 10:00:00 → Message 100 is posted
  * 10:00:05 → Message 200 is posted
  * 10:00:10 → Message 300 is posted

**Delay Between Messages** (All Mode Only):

* When using **All** posting order, an additional input field appears
* Enter the delay time in **seconds** between each message
* **Minimum**: 1 second (default if left empty)
* **Recommended**: 3-10 seconds to avoid Telegram rate limits
* This prevents your messages from being flagged as spam

**Random Order**

* Messages are posted in random sequence
* Each posting cycle selects a random message from your Message ID list
* **Use case**: Create variety and unpredictability in your posts
* **Example**: If you have Message IDs `100,200,300`, the posting sequence might be: 200 → 100 → 300 → 200 → 100...

**Sequential Order**

* Messages are posted in the exact order you entered them
* Cycles through the list from first to last, then repeats
* **Use case**: When message order matters (e.g., storytelling, tutorials, sequential announcements)
* **Example**: If you have Message IDs `100,200,300`, the posting sequence will always be: 100 → 200 → 300 → 100 → 200 → 300...

#### **4. Advanced Settings (Optional but Recommended)**

Identical to Interval Mode, but with one additional option.

* **Resume Real-Time Forwarding After Schedule Ends** (Default: ON): Once all fixed-time posts for the day are complete, this setting automatically resumes real-time forwarding. This is especially useful if you want the bot to pause real-time activity during high-priority scheduled posts, and then continue normal forwarding behavior afterward.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting10.webp" alt="schedule Telegram message posting" width="188"><figcaption></figcaption></figure>

#### **5.** **Save and Activate**

After adding all desired time slots and configuring settings, tap **“Done”** to save the task. Your bot will immediately begin scheduling posts based on your setup.

**What to Expect**

The Auto Forward Messages bot will now schedule Telegram message posting precisely at the defined times. Each message will go out **exactly when planned**, making this mode ideal for:

* Publishing breaking news at scheduled peak times.
* Running coordinated global campaigns across time zones.
* Executing strategic content drops during high-engagement windows.
* Replacing manual reminders with timed automation

**⏰ Important: Timezone Awareness**

Scheduled posts will follow the **timezone of the Telegram account connected to the Auto Forward Messages bot** — not your device’s timezone.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting11.webp" alt="schedule Telegram message posting" width="188"><figcaption></figcaption></figure>

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting12.webp" alt="schedule Telegram message posting" width="188"><figcaption></figcaption></figure>

If your connected account is **set to GMT+7**, for example, all scheduled times will **follow GMT+7 exactly**.

This means:

* ⚠️ Even if your phone or PC is in a different time zone, the schedule won’t adjust automatically.
* ✅ To ensure messages are delivered at the right time, set your Auto Forward account’s time zone to match the target region.

This is especially important for time-sensitive posts sent to international groups.\
\
If all your chats share the same time zone, set the account accordingly. If you manage groups across multiple time zones, choose the time zone that best fits your main audience.

### 🕰️ Repeat Schedule Feature User Guide

### Overview

The **Repeat Schedule** feature allows you to automatically repost messages according to recurring schedules. This is a powerful feature that helps you maintain posting activities automatically and in a planned manner.

***

### How to Use Repeat Mode

#### Step 1: Enable the Feature

1. Open the **Task** you want to set up scheduled posting for
2. Find and enable the **Auto Post Schedule** toggle
3. Select **Schedule Type** → **Repeat**

<figure><img src="../.gitbook/assets/image (4).png" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (5).png" alt="" width="375"><figcaption></figcaption></figure>

#### Step 2: Set Up Repeat Schedule

**2.1. Select Time**

* Tap the **time picker** button to open the time selector
* Choose the hour and minute you want to post the message
* Example: 09:00, 14:30, 18:00

**2.2. Enter Message ID**

* Enter the **Message ID** of the message you want to repost
* Supports multiple Message IDs, separated by commas
* Example: `123` or `123,456,789`

**2.3. Choose Repeat Mode**

The system provides 4 repeat modes:

**a) Daily**

* Messages will be reposted every day at the selected time
* Example: Post every day at 09:00 AM

**b) Weekly**

* Select the days of the week you want to post
* You can select one or multiple days:
  * **Sun** (Sunday)
  * **Mon** (Monday)
  * **Tue** (Tuesday)
  * **Wed** (Wednesday)
  * **Thu** (Thursday)
  * **Fri** (Friday)
  * **Sat** (Saturday)
* Example: Post on **Monday, Wednesday, Friday** at 14:00

**c) Monthly**

* Select the day of the month (1-31) you want to post
* Messages will be posted on that day every month
* Example: Post on **the 15th** of every month at 10:00

⚠️ **Note**: If you select days 29, 30, or 31, months without those days will be skipped

**d) Custom**

* Set custom repeat intervals (number of days)
* Examples:
  * Repeat every **2 days** (every other day)
  * Repeat every **3 days**
  * Repeat every **7 days** (equivalent to weekly)

#### Step 3: Add Repeat Schedule

1. After completing the setup, tap the **Add** button
2. The new repeat schedule will appear in the list
3. You can add multiple different repeat schedules

<figure><img src="../.gitbook/assets/image (6).png" alt="" width="375"><figcaption></figcaption></figure>

#### Step 4: Manage Repeat Schedules

**Edit**

* Tap the **Edit icon** (pen symbol) next to the repeat schedule
* Change the necessary information
* Tap **Update** to save changes

**Delete**

* Tap the **Delete icon** (trash can symbol)
* Confirm deletion in the dialog

#### Step 5: Additional Settings

**Pause Forwarding During Post**

* Enable to pause message forwarding while scheduled posting is in progress
* Avoids conflicts between forwarding and scheduled posting

**Resume Forwarding After Post**

* Enable to automatically resume forwarding after completing scheduled posting
* Only applies to **Fixed Time** and **Repeat Mode**

**Delay Target**

* Set the wait time (seconds) between posts to different targets
* Avoid spam and violating Telegram's limits
* **Recommended**: 4-10 seconds

#### Step 5. **Posting Order**

The **Posting Order** setting controls how messages are selected when you have multiple Message IDs. This feature is **only available in Interval Mode**.

**All (Send All Messages at Once) ⭐**

* **All messages are posted at once** in a single posting cycle
* Each message is sent with a configurable **delay between messages** to avoid spam
* **Default delay**: 1 second (if not specified)
* **Use case**: When you want to broadcast multiple messages together as a batch
* **Example**: If you have Message IDs `100,200,300` with a 5-second delay:
  * 10:00:00 → Message 100 is posted
  * 10:00:05 → Message 200 is posted
  * 10:00:10 → Message 300 is posted

**Delay Between Messages** (All Mode Only):

* When using **All** posting order, an additional input field appears
* Enter the delay time in **seconds** between each message
* **Minimum**: 1 second (default if left empty)
* **Recommended**: 3-10 seconds to avoid Telegram rate limits
* This prevents your messages from being flagged as spam

**Random Order**

* Messages are posted in random sequence
* Each posting cycle selects a random message from your Message ID list
* **Use case**: Create variety and unpredictability in your posts
* **Example**: If you have Message IDs `100,200,300`, the posting sequence might be: 200 → 100 → 300 → 200 → 100...

**Sequential Order**

* Messages are posted in the exact order you entered them
* Cycles through the list from first to last, then repeats
* **Use case**: When message order matters (e.g., storytelling, tutorials, sequential announcements)
* **Example**: If you have Message IDs `100,200,300`, the posting sequence will always be: 100 → 200 → 300 → 100 → 200 → 300...

#### Step 6: Save Settings

1. Review all information
2. Tap the **Update** button to save the configuration
3. The system will notify you when saved successfully

**⏰ Important: Timezone Awareness**

Scheduled posts will follow the **timezone of the Telegram account connected to the Auto Forward Messages bot** — not your device’s timezone.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting11.webp" alt="schedule Telegram message posting" width="188"><figcaption></figcaption></figure>

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/schedule-telegram-message-posting12.webp" alt="schedule Telegram message posting" width="188"><figcaption></figcaption></figure>

If your connected account is **set to GMT+7**, for example, all scheduled times will **follow GMT+7 exactly**.

This means:

* ⚠️ Even if your phone or PC is in a different time zone, the schedule won’t adjust automatically.
* ✅ To ensure messages are delivered at the right time, set your Auto Forward account’s time zone to match the target region.

This is especially important for time-sensitive posts sent to international groups.\
\
If all your chats share the same time zone, set the account accordingly. If you manage groups across multiple time zones, choose the time zone that best fits your main audience.

***

### Real-World Examples

#### Example 1: Post daily at 8:00 AM

```
- Time: 08:00
- Message ID: 123
- Repeat Type: Daily
```

→ Message ID 123 will be posted every day at 8:00 AM

#### Example 2: Post on Monday, Wednesday, Friday

```
- Time: 14:00
- Message ID: 456,789
- Repeat Type: Weekly
- Days: Mon, Wed, Fri
```

→ Messages ID 456 and 789 will be posted on Monday, Wednesday, Friday at 14:00

#### Example 3: Post on the first day of every month

```
- Time: 09:00
- Message ID: 111
- Repeat Type: Monthly
- Day of Month: 1
```

→ Message ID 111 will be posted on the 1st of every month at 09:00

#### Example 4: Post every 3 days

```
- Time: 18:00
- Message ID: 222,333
- Repeat Type: Custom
- Repeat Interval: 3
```

→ Messages ID 222 and 333 will be posted every 3 days at 18:00

***

### Important Notes

#### ⚠️ Limits & Rules

1. **Message ID must be valid**
   * Only accepts integers
   * Multiple IDs separated by commas
   * Valid examples: `123` or `123,456,789`
2. **Time must be selected**
   * Cannot be empty
   * Use the time picker to select accurately
3. **Weekly Mode**
   * Must select at least 1 day of the week
   * Can select multiple days
4. **Monthly Mode**
   * Only select days from 1-31
   * Days 29, 30, 31 may be skipped in some months
5. **Custom Mode**
   * Interval must be ≥ 1 day
   * Cannot be empty

#### 🔒 System Requirements

* Bot must be running (not stopped)
* Account must have active VIP subscription (if this is a premium feature)
* Task must be in active status

#### 💡 Usage Tips

1. **Avoid duplicates**: Don't create multiple repeat schedules with the same time
2. **Check Message ID**: Ensure Message ID exists in the source
3. **Reasonable delay**: Set delay to 5-10 seconds if you have multiple targets
4. **Test first**: Try with 1-2 schedules before expanding
5. **Monitor**: Check logs to ensure proper operation

#### ❌ Common Errors

| Error                                | Cause                            | Solution                                |
| ------------------------------------ | -------------------------------- | --------------------------------------- |
| "Please select time"                 | Time not selected                | Select time from picker                 |
| "Please enter message ID"            | Message ID empty                 | Enter valid Message ID                  |
| "Invalid message ID format"          | Wrong format                     | Only enter numbers, separated by commas |
| "Please select at least one day"     | Weekly mode with no day selected | Select at least 1 day                   |
| "Repeat interval must be at least 1" | Custom interval < 1              | Set interval ≥ 1                        |

***

### Frequently Asked Questions (FAQ)

#### FAQs

**Q: Can I use both Interval and Fixed Time modes together?**\
No. Each task must use either Interval Mode or Fixed Time Mode, not both at the same time. If you need both, create two separate tasks.

**Q: Can I schedule messages from different chats?**\
Yes, as long as your personal Telegram account has access to the source chats. However, since this feature works best for scheduled announcements, we recommend creating a dedicated source chat to organize and manage the messages you plan to schedule.

Additionally, make sure the message IDs you use for scheduling come from the source chats you added to the task. The bot can only auto-post messages if their IDs belong to chats already defined as source chats within that specific task.

**Q: Do I need to keep my device online after scheduling?**\
No, you don’t need to keep your device online. Once your schedule is configured, the Auto Forward Messages bot takes care of everything automatically—even if your phone or computer is offline. All logic is handled on the bot side.

**Q. How many repeat schedules can I create?**

There is no limit on the number of repeat schedules. However, keep it at a reasonable level for easier management.

**Q. Do repeat schedules automatically stop?**

No, repeat schedules will run continuously until you turn off the Task or delete the schedule.

**Q. Can I use multiple Message IDs?**

Yes, enter multiple IDs separated by commas. Example: `123,456,789`

**Q. What if I select day 31 for monthly repeats?**

Months without day 31 will be automatically skipped (February, April, June, September, November).

**Q. Can I combine multiple modes?**

No, each Task can only use 1 mode: Interval, Fixed Time, or Repeat.

**Q. How do I know if the schedule is running?**

Check the logs or posting history in the Task.

**Q. Can I pause repeat schedules?**

Yes, turn off the **Auto Post Schedule** toggle or stop the Task.

**Q. How is the timezone calculated?**

The system uses the timezone configured in your account settings.

