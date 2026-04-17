---
description: >-
  The Sender Type defines which Telegram account or bot will be used to send
  messages for a specific task. You can choose between using your personal
  Telegram account or one or more Telegram bots.
icon: paper-plane-top
---

# Setup Sender For Task

{% hint style="success" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

{% embed url="https://youtu.be/LP0ess1ddc4" %}

#### 🧭 Sender Type Interface

When configuring the sender, you’ll be asked to choose:

*   **Personal Telegram Account**

    Use your own Telegram account to send messages
*   **Telegram Bot**

    Use a bot created via [@BotFather](https://t.me/BotFather) to send messages on your behalf.

***

## 🤖 Telegram Bot Options

### How to Create a Telegram Bot with BotFather

To use bots in your forwarding tasks, you must first create them through BotFather, the official Telegram bot management tool.

**📌 Steps to Create a Bot**

1.  **Open BotFather**

    Visit [@BotFather](https://t.me/BotFather) on Telegram.

<figure><img src="../.gitbook/assets/image (246).png" alt="" width="238"><figcaption></figcaption></figure>

1.  **Start the Bot**

    Click Start or type /start.
2.  **Create a New Bot**

    Send the command:

```
/newbot
```

<figure><img src="../.gitbook/assets/image (247).png" alt="" width="238"><figcaption></figcaption></figure>

3.  Choose a Bot Name

    BotFather will ask you to enter a display name (e.g., My AutoForward Bot).
4.  Set a Username

    Choose a unique username that ends with bot (e.g., my\_autoforward\_bot).\
    After that, choose a **unique username** that ends with **“bot”** (e.g., `myautofw1_bot`). Make sure the username isn’t already taken and doesn’t include any special characters.

<figure><img src="../.gitbook/assets/image (248).png" alt="" width="238"><figcaption></figcaption></figure>

3. Copy the Bot Token

After creation, BotFather will generate an API token.\
Copy it for the next step.

Once the bot is created, you’ll receive a token like this:

```
123456789:AAHkLmNnOOpPqQxYzZ_ExampleToken
```

<figure><img src="../.gitbook/assets/image (249).png" alt="" width="238"><figcaption></figcaption></figure>

6. Save this token securely — you’ll need it to connect the bot in your system.

***

**✅ Next Steps**

<figure><img src="../.gitbook/assets/image (224).png" alt="" width="375"><figcaption></figcaption></figure>

* Go to **Settings** at Home App -> **Bot Management** in your app
* Click “+ Add New Bot”

<figure><img src="../.gitbook/assets/image (229).png" alt="" width="375"><figcaption></figcaption></figure>

* Paste the token
* **Save and verify the connection**

***

### ⚡ Config Sender Type

<figure><img src="../.gitbook/assets/image (230).png" alt="" width="375"><figcaption></figcaption></figure>

**The Sender Type determines which Telegram identity will be used to forward messages in this task.**

You can choose between two options:

#### 1️⃣ Personal Telegram Account

Use your own Telegram account (already logged in) to send messages.

✅ Best for:

* Fast and direct forwarding
* Tasks requiring access to private or restricted chats

⚠️ Note:

Your account must remain logged in and not restricted by Telegram. Avoid using this mode if you plan to automate at large scale, as Telegram limits user accounts more strictly than bots.

***

**2️⃣ Telegram Bot**

Use one or more Telegram bots to send messages instead of your personal account.

✅ Best for:

* High-volume or automated tasks
* Running multiple tasks in parallel

There are two modes for using bots:

* **Single Bot**: Use a single bot for all messages
* **Bot by Strategy**: Let the system choose from multiple bots based on strategy (e.g., Last Used, Round Robin, Random, Weighted)
  * **Last Used:** The same bot that sent the most recent message will be reused for the next one. Messages are grouped under a single bot until you manually reset or change tasks.
  * **Round Robin:** Bots take turns in a fixed sequence. The system cycles through the list, assigning the next message to the next bot. This ensures even usage across all bots over time.
  * **Random:** For each message sent to the target chat, the system randomly picks one bot from your list to send that individual message. This means each message may be sent by a different bot, offering highly distributed traffic with no fixed order.
  * **Weighted:** Bots are assigned weights (e.g., 50%, 30%, 20%), and the system distributes messages based on those percentages. Bots with higher weights are used more often, giving you flexible control over load distribution.

👉 You can configure bots in Bot Management

⚠️ Important:

All bots must:

* Be connected via token
* Be added to target groups/channels
* Be promoted to Admin with Send Messages permission

***

**📝 How to Switch Sender Type**

<figure><img src="../.gitbook/assets/image (250).png" alt="" width="357"><figcaption></figcaption></figure>

1. Tap on Sender Type
2. Select either Personal Telegram Account or Telegram Bot
3. Choose the specific bot or bot strategy (if applicable)
4. **Tap Save**

***

#### Final Thoughts

The **Sender Type** feature in Auto Forward for Telegram is at the heart of how your messages are delivered — offering you flexibility, control, and reliability.

* **Use Personal Telegram Account** if you’re managing a small number of tasks, want a hassle-free setup, or are sending to chats that don’t require admin rights. It’s quick, simple, and effective for lightweight use.
* **Choose Telegram Bot** if you’re aiming for long-term automation, higher reliability, or more privacy in how messages are sent. Bots can handle larger volumes, reduce the risk of restrictions, and help you stay anonymous — perfect when forwarding VIP, premium, etc. Whether you’re managing multiple chats or distributing tasks across teams, bots offer the control and scalability personal accounts can’t.
* **Choose Bot by Strategy** when you need all the benefits of Telegram bots — flexibility, scalability, anonymity, and risk reduction — plus intelligent rotation across multiple bots to balance message load and ensure smooth delivery under pressure. This advanced option is ideal for large-scale automation or high-traffic environments where performance and reliability are critical.

