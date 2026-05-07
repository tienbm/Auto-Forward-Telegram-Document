# X & Discord Publisher

### Overview

X & Discord Publisher lets you take content from Telegram and publish it automatically to external platforms, specifically **X (Twitter)** and **Discord**.

Instead of manually copying every post or announcement from Telegram to other platforms, you only need to set it up once. The system monitors your Telegram source, then publishes content automatically based on your configuration.

This feature is useful when you want to:

* Sync announcements from Telegram to X to keep your social channels active
* Push news, product updates, or community alerts from Telegram to Discord
* Automate operations when your team uses Telegram as the main content source
* Reduce repetitive manual work when posting the same content to multiple platforms

<figure><img src="../.gitbook/assets/image (258).png" alt="" width="424"><figcaption></figcaption></figure>

***

### Where is this feature?

You can open it from:

1. Go to **Home**
2. Tap **Publish**
3. You will see the **Publish Task** area

This area currently includes 4 main parts:

* **Publish List**: shows all publish tasks you have created
* **Platform Accounts**: manages the X and Discord accounts used for publishing
* **Create Publish Task**: creates a new publishing flow from Telegram to X or Discord
* **Publish Detail**: monitors task status, edits configuration, and starts or stops tasks

***

### What is it used for?

X & Discord Publisher is designed to turn Telegram into your **content input source**, then automatically distribute that content to other platforms.

#### For X Publisher

This is useful when you want to:

* Repost Telegram content to your project or brand's X account
* Maintain a steady posting flow on X without manual posting
* Use Telegram as the editorial source while X becomes the public distribution channel

#### For Discord Publisher

This is useful when you want to:

* Send Telegram announcements into a Discord server
* Automatically sync content between Telegram and your Discord community
* Publish the same content to one or multiple Discord channels through a connected bot account

***

### Main features

#### 1. Platform account management

You can add and manage separate accounts used for publishing.

**X Account**

To connect X, you need:

* API Key
* API Secret
* Access Token
* Access Secret

**Discord Account**

To connect Discord, you need:

* Discord Bot Token

After adding an account, you can:

* Verify the connection
* Edit credentials
* Delete accounts you no longer use
* Filter accounts by X or Discord

Related documents:

* How to get an X API Key
* How to get a Discord Bot Token

***

#### 2. Create a Publish Task from Telegram

Each Publish Task is its own publishing configuration.

When creating a task, you can define:

* A **task name** for easier management
* A **Telegram source** such as a channel or group to monitor
* A **destination platform**: X or Discord
* A connected **publishing account**

If you choose **Discord**, you can add **one or more Channel IDs** so the same content is published to multiple Discord channels at the same time.

***

#### 3. Track Telegram changes

A Publish Task does not only process new messages. It also supports options related to changes from the Telegram source:

* **Include edited messages**
* **Include deleted messages**

This is useful when you want the destination platform to stay aligned with the latest state of the original Telegram content.

***

#### 4. Customize content before publishing

Before content is published to X or Discord, you can configure additional content formatting such as:

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
3. Add an **X** or **Discord** account
4. Verify the account connection
5. Create a new **Publish Task**
6. Select the Telegram source
7. Select the destination account
8. If you use Discord, enter one or more **Channel IDs**
9. Configure Header, Footer, or scheduling if needed
10. Save the task and tap **Start Publish**

***

### When should you use this feature?

#### Use case 1: Repost project announcements to X

If your Telegram channel is your official announcement source, you can create a Publish Task to automatically repost those updates to your X account instead of copying them manually.

#### Use case 2: Sync Telegram with your Discord community

If you manage both Telegram and Discord communities, announcements from Telegram can automatically appear in one or more Discord channels so Discord users do not miss important updates.

#### Use case 3: Separate editorial source and distribution channels

Your content team can work inside Telegram, then use Publish Tasks to distribute that content to public or internal platforms automatically.

***

### Important notes

* This feature requires the **External Publish** addon to be active
* X or Discord accounts should be **verified successfully** before using them in a task
* For Discord, the bot must have access to the target channel and permission to send messages
* If you edit or delete a platform account, tasks using that account may stop working
* Use clear task names if you manage multiple publishing flows

***

### Recommended usage tips

* Use **one task for one clear purpose**, for example: Telegram News → X or Telegram Announcements → Discord
* Verify account connections before enabling a production task
* For Discord, test on a secondary channel before using the main channel
* If you want consistent formatting, configure Header and Footer early
* If you run multiple publish flows, use a consistent task naming pattern for easier management

***

### Summary

X & Discord Publisher helps you **turn Telegram into a central publishing source**, then automatically distribute content to **X** and **Discord**.

This feature is especially useful for users who need to:

* Repost Telegram content to social media
* Sync announcements into Discord communities
* Automate multi-platform content distribution
* Reduce manual work and improve operational consistency

When configured properly, it becomes an efficient way to extend Telegram content to external channels without increasing day-to-day workload.
