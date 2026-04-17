---
icon: puzzle-piece
---

# Dialog Broadcast

### Overview

Dialog Broadcast automatically sends messages from a source chat to multiple target chats on a customized schedule. Perfect for daily announcements, scheduled content distribution, and automated campaigns.

#### What It Does

* Pulls messages from a designated source chat
* Broadcasts to multiple targets (groups, channels, contacts, custom selections)
* Sends on your specified days and times
* Handles rate limiting and errors automatically
* Supports specific message IDs or always uses latest message

#### Key Benefits

✅ **Scheduled distribution** - Set it and forget it\
✅ **Multiple targets** - Reach all your audiences at once\
✅ **Rate limiting protection** - Auto-retry on Telegram limits\
✅ **Flexible timing** - Multiple broadcasts per day\
✅ **Error handling** - Skip failed targets, continue broadcasting

***

### Getting Started

#### Prerequisites

1. ✅ Purchase Dialog Broadcast addon
2. ✅ Have an active forwarding task with targets
3. ✅ Know which chat to use as message source

#### Quick Setup

**Step 1: Purchase & Enable**

1. Menu → My Addons → Dialog Broadcast → Unlock
2. Open your task settings
3. Find **Dialog Broadcast Settings** section
4. Toggle **Enable Dialog Broadcast** to ON

**Step 2: Configure Source**

**Message Source**: Select the chat where messages originate

**Message IDs** (optional):

* Leave empty to always broadcast the latest message
* Or enter specific message IDs: `123,124,125`

**Step 3: Select Targets**

Choose **Target Types**:

* ☑️ **Groups** - Broadcast to group chats
* ☑️ **Channels** - Broadcast to channels
* ☑️ **Contacts** - Broadcast to individual users (high spam risk)
* ☑️ **Custom Targets** - Pick specific chats from task targets

**Exclude Targets**: Optionally blacklist specific chats

**Step 4: Set Schedule**

**Schedule Days**: Select days of the week (Mon-Sun)

**Schedule Times**: Add specific times

* Example: `09:00`, `14:00`, `20:00`
* Tap **Add Time** for multiple times per day

**Step 5: Configure Options**

**Delay Between Sends**: 5-600 seconds (recommended: 10-30s)\
**Max Targets Per Run**: 1-5000 (test with low numbers first)\
**Show Forward Header**: ON = shows "Forwarded from...", OFF = sends as new message\
**Retry on Flood**: ON (recommended) - auto-retry if rate limited\
**Skip on Error**: ON (recommended) - continue if some targets fail

**Step 6: Save & Monitor**

Tap **Save** and check your first scheduled broadcast time. Monitor results and adjust as needed.

***

### Configuration Details

#### Message Selection

**Latest Message Mode** (Message IDs empty):

* Bot checks source chat at scheduled time
* Broadcasts the most recent message
* Perfect for daily updates, news digests

**Specific Message IDs**:

* Enter IDs separated by commas: `100,101,102`
* Bot broadcasts these exact messages
* Perfect for fixed announcements, evergreen content

**Finding message IDs**:

* Desktop Telegram: Right-click message → Copy Message Link → ID is in the URL
* Mobile: Long press → Forward → See message ID in preview

#### Target Selection

**Groups**: All group chats in your task targets\
**Channels**: All channels (where you're admin)\
**Contacts**: Individual users (⚠️ minimum 30s delay enforced due to spam risk)\
**Custom Targets**: Hand-pick specific chats from task target list

**Exclude Targets**: Blacklist specific chats that shouldn't receive broadcasts

#### Schedule Configuration

**Days**: Select one or more days. Broadcasts only happen on selected days.

**Times**: Add multiple broadcast times:

* System uses your server timezone (UTC typically)
* Format: HH:MM (24-hour format)
* Example: `09:00` = 9:00 AM, `21:30` = 9:30 PM
* Add as many times as you need per day

**How it works**: Each selected day at each scheduled time, the bot triggers a broadcast run.

#### Advanced Options

**Delay Between Sends**:

* Pause in seconds between each target
* Range: 5-600 seconds
* **Recommended**: 10-30s (balances speed and safety)
* **Contacts**: Minimum 30s enforced automatically

**Max Targets Per Run**:

* Limits how many targets receive broadcast per trigger
* Range: 1-5000
* Use for testing (set to 5-10) or gradual rollout
* Prevents overwhelming your bot

**Retry on Flood**:

* When ON: Bot auto-retries if Telegram rate limits hit
* **Recommended**: Always ON for reliability

**Skip on Error**:

* When ON: If one target fails, bot continues to next target
* When OFF: Stops broadcast on first error
* **Recommended**: ON for maximum delivery

***

### Common Use Cases

#### Daily News Digest

**Setup**:

```
Source: Your news aggregation private channel
Message IDs: Empty (use latest)
Target Types: Channels, Groups
Schedule: Mon-Fri at 08:00
Delay: 15s, Max Targets: 100
```

Every weekday at 8 AM, broadcasts latest compiled news.

#### Weekly Announcement

**Setup**:

```
Source: Admin announcements channel
Message IDs: Specific message ID (doesn't change)
Target Types: Groups only
Schedule: Monday at 09:00
Delay: 20s
```

Same announcement every Monday to all groups.

#### Multi-Time Campaign

**Setup**:

```
Source: Marketing channel
Message IDs: Three campaign message IDs
Target Types: Custom targets (selected premium groups)
Schedule: Mon-Fri at 10:00, 14:00, 18:00
Delay: 30s, Max Targets: 50
```

Broadcasts 3 marketing messages, 3 times per day to selected audiences.

***

### Troubleshooting

#### Issue: Nothing Broadcasting

**Check**:

* [ ] Dialog Broadcast is enabled in task settings
* [ ] At least one schedule day selected
* [ ] At least one time added
* [ ] Source chat selected
* [ ] Target types selected
* [ ] Current time matches your bot's timezone

**Fix**: Verify each checkbox above. Test with a time 5 minutes from now.

***

#### Issue: Some Targets Not Receiving

**Possible causes**:

* Max Targets Per Run is too low
* Target excluded in Exclude Targets list
* Bot doesn't have permission in that target
* Target blocked your bot

**Fix**:

* Increase Max Targets
* Review Exclude list
* Verify bot permissions in target chats

***

#### Issue: Delay/Timing Issues

**Problem**: Broadcasts taking too long or hitting rate limits

**Solution**:

* Increase delay between sends (try 30s)
* Reduce max targets per run (try 50)
* Enable Retry on Flood
* For contacts, remember 30s minimum is enforced

***

#### Issue: Wrong Message Broadcast

**Check**:

* Are Message IDs correct?
* If using "latest", is correct message the latest in source?

**Fix**:

* Double-check message IDs (copy from Telegram)
* Test with specific message IDs first
* Verify source chat is correct

***

### Best Practices

#### Start Small

Test with 5-10 targets and one time first. Scale up after confirming it works.

#### Optimal Timing

* **News**: Early morning (7-9 AM)
* **Marketing**: Mid-day (12-2 PM) and evening (6-8 PM)
* **Announcements**: Start of business day (9-10 AM)

#### Safe Delays

* **Groups/Channels**: 10-30 seconds
* **Contacts**: 30-60 seconds minimum
* **High volume (100+ targets)**: 20-30 seconds

#### Use Latest Message for Dynamic Content

Leave Message IDs empty when broadcasting daily-changing content like news, updates, digests.

#### Use Specific IDs for Fixed Content

Enter Message IDs when broadcasting recurring announcements, promotions, evergreen content.

#### Monitor First Runs

Check your first few broadcasts manually to ensure:

* Correct message is sent
* All targets receive it
* Timing is correct
* No spam complaints

#### Combine with Other Addons

* **With Image Crop**: Broadcast clean images
* **With Button Clone**: Preserve CTAs in broadcasts
* **With content filters**: Clean and broadcast

***

### Frequently Asked Questions

#### Can I broadcast to unlimited targets?

Yes, but set reasonable Max Targets (50-100) and Delay (20-30s) to avoid rate limits.

#### What timezone are scheduled times in?

Server timezone (typically UTC). Test with a time 5 minutes from now to verify.

#### Can I broadcast different messages to different groups?

Not directly. Create separate tasks with different sources and target selections.

#### Does it work with media (photos, videos)?

Yes! Broadcasts whatever message type is in the source (text, photo, video, file, etc.).

#### What if source message is deleted?

If using specific message IDs and message is deleted, broadcast fails. If using latest message, bot broadcasts current latest message.

#### How do I stop broadcasts temporarily?

Toggle "Enable Dialog Broadcast" to OFF. Schedule and settings are preserved.

#### Can I test before going live?

Yes! Set Max Targets to 1-2, select your private channel as custom target, and test.

***

### Getting Help

If issues persist:

1. Check Addons FAQ for more Q\&A
2. Test in isolation (new task, 1 target, near-future time)
3. Contact support with:
   * Your schedule configuration
   * Expected vs actual behavior
   * Screenshots of settings

**Support**: Menu → Help & Support or support@autoforwardtelegram.com

***

### Summary

Dialog Broadcast automates scheduled message distribution:

✅ Set source + targets + schedule = automated broadcasts\
✅ Handles rate limiting and errors gracefully\
✅ Flexible timing with multiple times per day\
✅ Safe delays and limits to prevent spam flags\
✅ Test with small targets before scaling up

**Perfect for**: Daily digests, recurring announcements, marketing campaigns, scheduled updates.

***

**Last Updated**: March 2026\
**Addon Version**: 1.0\
**App Version**: 1.0.44+
