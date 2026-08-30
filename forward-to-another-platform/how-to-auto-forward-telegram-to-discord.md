---
icon: discord
---

# How to Auto Forward Telegram to Discord

AutoForward can publish new Telegram messages to one or more Discord text channels through a Discord bot. Set up the bot once, connect it to AutoForward, choose your Telegram sources and Discord channel IDs, then create a **Publish Task**.

The current AutoForward Discord flow uses a **Discord Bot** and **Channel ID**. It does not use a Discord webhook.

### What you need

Before you begin, prepare:

* An AutoForward account that is signed in and connected to Telegram.
* Access to the Telegram channel, group, or chat that you want to monitor.
* An active **External Publish** addon.
* Permission to create an application in the [Discord Developer Portal](https://discord.com/developers/applications).
* A Discord server and target text channel where the bot can view and send messages.
* A Discord Bot Token in the format required by AutoForward: `Bot YOUR_DISCORD_BOT_TOKEN`.

### How it works

```
Telegram source(s) → AutoForward Publish Task → Discord Bot → Discord channel(s)
```

Discord Publish:

* Publishes **new messages** after the task is created.
* Can monitor one or more selected Telegram sources.
* Can publish the same message to one or more Discord channels.
* Requires the bot to be a member of the target server and able to post in each channel.
* Does not automatically repost Telegram messages that existed before the task was created.

### 1. Create a Discord application and bot

1. Open the [Discord Developer Portal](https://discord.com/developers/applications) and sign in.
2. Select **New Application**.
3. Enter an application name, then select **Create**.
4. Open the **Bot** page in the application settings. If the application does not have a bot user yet, select **Add Bot** and confirm.
5. In the token section, select **Reset Token** to generate a new bot token, then select **Copy**.
6. Store the token in a secure password manager. You will need it in the next step.

Do not add quotes or use the Application ID, Public Key, Client Secret, or another Discord value in the **Discord Bot Token** field.

For a focused token walkthrough, see How to Get a Discord Bot Token.

<figure><img src="../.gitbook/assets/image (315).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Treat the Discord Bot Token like a password. If it is exposed, select **Reset Token**, copy the new token, and update the Discord account in AutoForward immediately.
{% endhint %}

### 2. Invite the bot to your Discord server

The bot must be installed in the server before AutoForward can publish to its channels.

1. In the Discord Developer Portal, open the application's **Installation** page. If your portal uses the older layout, open **OAuth2 → URL Generator** instead.
2. Create a server installation link with the `bot` scope.
3.  Request at least these bot permissions:

    * **View Channels**
    * **Send Messages**

    If you want to forward media or use rich links, also request **Embed Links** and **Attach Files**.
4. Copy the generated installation URL and open it in your browser.
5. Choose the target server and authorize the bot. You may need server permission to add bots.
6. Open the target channel in Discord and confirm that the bot can view and send messages there. Channel-specific permission overrides can remove access even when the bot has server-level permissions.

<figure><img src="../.gitbook/assets/image (316).png" alt=""><figcaption></figcaption></figure>

### 3. Get the Discord Channel ID

AutoForward uses the numeric **Channel ID**, not the channel name, invite link, or a message link.

1. Enable **Developer Mode** in Discord:
   * **Desktop**: open **User Settings → Advanced**, then enable **Developer Mode**.
   * **Mobile**: open your avatar, select the gear icon, open **Advanced**, then enable **Developer Mode**.
2. In the server, right-click the target channel on desktop, or press and hold it on mobile.
3. Select **Copy Channel ID**.
4. Keep the copied ID ready for the AutoForward task. Repeat these steps for every channel that should receive the messages.

See Discord's [official instructions for finding a Channel ID](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID) if you need help locating the option.

<figure><img src="../.gitbook/assets/image (317).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (318).png" alt=""><figcaption></figcaption></figure>

### 4. Connect the Discord bot to AutoForward

1. Open AutoForward and go to **Home**.
2. Select **Publish**.
3. On the **Publish Tasks** page, select **Manage Accounts** to open **Platform Accounts**.
4. Select **Add Account**.
5. Under **Select Platform**, choose **Discord**.
6. Enter an **Account Name**, such as `Community Discord Bot`.
7. In **Discord Bot Token**, paste the token with the required `Bot` prefix.
8. Select **Save**.

AutoForward verifies the bot connection after saving. The account is ready when its status shows **Connected**.

If the account is not connected, open its actions and select **Verify Connection** after checking the token format and bot installation. Only a connected Discord account can be selected in a Publish Task.

You can also add the bot from the task wizard by selecting **Add connection** on the **Connection** step.

<figure><img src="../.gitbook/assets/image (320).png" alt=""><figcaption></figcaption></figure>

### 5. Create a Discord Publish Task

Return to **Publish Tasks** and select **Create Publish Task**. AutoForward opens a four-step wizard:

1. **Provider**
2. **Connection**
3. **Source and recipient**
4. **Review**

#### Step 1: Choose Discord as the provider

1. On the **Provider** step, select **Discord**.
2. Select **Next**.

<figure><img src="../.gitbook/assets/image (322).png" alt=""><figcaption></figcaption></figure>

#### Step 2: Choose the Discord connection

1. On the **Connection** step, select a Discord account with the **Connected** status.
2. If no account is available, select **Add connection**, create the Discord account, and save it.
3. After the account is connected, select **Next**.

If the account shows **Verify connection** or is not listed, return to **Platform Accounts**, verify the bot, and refresh the connection list.

<figure><img src="../.gitbook/assets/image (323).png" alt=""><figcaption></figcaption></figure>

#### Step 3: Select Telegram sources and Discord channels

On **Source and recipient**:

**Select Telegram sources**

1. Open the Telegram source selector.
2. Select one or more Telegram channels, groups, or chats.
3. Confirm that all required sources are selected.

**Add Discord destination channels**

1. In **Discord Options**, find **Channel #1**.
2. Paste the numeric value into **Channel ID**.
3. To publish to another Discord channel, select **Add Discord Channel** and enter its Channel ID.
4. Repeat until every target channel is listed.

AutoForward checks each Channel ID before the task can be saved. The bot must be able to access and send messages to every channel you add.

If you need to customize how source changes are handled, open **Advanced Settings**. Depending on your task configuration, you can configure **Edit**, **Delete**, **Add Header**, **Add Footer**, **Auto Post Scheduler**, **Retry on Rate Limit**, and **Skip on Error**.

<figure><img src="../.gitbook/assets/image (324).png" alt=""><figcaption></figcaption></figure>

#### Step 4: Review and create the task

On the **Review** step, check:

* The **Task Name**.
* The provider: **Discord**.
* The selected **Connection** and its **Connected** status.
* The Telegram source count and names.
* Every Discord destination **Channel ID**.
* The **New messages only** rule.

Select **Create Publish Task** when the configuration is correct.

<figure><img src="../.gitbook/assets/image (321).png" alt=""><figcaption></figcaption></figure>

### After setup: test the forwarding flow

After the task is created, AutoForward opens the **Publish Detail** screen.

1. Confirm that the task status is **Running**.
2. Send a new test message to one of the selected Telegram sources.
3. Check the configured Discord channel for the forwarded message.
4. If the task is **Stopped**, select **Start Publish**, wait for the status to change to **Running**, and send a new test message.

The task starts with **new messages only**. Telegram messages that existed before the task was created are not automatically reposted.

{% hint style="info" %}
🖼️ **IMAGE BOX 09 — Discord Publish Task running**

Show **Publish Detail** with the task in the **Running** state and the Discord destination visible. Use a test task, source, account, and Channel ID; do not show bot tokens, private server information, or message content that should not be published.
{% endhint %}

### Manage your Discord Publish Task

#### Start or stop the task

* **Start Publish** starts a stopped task.
* **Stop Publish** pauses the task and prevents new messages from being sent until it is started again.

#### Edit the task

Open the task and select **Edit Publish Task**. You can update the task name, Telegram sources, Discord Channel IDs, and supported task options. Save the task after making changes.

#### Add or remove a Discord channel

Edit the task from **Publish Detail**, then update **Discord Options**:

* Select **Add Discord Channel** to add another destination.
* Remove an extra channel from the channel list.
* Save the task and wait for AutoForward to validate every destination again.

#### Update or reconnect the bot

If the token is reset or the bot loses access:

1. Open **Platform Accounts** from **Publish**.
2. Open the Discord account and select **Edit Account**.
3. Replace the value in **Discord Bot Token** with the current `Bot YOUR_DISCORD_BOT_TOKEN` value.
4. Select **Save**, then select **Verify Connection** if needed.
5. Return to the task and select **Start Publish** if the task is stopped.

#### Delete the task or account

* Deleting a Publish Task removes only its AutoForward configuration. It does not delete the Discord bot, server, or channel.
* Deleting the Discord account removes the saved connection from AutoForward. Publish Tasks using that account may stop working.
* Resetting a Discord token invalidates the old token. Update the saved account before verifying or publishing again.

### Common statuses

| Status        | Meaning                                                           | What to do                                                                        |
| ------------- | ----------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| **Connected** | AutoForward verified the Discord Bot Token.                       | Select this account in the task wizard.                                           |
| **Pending**   | The account is waiting for verification to finish.                | Refresh the account list, then verify the connection again if needed.             |
| **Invalid**   | The token is incorrect, expired, or no longer accepted.           | Reset the token in Discord, update AutoForward, and select **Verify Connection**. |
| **Expired**   | The saved connection is no longer usable.                         | Edit the account with a current token and verify it again.                        |
| **Running**   | The Publish Task is monitoring Telegram and can publish messages. | Send a new test message to a selected source.                                     |
| **Stopped**   | The Publish Task is paused.                                       | Select **Start Publish** to resume it.                                            |

### Troubleshooting

#### AutoForward cannot verify the Discord account

Check the following:

1. The value starts with `Bot` , including exactly one space after `Bot`.
2. The token was copied from the correct Discord application.
3. The token has not been reset since it was added to AutoForward.
4. You pasted the bot token, not the Application ID, Public Key, or Client Secret.
5. Save the account again, then select **Verify Connection**.

#### The account is connected but no message appears in Discord

1. Confirm that the bot was added to the correct server.
2. Check that the bot can **View Channels** and **Send Messages** in the target channel.
3. Confirm that the Channel ID belongs to the intended channel and was copied after enabling **Developer Mode**.
4. Confirm that the Publish Task status is **Running**.
5. Send a new Telegram message after the task was created. Older messages are not automatically reposted.
6. If you added multiple channels, check each channel's permissions separately.

#### AutoForward rejects a Channel ID

* Paste the numeric Channel ID, not the channel name, invite URL, or message link.
* Confirm that the bot can access the channel.
* Remove extra spaces or other characters.
* If the channel is private, ask a server administrator to add the bot and grant channel access.

#### The bot can access the server but not the target channel

Discord channel permission overrides can block a bot even when it has server-level permissions. Open the target channel's permissions and allow the bot role to view the channel and send messages.

#### Media or rich links are not delivered

Confirm that the bot has the permissions required by the content, such as **Embed Links** and **Attach Files**. Test plain text first to separate a permission problem from a content-specific problem.

#### The task stopped after an error

Open **Publish Detail**, resolve the bot token or channel permission problem, then select **Start Publish**. Send a new test message after the task returns to **Running**.

### Frequently asked questions

#### Can one Publish Task send to multiple Discord channels?

Yes. Add each destination with **Add Discord Channel** and enter its numeric **Channel ID**. AutoForward validates every channel before saving the task.

#### Can I use a Discord webhook instead of a bot?

Not in the current AutoForward Discord flow. Connect a Discord Bot Token and use one or more Channel IDs.

#### Does AutoForward repost old Telegram messages after setup?

No. The Discord Publish flow starts with new Telegram messages after the task is created.

#### Does deleting a Publish Task delete my Discord bot?

No. Deleting a task removes only the AutoForward task configuration. The Discord application, bot, server, and channels remain unchanged.

#### What happens if I reset the bot token?

The old token stops working. Copy the new token, update the Discord account in AutoForward, save it, and verify the connection again.

### Security reminders

* Treat the Discord Bot Token like a password.
* Never share it in screenshots, chats, support tickets, or public repositories.
* Use fake or fully redacted values in documentation and tutorial screenshots.
* Reset the token immediately if you think it has been exposed.
