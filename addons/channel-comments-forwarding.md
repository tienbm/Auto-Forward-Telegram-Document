---
description: >-
  The Channel Comments Forwarding Addon allows Auto Forward Messages to
  automatically forward comments from posts in a Telegram source channel.
icon: puzzle
---

# Channel Comments Forwarding

### Overview

The **Channel Comments Forwarding Addon** allows Auto Forward Messages to automatically forward comments from posts in a Telegram source channel.

Instead of sending comments as unrelated messages, the addon preserves their relationship with the original post:

**Source Post → Forwarded Target Post**

**Source Comment → Reply to the corresponding Target Post**

This makes it possible to synchronize both **channel content and the discussions around it**.

<figure><img src="../.gitbook/assets/image (343).png" alt=""><figcaption></figcaption></figure>

***

### How Telegram Channel Comments Work

Telegram channel comments are powered by a **Discussion Group** linked to the channel.

Your Telegram setup needs to follow this structure:

**Source Channel**\
↓\
**Linked Discussion Group**\
↓\
**Post Discussion / Comments**

When a Discussion Group is linked to a channel, Telegram creates a discussion thread for channel posts. Messages inside these threads appear as comments underneath the corresponding channel post.

Therefore, a Discussion Group must first be linked to your source channel before the addon can detect channel comments.

***

### Step 1 — Create Your Source Channel

If you don't already have a source channel:

1. Open Telegram.
2. Select **New Channel**.
3. Enter your channel name and details.
4. Choose **Public** or **Private**.
5. Finish creating the channel.

Make sure your Telegram account has the necessary administrator permissions for the channel.

***

### Step 2 — Create a Discussion Group

Next, create a Telegram group that will handle the discussions for your channel.

Go to:

**Telegram → New Group**

Create a group, for example:

**My Channel Discussion**

This group will later be linked to your Source Channel.

You don't need to manually forward posts to this group. Telegram handles the relationship automatically after the group is linked.

***

### Step 3 — Link the Discussion Group to the Source Channel

Open your Source Channel and navigate to:

**Channel Info → Edit / Manage Channel → Discussion**

Select:

**Add a Group**

Then select the Discussion Group created in the previous step.

Your structure should now be:

**Source Channel → Discussion Group**

Once successfully linked, Telegram can display comments underneath posts in your channel.

***

### Step 4 — Verify Channel Comments

Publish a **new test post** after linking the Discussion Group.

You should see a comment option underneath the post, such as:

**💬 Leave a comment**

Once users start commenting, it may appear as:

**💬 3 Comments**

Open the discussion and send a test comment.

For example:

**Channel Post**

> 🚀 New update is available!

**Comment**

> ↳ Amazing update! 🔥

If you can see the comment underneath the source post, your Telegram Discussion Group is configured correctly.

***

### Step 5 — Enable the Channel Comments Forwarding Addon

The comment forwarding functionality is provided through the separate **Channel Comments Forwarding Addon**.

Make sure the addon is **active on your account**.

Then configure your forwarding task normally:

**Source:** Source Channel\
**Target:** Target Channel / Group

Enable **Channel Comments Forwarding** for the task if the option is available in its settings.

> **Important:** The Discussion Group itself does not need to be configured as your normal forwarding source. Keep the **Channel** as the Source.

The addon will handle the relationship between the source channel post and its discussion comments.

<figure><img src="../.gitbook/assets/image (344).png" alt=""><figcaption></figcaption></figure>

***

### Step 6 — How Comments Are Forwarded

Suppose your source contains:

**SOURCE CHANNEL**

> 📢 New product released!
>
> 💬 3 Comments

With comments:

> ↳ Alice: Amazing! 😍\
> ↳ Bob: When will it be available?\
> ↳ Charlie: Great update! 🔥

Auto Forward Messages first forwards the channel post to your configured target.

When the addon detects the comments, the target will look like:

**TARGET**

> 📢 New product released!
>
> ↳ Alice: Amazing! 😍\
> ↳ Bob: When will it be available?\
> ↳ Charlie: Great update! 🔥

Each comment is sent as a **reply associated with the corresponding forwarded post**.

The mapping is therefore preserved:

**Post A → Forwarded Post A**\
**Comment on Post A → Reply to Forwarded Post A**

This prevents comments from becoming disconnected standalone messages.

***

### Important Requirements

For the **Channel Comments Forwarding Addon** to work correctly:

* The Source must be a Telegram Channel.
* The Source Channel must have a **linked Discussion Group**.
* Comments must already be available on the source channel.
* The **Channel Comments Forwarding Addon** must be active.
* Your forwarding task must have access to the required source and target.
* The original channel post must be handled by the forwarding task so the addon can associate subsequent comments with the correct target post.

#### Recommended Setup

**Telegram**

`Source Channel → Linked Discussion Group → Comments`

**Auto Forward Messages**

`Source Channel → Target`

**Channel Comments Forwarding Addon**

`Source Comment → Reply to corresponding Target Post`

Once everything is configured, Auto Forward Messages can synchronize both the **channel posts and their conversations** automatically.
