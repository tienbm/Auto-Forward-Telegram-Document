---
icon: user-robot
---

# Clone Messages with a Telegram Bot

{% hint style="info" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

### Overview

Clone Bot Sender lets a Clone Profile send cloned messages through a Telegram bot instead of your personal Telegram account.

This can help separate automated clone activity from your personal account, reduce the chance that your account is identified as the sender, and reduce the risk of account restrictions while cloning.

Bot Sender does not guarantee protection from restrictions or bans. Use the feature responsibly and follow Telegram rules and the rules of the chats you use.

### Requirements

Before enabling Clone Bot Sender, make sure you have:

* an active paid **Platinum** plan
* at least one Telegram bot token saved in AutoForward
* added the bot to the target chat
* granted the bot the permissions required to send messages

Platinum Trial, Gold, Diamond, Free, and expired plans cannot enable Clone Bot Sender.

### Sender Options

<figure><img src="../.gitbook/assets/image (262).png" alt=""><figcaption></figcaption></figure>

Clone Profiles support three sender options:

#### Personal Telegram Account

Messages are sent using your connected Telegram account. This is the default option.

#### Bot by Strategy

AutoForward selects a bot using your current bot-selection strategy. Use this option when you want the system to manage bot selection automatically.

#### Specific Bot

You select one of your saved bots. AutoForward identifies it by the alias saved in Bot Management.

### Add a Telegram Bot

If you have not configured a bot yet:

1. Create a bot with **@BotFather** in Telegram.
2. Copy the bot token provided by BotFather.
3. Open **Bot Management** in AutoForward.
4. Add a new bot and paste the token.
5. Give the bot an alias that helps you recognize it.
6. Save the bot.
7. Add the bot to the target Telegram chat and grant it permission to send messages.

Keep your bot token private. Anyone with the token may be able to control your bot.

### Enable Bot Sender for a New Clone Profile

1. Open **Clone Profiles**.
2. Create a new Clone Profile.
3. Select the source and target chats.
4. Expand **Advanced Settings**.
5. Turn on **Send clone with Bot**.
6. Tap **Select bot**.
7. Choose **Telegram Bot**.
8. Choose one of the following:
   * **Bot by Strategy** to let AutoForward select the bot automatically.
   * **Select Bot** to choose a specific saved bot.
9. Use **Verify bot access to target chats** to check the bot setup.
10. Finish configuring the profile and save it.

Verification is recommended, but it does not replace Telegram permissions. The bot must still be able to send messages in the target chat.

### Change Bot Sender on an Existing Clone Profile

1. Open **Clone Profiles**.
2. Select the profile you want to change.
3. Tap **Edit**.
4. Expand **Advanced Settings**.
5. Open the Bot Sender selection.
6. Select **Personal Telegram Account** or **Telegram Bot**.
7. If you select **Telegram Bot**, choose a bot strategy or a specific bot.
8. Wait for the setting to finish saving before leaving the screen.

Bot Sender changes on a saved profile are saved automatically.

If the same profile was changed from another device or session, AutoForward reloads the latest setting and asks you to make your selection again. This prevents an older change from replacing a newer one.

### Switch Back to Your Personal Account

To stop using a bot:

1. Edit the Clone Profile.
2. Open **Advanced Settings**.
3. Turn off **Send clone with Bot**, or select **Personal Telegram Account** from the sender menu.
4. Wait for the change to finish saving.

If you previously used Bot Sender but no longer have an eligible Platinum plan, you can still switch back to **Personal Telegram Account**. Other Clone Profile settings remain available according to your current plan.

### Verify Bot Access

Before running a clone:

1. Confirm that the bot is a member of the target chat.
2. Grant the bot permission to send messages.
3. In the Clone Profile, tap **Verify bot access to target chats**.
4. Follow the instructions shown by AutoForward.

If verification fails, review the bot's role and permissions in the target chat, then try again.

### Important Notes

* Telegram albums are sent using your **Personal Telegram Account**, even when Bot Sender is enabled.
* **Bot by Strategy** uses the bot strategy currently configured in Bot Management.
* A specific bot must still exist in your saved bot list. If it was deleted, select another bot.
* Changing the visible name of a bot in Telegram does not automatically change the alias saved in AutoForward.
* Clone Profiles use Personal Telegram Account by default.

### Troubleshooting

#### I cannot enable Bot Sender

Check that:

* your paid Platinum plan is active
* you are not using a Platinum Trial
* at least one bot token is configured

If your plan is not eligible, tap **Upgrade to Platinum**. AutoForward opens the Platinum purchase screen directly.

#### AutoForward says that no bot is configured

Open **Bot Management**, add a valid BotFather token, then return to the Clone Profile and try again.

#### The selected bot is no longer available

The bot may have been deleted from Bot Management. Refresh the bot list and select another bot, or use **Bot by Strategy**.

#### The bot cannot send to the target

Add the bot to the target chat and grant it permission to send messages. In groups or channels, the bot may need to be an administrator.

#### My sender selection changed while I was editing

The profile may have been updated from another device or session. AutoForward loads the latest server state instead of overwriting it. Review the current sender and choose again if you still want to change it.

#### An album was sent by my personal account

This is expected. Albums currently continue to use the Personal Telegram Account.
