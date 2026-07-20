---
description: >-
  This guide explains how to choose topics for a forwarding task and how to use
  Topic Sync.
icon: hashtag
---

# Setup Topics for a Forwarding Task

### What Is Topic Setup?

Topic setup lets you control which topics receive forwarded messages.

* **Source topics**: topics where messages are read.
* **Target topics**: topics where messages are forwarded.
* You can create more than one source-to-target mapping.

<figure><img src=".gitbook/assets/Simulator Screenshot - iPhone 17 - 2026-07-20 at 11.21.36.png" alt="" width="375"><figcaption></figcaption></figure>

### Set Up Topics Manually

1. Open your forwarding task.
2. Open **Set Up Forward Topics**.
3. Expand **Manual topic mapping**.
4. In a mapping row, tap **Add Source Topics**.
5. Search for a group or topic, then select one or more topics.
6. Tap **Done**.
7. Tap **Add Target Topics** and select the target topic or topics.
8. Tap **Add More Forward Topics** to create another mapping row if needed.
9. Tap **Save** on the setup screen.

You can remove a selected topic with the remove icon. To remove a complete mapping row, use the close icon on that row.

#### Selecting Topics

The topic selection screen provides:

* Search by group name or chat ID.
* Filters for **All**, **Group**, **Channel**, **Bot**, and **User**.
* Multiple topic selection.
* An option to select all topics in the listed groups.
* **Reload** for a group when the topic list is out of date.

When you select specific topics in a group, the all-topics option for that group is replaced by the specific selection.

If a group has no topics, enable **Topics** in Telegram first, then reload the group.

#### Add a Missing Topic

If a topic is not returned by Telegram, tap **Add Topic** for the group and enter its topic ID and name. Then select it and tap **Done**.

<figure><img src=".gitbook/assets/Screenshot 2026-07-01 at 15.16.18.png" alt="" width="342"><figcaption></figcaption></figure>

### What Is Topic Sync?

Topic Sync automatically keeps topics aligned between your source and target groups in a forwarding task.

* New source topics are created automatically in the target group.
* Renamed source topics are updated in the target group.
* Existing topics can be copied once using **Copy existing topic structure**.

### Before You Start

Make sure **Topics** is enabled in every target group. The bot must also have permission to create and rename topics there.

### Enable Topic Sync

1. Open your forwarding task.
2. Open **Forward Topics**.
3. Turn on **Auto-sync topics**.
4. Tap **Save**.

Auto-sync starts after the task is saved.

### Copy Existing Topics

Auto-sync handles new changes. To copy topics that already exist:

1. Tap **Copy existing topic structure**.
2. Select the source group or groups.
3. Select the target group or groups.
4. Confirm the copy request.
5. Save the task if you are creating a new task.

The copy runs in the background. You may see these statuses:

* **Queued**: waiting for the bot to start.
* **Processing**: the bot is copying topics.
* **Completed**: all topics were processed successfully.
* **Partial**: some topics were copied, but some failed.
* **Failed**: the copy could not be completed. Check the target group permissions and try again.

The summary shows how many topics were created, already existed, or failed. Existing target topics with the same name are reused.

### Manual Mapping

You can use **Manual topic mapping** together with Topic Sync. Manual mapping is useful when a source topic should be forwarded to a specific target topic or when you want to adjust individual mappings.

### Important Notes

* Copying only includes topics that exist when you start the copy.
* Turn on **Auto-sync topics** to keep future topics and renames synchronized.
* Topic deletion is not synchronized. Deleting a source topic does not delete the target topic.
* If the copy stays queued for a while, keep the task saved and check again later. The bot processes it in the background.
* Selecting topics does not save the task by itself. Always tap **Save** on the setup screen.
