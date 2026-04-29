# How to Get a Discord Bot Token

## How to Get a Discord Bot Token

### Overview

Use this guide when you want to connect a Discord account inside AutoForward.

AutoForward uses a **Discord Bot Token** to authenticate your bot before it can publish messages to Discord channels or webhook-based destinations.

If you are on the **Add Platform Account** screen and selected **Discord**, this is the value you need to paste into the **Discord Bot Token** field.

***

### Before You Start

Make sure you have:

* A Discord account
* Access to the Discord server where the bot will be used
* Permission to create applications in the Discord Developer Portal

***

### Step 1: Open the Discord Developer Portal

1. Go to https://discord.com/developers/applications
2. Sign in with your Discord account
3. Click **New Application**

***

### Step 2: Create a New Discord Application

1. Enter a name for your bot
2. Click **Create**
3. You will be taken to the application dashboard

Use a clear name so you can recognize it later inside AutoForward, for example:

* `AutoForward Bot`
* `News Relay Bot`
* `Telegram to Discord Bot`

***

### Step 3: Add a Bot to the Application

1. In the left sidebar, open the **Bot** tab
2. Click **Add Bot**
3. Confirm by clicking **Yes, do it!**

After this step, Discord creates a bot user for your application.

***

### Step 4: Copy the Bot Token

1. Stay on the **Bot** tab
2. Find the token section
3. Click **Reset Token** if Discord asks you to generate one first
4. Click **Copy** to copy the token

This copied value is your bot token.

Example raw token format:

```
MTIzNDU2Nzg5MDEyMzQ1Njc4.GhIjKl.MnOpQrStUvWxYz1234567890
```

***

### Step 5: Format the Token for AutoForward

In the current AutoForward Discord account flow, use the token in this format:

```
Bot YOUR_DISCORD_BOT_TOKEN
```

Example:

```
Bot MTIzNDU2Nzg5MDEyMzQ1Njc4.GhIjKl.MnOpQrStUvWxYz1234567890
```

Important:

* Include the word `Bot`
* Include exactly one space after `Bot`
* Then paste the token you copied from Discord
* Do not add quotes

If you only copied the raw token from Discord, prepend `Bot` before pasting it into AutoForward.

***

### Step 6: Add the Token in AutoForward

1. Open **Platform Accounts** in AutoForward
2. Tap **Add Account**
3. Select **Discord**
4. Enter an account name
5. Paste the formatted value into **Discord Bot Token**
6. Save the account
7. Run **Verify Connection** if that option is shown

If the token is valid, the account status should move to a connected state after verification.

***

### Step 7: Invite the Bot to Your Discord Server

Getting the token is not enough by itself. To send messages to a Discord server, your bot must also be added to that server.

Basic flow:

1. Open the **OAuth2** tab in the Discord Developer Portal
2. Go to **URL Generator**
3. Select the scopes your setup needs
4. Generate the invite URL
5. Open the URL and add the bot to your server

At minimum, make sure the bot has the permissions required for your destination type, such as:

* View Channels
* Send Messages
* Embed Links
* Attach Files

If you plan to publish into a specific channel by bot account, also confirm that the bot can see and post in that channel.

***

### Common Mistakes

#### 1. Pasting the raw token without the prefix

Wrong:

```
MTIzNDU2Nzg5MDEyMzQ1Njc4.GhIjKl.MnOpQrStUvWxYz1234567890
```

Correct:

```
Bot MTIzNDU2Nzg5MDEyMzQ1Njc4.GhIjKl.MnOpQrStUvWxYz1234567890
```

#### 2. Resetting the token and still using the old value

If you click **Reset Token** in Discord, the old token stops working immediately. Update the token in AutoForward right away.

#### 3. Bot not added to the server

Even with a valid token, the bot cannot deliver messages if it has not been invited to the target server.

#### 4. Missing channel permissions

The bot may verify successfully but still fail to publish if it lacks permission in the target channel.

***

### Security Notes

* Treat your Discord Bot Token like a password
* Never share it in screenshots, chats, or support tickets
* Never commit it to Git or public repositories
* If the token is exposed, reset it immediately in the Discord Developer Portal and update AutoForward with the new value

***

### Quick Checklist

* Application created in Discord Developer Portal
* Bot added to the application
* Bot token copied
* `Bot` prefix added before the token
* Token pasted into AutoForward
* Account saved and verified
* Bot invited to the correct Discord server
* Bot has permission to post in the target channel

***

### Troubleshooting

If AutoForward cannot verify your Discord account:

1. Re-copy the token from the Discord Developer Portal
2. Make sure the value starts with `Bot`
3. Remove accidental extra spaces before or after the token
4. Confirm the token has not been reset
5. Save the account again and re-run verification

If the account verifies but publishing still fails, check the bot's server membership and channel permissions.
