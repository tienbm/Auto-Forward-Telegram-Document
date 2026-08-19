---
icon: discord
---

# How to Auto Forward Telegram to Discord

### Overview

Discord Publisher automatically forwards content from Telegram to Discord.

Set it up once. The system monitors a Telegram source and sends content to Discord.

This feature is useful when you want to:

* Push news, product updates, or community alerts from Telegram to Discord
* Automate operations when your team uses Telegram as the main content source
* Reduce repetitive manual work across community channels

<figure><img src="../.gitbook/assets/image (258).png" alt="" width="424"><figcaption></figcaption></figure>

***

### Where is this feature?

You can open it from:

1. Go to **Home**
2. Tap **Publish**
3. You will see the **Publish Task** area

This area includes four main parts:

* **Publish List**: shows all publish tasks you have created
* **Platform Accounts**: manages Discord accounts used for publishing
* **Create Publish Task**: creates a publishing flow from Telegram to Discord
* **Publish Detail**: monitors task status, edits configuration, and starts or stops tasks

***

### What is it used for?

Discord Publisher uses Telegram as your **content source**. It distributes that content to your Discord community automatically.

This is useful when you want to:

* Send Telegram announcements into a Discord server
* Automatically sync content between Telegram and your Discord community
* Publish the same content to one or multiple Discord channels through a connected bot account

***

### Main features

#### 1. Platform account management

You can add and manage separate accounts used for publishing.

**Discord Account**

To connect Discord, you need:

* Discord Bot Token

After adding an account, you can:

* Verify the connection
* Edit credentials
* Delete accounts you no longer use

Related documents:

* [How to get a Discord Bot Token](how-to-get-a-discord-bot-token.md)

***

#### 2. Create a Publish Task from Telegram

Each Publish Task is its own publishing configuration.

When creating a task, you can define:

* A **task name** for easier management
* A **Telegram source** such as a channel or group to monitor
* A connected **Discord account**
* One or more destination **Channel IDs**

The same content can be published to multiple Discord channels at once.

***

#### 3. Track Telegram changes

A Publish Task does not only process new messages. It also supports options related to changes from the Telegram source:

* **Include edited messages**
* **Include deleted messages**

This is useful when you want the destination platform to stay aligned with the latest state of the original Telegram content.

***

#### 4. Customize content before delivery

Before content is sent to Discord, you can configure:

* **Header**: adds text at the beginning of the post
* **Footer**: adds text at the end of the post

Examples:

* Add a source label at the top of each post
* Insert a follow reminder at the bottom
* Standardize formatting before sending content to another platform

***

#### 5. Schedule publishing

You can use scheduling to control when content is published.

This is useful when you want to:

* Avoid publishing immediately when a Telegram message arrives
* Run publishing on a specific operational schedule
* Re-post content according to the task's schedule settings

In the current app flow, this is opened through **Auto Post Schedule** in the create form or in Publish Detail.

***

#### 6. Delivery and error handling options

To make publishing more stable, the task supports a few delivery-related options:

* **Retry on rate limit**
* **Skip on error so the task can continue running**

These settings are especially useful if you publish frequently or operate multiple publish tasks at the same time.

***

#### 7. Task status management

After a task is created, you can open its detail screen to:

* View task status
* **Start Publish**
* **Stop Publish**
* Edit the task
* Delete the task

This gives you direct control over each publishing flow based on your operational needs.

***

### Quick start flow

If you want to start quickly, follow this order:

1. Open **Home → Publish**
2. Go to **Platform Accounts**
3. Add a **Discord** account
4. Verify the account connection
5. Create a new **Publish Task**
6. Select the Telegram source
7. Select the destination account
8. Enter one or more **Channel IDs**
9. Configure Header, Footer, or scheduling if needed
10. Save the task and tap **Start Publish**

***

### When should you use this feature?

#### Use case 1: Sync Telegram with your Discord community

If you manage both Telegram and Discord communities, announcements from Telegram can automatically appear in one or more Discord channels so Discord users do not miss important updates.

#### Use case 2: Separate editorial source and distribution channel

Your content team can work in Telegram. Publish Tasks then distribute content to Discord automatically.

***

### Important notes

* This feature requires the **External Publish** addon to be active
* Discord accounts should be **verified successfully** before using them in a task
* For Discord, the bot must have access to the target channel and permission to send messages
* If you edit or delete a platform account, tasks using that account may stop working
* Use clear task names if you manage multiple publishing flows

***

### Recommended usage tips

* Use **one task for one clear purpose**, for example: Telegram Announcements → Discord
* Verify account connections before enabling a production task
* For Discord, test on a secondary channel before using the main channel
* If you want consistent formatting, configure Header and Footer early
* If you run multiple publish flows, use a consistent task naming pattern for easier management

***

### Summary

Discord Publisher turns Telegram into a central publishing source for Discord.

This feature helps you:

* Sync announcements into Discord communities
* Automate Telegram-to-Discord delivery
* Reduce manual work and improve operational consistency

When configured properly, it keeps your communities aligned without extra manual work.
