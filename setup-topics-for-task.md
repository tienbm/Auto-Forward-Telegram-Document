# Setup Topics For Task

## Topic Sync User Guide

### What Is Topic Sync?

Topic Sync automatically keeps topics aligned between your source and target groups in a forwarding task.

* New source topics are created automatically in the target group.
* Renamed source topics are updated in the target group.
* Existing topics can be copied once using **Copy existing topic structure**.

### Before You Start

Make sure **Topics** is enabled in every target group. The bot must also have permission to create and rename topics there.

### How to Set Up Topic Sync

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

You can still open **Manual topic mapping** to edit or remove individual mappings. Manual mapping is useful when a source topic should be forwarded to a specific target topic.

### Important Notes

* Copying only includes topics that exist when you start the copy.
* Turn on **Auto-sync topics** to keep future topics and renames synchronized.
* Topic deletion is not synchronized. Deleting a source topic does not delete the target topic.
* If the copy stays queued for a while, keep the task saved and check again later. The bot processes it in the background.
