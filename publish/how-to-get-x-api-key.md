# How to Get X API Key

## How to Get X API Key

### Overview

Use this guide when you want to connect an **X (Twitter)** account inside AutoForward.

AutoForward currently requires these 4 values for an X Platform Account:

* API Key
* API Secret
* Access Token
* Access Secret

If you are on the **Add Platform Account** screen and selected **X**, these are the values you need to paste into the form.

***

### Before You Start

Make sure you have:

* An X account
* Access to the X Developer Portal
* A developer app or permission to create one

Important:

* AutoForward needs both the **app keys** and the **user access tokens**
* Your app should have permission to **post on your behalf**
* If your app is set to read-only, verification or publishing may fail

***

### What You Need to Collect

You will copy these 4 values from the X Developer Portal:

| AutoForward field | Value from X        |
| ----------------- | ------------------- |
| `API Key`         | API Key             |
| `API Secret`      | API Key Secret      |
| `Access Token`    | Access Token        |
| `Access Secret`   | Access Token Secret |

***

### Step 1: Open the X Developer Portal

1. Go to https://developer.x.com/en/portal/dashboard
2. Sign in with your X account
3. Open your existing Project/App, or create a new one if needed

If X asks you to create a Project first, complete that step and then create an App inside it.

***

### Step 2: Open Your App Settings

1. In the Developer Portal, select the app you want to use with AutoForward
2. Open the app details page
3. Find the sections related to:
   * Keys and tokens
   * App permissions
   * User authentication settings

The exact layout in X may change over time, but these sections are the ones you need.

***

### Step 3: Set the Correct App Permissions

Before generating tokens, make sure the app can publish posts.

Recommended setting:

* **Read and write**

If your app only has **Read** permission, AutoForward may connect incorrectly or fail when trying to publish.

If you change permissions later:

* Save the new permission settings
* Generate a new **Access Token** and **Access Secret**
* Update the values in AutoForward

***

### Step 4: Enable User Authentication If Needed

Depending on the current X Developer Portal flow, you may need to enable user authentication for your app.

If X shows a **User authentication settings** section:

1. Enable it
2. Choose the setup that allows user-context access
3. Save the settings

For AutoForward, the important point is that your app must be able to create **Access Token** and **Access Token Secret** for your account.

***

### Step 5: Copy API Key and API Secret

1. Open the **Keys and tokens** section
2. Find your app keys
3. Copy:
   * **API Key**
   * **API Key Secret**

In some X screens, these may also be labeled as:

* Consumer Key
* Consumer Secret

If so:

* Consumer Key = API Key
* Consumer Secret = API Secret

***

### Step 6: Generate Access Token and Access Secret

In the same **Keys and tokens** area, find the user token section and generate:

* **Access Token**
* **Access Token Secret**

This step is required.

AutoForward cannot use only the API Key and API Secret. It also needs the user-level token pair.

If X provides a **Regenerate** button instead of **Generate**, use that and copy the newly created values.

***

### Step 7: Paste the Values into AutoForward

1. Open **Platform Accounts** in AutoForward
2. Tap **Add Account**
3. Select **X**
4. Enter an account name
5. Paste each value into the matching field:
   * API Key
   * API Secret
   * Access Token
   * Access Secret
6. Save the account
7. Run **Verify Connection** if that option is shown

If the credentials are valid, the account should move to a connected state after verification.

***

### Field Mapping Example

If X gives you these values:

```
API Key: abc123
API Key Secret: def456
Access Token: ghi789
Access Token Secret: xyz000
```

Then in AutoForward you fill:

```
API Key      -> abc123
API Secret   -> def456
Access Token -> ghi789
Access Secret -> xyz000
```

***

### Common Mistakes

#### 1. Copying only the API Key pair

AutoForward needs all 4 values, not just:

* API Key
* API Secret

You must also provide:

* Access Token
* Access Secret

#### 2. App is set to read-only

If the app permission is **Read** only, posting may fail.

Use:

* **Read and write**

#### 3. Changed permissions but kept old access tokens

If you update app permissions in X, older access tokens may no longer match the new permission scope.

After changing permissions:

1. Regenerate the Access Token
2. Regenerate the Access Token Secret
3. Update AutoForward with the new values

#### 4. Regenerated keys in X but still using the old ones in AutoForward

When you regenerate any credential in X, the previous value can stop working.

Update AutoForward immediately with the new values.

#### 5. Mixing credentials from different apps

Make sure all 4 values come from the same X app and the same user context.

***

### Security Notes

* Treat all 4 values like passwords
* Never share them in chats, screenshots, or tickets
* Never commit them to Git or public repositories
* If any value is exposed, regenerate it in X and update AutoForward immediately

***

### Quick Checklist

* X Developer Portal access is available
* Correct app is selected
* App permission is set to **Read and write**
* API Key copied
* API Secret copied
* Access Token generated and copied
* Access Secret generated and copied
* All 4 values pasted into AutoForward
* Account saved and verified

***

### Troubleshooting

If AutoForward cannot verify your X account:

1. Re-check that all 4 fields are filled
2. Confirm the app permission is **Read and write**
3. Regenerate **Access Token** and **Access Secret** after any permission change
4. Make sure the values come from the same app
5. Save the account again and re-run verification

If verification succeeds but publishing still fails, review the app permission and regenerate the user access tokens one more time.
