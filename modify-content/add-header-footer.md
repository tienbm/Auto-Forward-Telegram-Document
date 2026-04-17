---
description: >-
  Want to customize your Telegram auto-forwarded messages with extra context,
  branding, or call-to-actions? With the Auto Forward...
icon: heading
---

# Add Header / Footer

{% hint style="info" %}
You can add a header or footer for each post when forward to channels target
{% endhint %}

{% hint style="success" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

{% embed url="https://youtu.be/9njoEAe5a78" %}

### How to add Header - Footer use  App/Web

<figure><img src="../.gitbook/assets/image (252).png" alt=""><figcaption></figcaption></figure>

#### What Are Headers and Footers in Telegram Forwarded Messages?

* **A Header** appears **before** the forwarded message. It’s perfect for labels, sources, or attention-grabbers.
* **A Footer** appears **after** the message. It’s ideal for links, time stamps, disclaimers, or emojis.

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/telegram-forwarded-messages-header-footer1.webp" alt="Customize Telegram Forwarded Messages Easily" width="375"><figcaption></figcaption></figure>

These two blocks work independently but can be combined to elevate your message presentation.

***

#### 1️⃣ Add a Header to Make Messages More Understandable

A **header** appears **before** your original message. This is perfect for labeling content—like announcements, reminders, or alerts.

**How to Set It:**

1. Open your existing forwarding task
2. Scroll to the **Header** section
3. Type your custom content
4. Tap **Done**

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/telegram-forwarded-messages-header-footer2.webp" alt="Customize Telegram Forwarded Messages Easily" width="375"><figcaption></figcaption></figure>

**Example Header:**

```
📢 New Update:
```

When someone sends a message like:

```
We’ll have maintenance at 10PM UTC.
```

Your target chat will receive:

```
📢 New Update:

We’ll have maintenance at 10PM UTC.
```

You just made the message more readable and clearly tagged its purpose.

#### 2️⃣ Add a Footer with Extra Info or Links

A **footer** appears **after** your message. It’s ideal for contact links, disclaimers, or just a nice wrap-up.

**How to Set It:**

1. In your task, go to the **Footer** section
2. Write your content, using line breaks (`\n`) for clarity
3. Tap **Done**

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/telegram-forwarded-messages-header-footer3.webp" alt="" width="375"><figcaption></figcaption></figure>

**Example Footer:**

```
Need help? Contact us: t.me/abc
```

Now if someone forwards a message:

```
Here’s the weekly report link.
```

It will show like:

```
Here’s the weekly report link.

Need help? Contact us: t.me/abc
```

Perfect for support teams or help desks.

#### ✨ Use Shortcodes

If you’re running a crypto signals group or sharing on-chain alerts, shortcodes make your formatting dynamic and automatic.

**What Are Shortcodes?**

Shortcodes are special tags that get replaced automatically in forwarded messages.

**How to Use:**

1. Go to Header or Footer section
2. Tap **“Add Shortcode”**
3. Choose what you want
4. Insert into your text and save

<figure><img src="https://blog.autoforwardtelegram.com/wp-content/uploads/2025/07/telegram-forwarded-messages-header-footer4.webp" alt="" width="375"><figcaption></figcaption></figure>

{% tabs %}
{% tab title="Shortcode Explained" %}
📖 Some formats you can refer to:

#### 🔧 Formatting Helpers

* **EMPTY** – Use this if you don’t want to show the header.
* **\n** – Line break.
* &#x20;**\t** – Add a tab space (horizontal spacing).

***

#### 🧾 Message Content

* **\[\[ORIGIN\_TEXT]]** – The full content of the original message.
* **\[\[ORIGIN\_QUOTED\_TEXT]]** – A quoted preview or snippet from the original post.
* **\[\[ORIGIN\_DESCRIPTION]]** – Description of the original channel or group.

***

#### 👤 Sender Information

* **\[\[ORIGIN\_USERNAME]]** – Username of the original sender (if available).
* **\[\[ORIGIN\_USERID]]** – Telegram User ID of the original sender.
* **\[\[ORIGIN\_NAME]]** – Full name of the sender or the original channel name.
* **\[\[FROM\_USER]]** – Username of the user who forwarded the message.
* **\[\[SENDER\_CHAT]]** – Display name of the sender (can be user or chat).
* **\[\[FORWARD\_FROM\_CHAT]]** – Name of the original message owner or source channel.

***

#### 🕒 Time & Date

* **\[\[CURRENT\_TIME]]** – Current system time (HH:MM:SS).
* **\[\[CURRENT\_DATE]]** – Current date (DD/MM/YYYY).
* **\[\[CURRENT\_DATETIME]]** – Full current date and time.
* **\[\[CURRENT\_TIMESTAMP]]** – Current Unix timestamp.
* **\[\[ORIGIN\_POST\_TIME]]** – Time the original post was created.
* **\[\[ORIGIN\_POST\_DATE]]** – Original post creation date (raw).
* \[\[ORIGIN\_POST\_DATE\_FORMATTED]] – Formatted post date.
* **\[\[ORIGIN\_POST\_DATETIME]]** – Full date and time of the original post.

***

#### 📎 Post Metadata

* **\[\[ORIGIN\_POST\_ID]]** – Message ID of the original post.
* **\[\[ORIGIN\_CHAT\_ID]]** – Chat ID where the original post came from.
* **\[\[MESSAGE\_ID]]** – ID of the current message.
* **\[\[REPLY\_TO\_MESSAGE\_ID]]** – ID of the message this one is replying to.
* **\[\[IS\_FORWARD]]** – Whether the message is a forward (true / false).
* **\[\[IS\_REPLY]]** – Whether the message is a reply (true / false).
* **\[\[MESSAGE\_LINK]]** – Direct link to the original or forwarded message.

***

#### 📡 Chat Information

* **\[\[CHAT\_TYPE]]** – Type of chat (PRIVATE, GROUP, CHANNEL, etc.).
* **\[\[CHAT\_USERNAME]]** – Username of the chat (if public).
* **\[\[CHAT\_MEMBERS\_COUNT]]** – Number of members in the chat.
* **\[\[SOURCE\_NAME]]** – Name of the forward source (if available).
* **\[\[ORIGIN\_NAME\_URL]]** – Hyperlinked name of the original source.

***

#### 📂 Media Information

* **\[\[MEDIA\_TYPE]]** – Type of attached media (photo, video, document, etc.).
* **\[\[FILE\_SIZE]]** – File size (formatted).
* **\[\[FILE\_NAME]]** – File name.
* **\[\[HAS\_MEDIA]]** – Whether the message contains media (true / false).

***

#### 📊 Message Stats

* **\[\[VIEW\_COUNT]]** – Number of views (for public channel posts).
* **\[\[FORWARD\_COUNT]]** – Number of times the message was forwarded.
* **\[\[REACTIONS\_COUNT]]** – Total number of reactions (if any).

***

#### ✏️ Text Analysis

* **\[\[WORD\_COUNT]]** – Number of words in the message.
* **\[\[CHAR\_COUNT]]** – Number of characters.
* **\[\[LINE\_COUNT]]** – Number of lines.
* **\[\[TEXT\_LENGTH]]** – Length of the text (same as character count in most cases).

***

#### 🔍 Content Extraction

* **\[\[HASHTAGS]]** – All hashtags found in the message.
* **\[\[MENTIONS]]** – All mentioned usernames (@user).
* **\[\[URLS]]** – All URLs found in the message.

***

#### 🎲 Randomization

* **\[\[RANDOM\_EMOJI]]** – A random emoji from a predefined collection.
* **\[\[RANDOM\_NUMBER]]** – A random number between 1–1000.


{% endtab %}
{% endtabs %}

**Example Footer for Traders:**

```
📈 Source: [[SENDER_CHAT]]  
🕒 Time: [[CURRENT_TIME]]
```

So when a message is sent in your source group/channel, like:

```
Long BTC at $29,800  
TP: $31,000 | SL: $29,000
```

Your target group/channel will receive it like this:

```
Long BTC at $29,800  
TP: $31,000 | SL: $29,000  

📈 Source: @VIPTradeSignals  
🕒 Time: 17:07:48
```

No need to manually tag anything—it updates itself every time.

### Auto-Hide Header When Content is Empty

If the forwarded message has no content, the header will now be automatically hidden.

This keeps your messages clean and professional – no more awkward blank blocks!

**How to Set It:**

1. Open your existing forwarding task
2. Scroll to the **Header** section
3. At Add Header/Footer turnon Hide when empty
4. **Click Done**

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

***

### Random Header/Footer

Make your messages more dynamic and natural!\
You can now set multiple header or footer templates, and AutoForward will randomly pick one for each forwarded message.\
Ideal for marketing, engagement, and avoiding repetitive content

**How to Set It:**

1. Open your existing forwarding task
2. Scroll to the **Header** section
3. At Add Header/Footer enter content then click Random

<figure><img src="../.gitbook/assets/image (256).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (257).png" alt=""><figcaption></figcaption></figure>

**Finaly Click Done.**

***

