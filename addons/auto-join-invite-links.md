---
icon: puzzle-piece
---

# Auto Join Invite Links

### 🚀 Overview

Auto Join Invite Links allows your system to automatically join private Telegram groups or channels from invite links found in trusted source chats.

Instead of manually opening and joining each link, this addon handles it for you in real time.

👉 Perfect for automation workflows where invite links are frequently shared.

***

### ⚙️ How It Works

1. A new message arrives from a source chat
2. The system scans the message for private invite links
3. If a valid invite link is found:
   * The system checks whether the source chat is trusted
4. If the source is trusted → the bot will automatically join the linked group/channel

***

### ✅ Key Features

* 🔗 Automatically joins private invite links
* 🛡️ Works only with trusted source chats (you control this)
* ⚙️ Can be enabled or disabled per Forward Task
* 🎯 Reduces manual work when handling multiple invite links

### 🛡️ Trusted Sources

This is a key safety mechanism:

* The system will only join links from sources you explicitly allow
* Prevents unwanted joins from unknown or unsafe channels

👉 You stay in full control of where the bot can join.

***

### 📌 Behavior Notes

* Each task can have its own trusted sources
* If `trusted_sources` is empty → no links will be joined
* Works automatically without interrupting your forwarding workflow

***

### 🚫 Limitations

* ❗ Only works with private invite links
* ❗ Will not join links from untrusted sources
* ❗ Requires valid Telegram invite links

***

### 💡 Use Cases

#### 1. Signal / Alpha groups

Automatically join new private groups shared by trusted channels

***

#### 2. Community expansion

Quickly access new communities without manual actions

***

#### 3. Automation pipelines

Combine with auto-forward to build a fully automated content + access system

***

### 🎯 Recommendation

Use this addon if you:

* Follow channels that frequently share invite links
* Want to automate joining private groups
* Need a controlled and safe auto-join system
