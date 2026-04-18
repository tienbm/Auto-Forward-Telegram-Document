---
icon: puzzle-piece
---

# Recover Token from Linked Post

### 🚀 Overview

Recover Token from Linked Post solves a common issue in Crypto Mode:

❌ The current message does not contain a token\
✅ But the token exists in a linked post

This addon automatically:

* Detects links inside the message (text, caption, URL, text-link)
* Finds the linked post within the same Telegram channel
* Extracts the token from that post
* Continues forwarding using the recovered token

👉 This ensures you don’t miss signals just because the token isn’t in the current message

***

### ⚙️ How It Works

1. Crypto Mode attempts to extract a token from the current message
2. If no token is found → the addon is triggered
3. The system will:
   * Scan all links in the message
   * Identify linked posts in the same channel
   * Retrieve the content of the linked post
   * Extract the token from that content
4. If a token is found → it will be used for forwarding

***

### ✅ Key Features

* 🔗 Recover tokens from linked posts within the same channel
* 🧠 Automatic fallback when the current message has no token
* 📄 Supports multiple link sources:
  * Message text
  * Captions
  * URL entities
  * Text-link entities

***

### ⚠️ Requirements

This addon only works if:

* ✅ Contract Address Mode is enabled (`crypto_contract = true`)

If not enabled, the addon will not function.

### 💡 Use Cases

#### 1. Split signal content

* Message A: “Check this 👇” + link
* Message B (linked): contains the token\
  👉 The addon extracts the token from Message B

***

#### 2. Teaser-style posts

* Current message has no token
* Token is hidden in a previous/linked post\
  👉 No missed signals

***

#### 3. Clean content channels

* Channels intentionally avoid posting contracts directly\
  👉 Token can still be recovered from linked posts

***

### 🎯 Recommendation

This addon is especially useful if you:

* Follow crypto channels that rely on linked posts
* Want to avoid missing tokens due to incomplete messages
* Need higher accuracy in Crypto Mode
