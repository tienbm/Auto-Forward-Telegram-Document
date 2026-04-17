# 📭 Bot Not Forwarding Messages – How to Troubleshoot

**📭 Bot Not Forwarding Messages – How to Troubleshoot**

If you notice that the bot isn’t forwarding messages as expected, don’t worry — this guide will walk you through the common causes and how to resolve them quickly.

***

### 🛠️ Step 1: Review All Active Filters and Rules

Before assuming there’s a bug, it’s important to check if the issue is caused by any filtering or automation features you’ve enabled.

Please carefully review the following:

**✅ Blacklist**

Blocks messages containing specific keywords, usernames, or content types.

➡️ Check if the message being blocked contains any blacklisted items.

**✅ Whitelist**

Allows the bot to forward only messages that match certain criteria.

➡️ Make sure the source of your message is on the allowed list.

**✅ Filters**

Filters can restrict message types such as:

• Only text

• Only media (photos/videos)

• Only forwarded messages

➡️ Ensure the filter settings are not too restrictive.

**✅ Cleaner**

Automatically deletes certain messages after they’re received.

➡️ This could remove messages before they are forwarded.

**✅ Rules (Custom Conditions)**

You may have defined rules that unknowingly exclude certain message types or sources.

➡️ Disable all rules temporarily to test if they are the cause.

**✅ Other Active Tasks**

Check whether other forwarding tasks are working properly.

➡️ If all tasks are failing, the issue may be global (e.g. network, bot permissions, or system-wide settings).

**✅ Source Group or Channel Type**

If your source chat is a large group or big channel, it may behave differently due to Telegram or Discord limitations.

➡️ In such cases, **try enabling Debug Mode in the app or web version** to see detailed logs and message handling behavior.

> ⚠️ Pro Tip: If you’re not sure which filter is causing the issue, try disabling all filters and rules. Then test if the bot works normally again.

***

## **Verify Source,Target ID is correct**

1. Search for the @**FindMyIDs\_Bot** on Telegram or access it via this [link](https://t.me/FindMyIDs_Bot).
2. Click **Start** to begin using the bot.

**Step 2: Forward a Message or Post**

![](https://docs-v2.autoforwardtelegram.com/~gitbook/image?url=https%3A%2F%2F3402573870-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FddnL4cgrrb4y0Pnwxc5r%252Fuploads%252FqEDSRwnyLZEBL701ounV%252Fimage.png%3Falt%3Dmedia%26token%3D9500163e-5b28-448a-b650-09d06142b586\&width=768\&dpr=3\&quality=100\&sign=e8293136\&sv=2)

* Forward a post or message containing special text formatting directly to the bot.

### 🧪 Step 2: Simulate the Problem in a New Test Setup

If the issue persists even with all filters and rules disabled, please help us investigate further by creating a new, clean test environment.

#### 🔧 What You Need to Do:

#### 1. Create a New Source Channel

• You can make it private and empty — just for testing.

#### 2. Create a New Target Channel

• Set it to public or private — either is fine.

#### **3. Setup a new Task Forward**

Create a simple forwarding task from Telegram Channel Source to the Telegram Channel Target.

{% content-ref url="../../guides/how-to-create-task-auto-forward.md" %}
[how-to-create-task-auto-forward.md](../../guides/how-to-create-task-auto-forward.md)
{% endcontent-ref %}

{% embed url="https://www.youtube.com/watch?v=DSCp3rvKXuE" %}

***

#### 📤 Step 3: Share the Following Info with [Admin](https://t.me/redf0x1)

Once you’ve set up the test environment, please send the following:

**• 👤 Your AutoForward UserID**

**• 🔗 Invitation link to the Telegram channel source and target**

**• 🔗 GRANT ACCESS AS ADMIN TO SUPPORT FIX BUG**

You can send this information directly to the [admin](https://t.me/redf0x1) via our support contact.

***

### 🧑‍💻 Step 4: Admin Will Help Troubleshoot

Once we receive your test setup and links, our team will:

• Verify bot connectivity

• Reproduce the issue

• Help identify the root cause

• Guide you through the fix (or apply it directly)

***

❓ Need Help?

If you need assistance during setup or have questions, don’t hesitate to contact our support team. We’re here to make sure your bot runs smoothly!
