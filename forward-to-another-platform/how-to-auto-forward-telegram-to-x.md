---
icon: x
---

# How to Auto Forward Telegram to X

### Overview

X Publisher automatically forwards content from Telegram to X.

Set it up once. The system monitors a Telegram source and publishes content to X.

This feature is useful when you want to:

* Sync announcements from Telegram to X to keep your social channels active
* Automate operations when your team uses Telegram as the main content source
* Reduce repetitive manual work across publishing channels

<figure><img src="../.gitbook/assets/image (258).png" alt="" width="424"><figcaption></figcaption></figure>

***

### Where is this feature?

You can open it from:

1. Go to **Home**
2. Tap **Publish**
3. You will see the **Publish Task** area

This area includes four main parts:

* **Publish List**: shows all publish tasks you have created
* **Platform Accounts**: manages X accounts used for publishing
* **Create Publish Task**: creates a publishing flow from Telegram to X
* **Publish Detail**: monitors task status, edits configuration, and starts or stops tasks

***

### What is it used for?

X Publisher uses Telegram as your **content source**. It publishes that content to X automatically.

This is useful when you want to:

* Repost Telegram content to your project or brand's X account
* Maintain a steady posting flow on X without manual posting
* Use Telegram as the editorial source while X becomes the public distribution channel

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

After adding an account, you can:

* Verify the connection
* Edit credentials
* Delete accounts you no longer use

Related documents:

* [How to Get X API Key](how-to-get-x-api-key.md)

***

#### 2. Create a Publish Task from Telegram

Each Publish Task is its own publishing configuration.

When creating a task, you can define:

* A **task name** for easier management
* A **Telegram source** such as a channel or group to monitor
* A connected **X account**

***

#### 3. Track Telegram changes

A Publish Task does not only process new messages. It also supports options related to changes from the Telegram source:

* **Include edited messages**
* **Include deleted messages**

This is useful when you want the destination platform to stay aligned with the latest state of the original Telegram content.

***

#### 4. Customize content before publishing

Before content is published to X, you can configure:

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
3. Add an **X** account
4. Verify the account connection
5. Create a new **Publish Task**
6. Select the Telegram source
7. Select the destination account
8. Configure Header, Footer, or scheduling if needed
9. Save the task and tap **Start Publish**

***

### When should you use this feature?

#### Use case 1: Repost project announcements to X

If your Telegram channel is your official announcement source, you can create a Publish Task to automatically repost those updates to your X account instead of copying them manually.

#### Use case 2: Separate editorial source and distribution channel

Your content team can work in Telegram. Publish Tasks then distribute content to X automatically.

***

### Important notes

* This feature requires the **External Publish** addon to be active
* X accounts should be **verified successfully** before using them in a task
* If you edit or delete a platform account, tasks using that account may stop working
* Use clear task names if you manage multiple publishing flows

***

### Recommended usage tips

* Use **one task for one clear purpose**, for example: Telegram News → X
* Verify account connections before enabling a production task
* If you want consistent formatting, configure Header and Footer early
* If you run multiple publish flows, use a consistent task naming pattern for easier management

***

### Summary

X Publisher turns Telegram into a central publishing source for X.

This feature helps you:

* Repost Telegram content to social media
* Automate Telegram-to-X publishing
* Reduce manual work and improve operational consistency

When configured properly, it keeps your X account active without extra manual work.
