---
description: >-
  Automatic short URL generation creates shortened links for Shopee affiliate
  URLs while your content is being processed. The feature uses a verified
  teleURL credential.
---

# Set Up Automatic Short URLs For Shopee URL

### How does this feature work?

The overall flow is:

`Shopee affiliate link` → `AutoForward` → `teleURL` → `Short URL`

You only need to set up a teleURL credential once. You can then enable, disable, or change the credential at any time.

{% hint style="info" %}
**Important:** Setting up the short URL credential is a separate process and **does not require a Shopee Affiliate ID**. The Affiliate ID is only used when the app processes Shopee affiliate data.
{% endhint %}

### Before you start

<figure><img src="../../.gitbook/assets/image (279).png" alt=""><figcaption></figcaption></figure>

Prepare the following:

* An AutoForward task detail with the **Affiliate Monetization** section.
* A teleURL account, or permission to create one.
* A `SECURE_API_KEY_VALUE` generated on teleURL.com.
* A stable Internet connection.

### 1. Open Short URL setup

1. Open the task you want to configure.
2. Open **Edit content**.
3. Select **Affiliate Monetization**.
4. Open the **Shopee** card.
5. Select **Setup auto gen shortURL**.

If the Shopee configuration is collapsed, enable the Shopee switch to display the options inside the card. This only opens the configuration section; it does not replace the credential setup and does not require an Affiliate ID first.

<figure><img src="../../.gitbook/assets/image (280).png" alt=""><figcaption></figcaption></figure>

### 2. Create a teleURL credential

If you do not have a credential yet, select **Create teleURL credential**.

#### Get `SECURE_API_KEY_VALUE` from teleURL

Follow these steps:

1. Open [teleURL.com](https://teleurl.com/).
2. Sign in or create a teleURL account.
3. Open **Settings**.
4. Scroll down to the API management section.
5. Press **Generate** to create a key.
6. Create or retrieve the `SECURE_API_KEY_VALUE`.
7. Copy the key and return to the app.
8. Paste the key into the secure input field.

{% hint style="warning" %}
**Keep your key secure:** Do not share `SECURE_API_KEY_VALUE` in messages, screenshots, or unsafe storage. The app does not display the secret value again after submission.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (283).png" alt=""><figcaption></figcaption></figure>

#### Enter the credential in the app

The credential form contains:

* **Credential label:** A name to help you recognize the credential, for example `Main teleURL account`.
* **SECURE\_API\_KEY\_VALUE:** Paste the key from teleURL into the secure input field.

Then press **Verify and save**.

The app will:

1. Save the credential.
2. Send a verification request to teleURL.
3. Accept the credential only when its status is **Available**.
4. Clear the secret value from the input after the process finishes.
5. Return to the setup screen and automatically select the new credential.

<figure><img src="../../.gitbook/assets/image (284).png" alt=""><figcaption></figcaption></figure>

### 3. Select a credential

On the **Credential** step, the app shows only teleURL credentials that have been verified and have an **Available** status.

1. Tap the credential you want to use.
2. Check the credential label and the last verification time.
3. Press **Continue**.

Tapping a credential only changes the selection. The app does not move to the next step until you press **Continue**.

<figure><img src="../../.gitbook/assets/image (285).png" alt=""><figcaption></figcaption></figure>

### 4. Review the credential

On the **Review** step, check the selected credential before continuing.

* Press **Verify credential** or **Verify again** inside the credential card if you want to verify it again.
* The previous raw key cannot be viewed again.
* Press **Back** to return to credential selection.
* Press **Continue** to move to confirmation.

<figure><img src="../../.gitbook/assets/image (286).png" alt=""><figcaption></figcaption></figure>

### 5. Confirm the setup

On the **Confirm** step, review the credential one last time and choose:

* **Complete setup** for the first setup.
* **Update setup** when changing the selected credential.

After the save succeeds:

* Short URL generation is enabled.
* The credential ID is linked to the task.
* The app returns to the Affiliate Monetization screen.
* The Shopee card is refreshed and shows the new status immediately.

<figure><img src="../../.gitbook/assets/image (287).png" alt=""><figcaption></figcaption></figure>

### 6. Check the connected status

After a successful connection, the Shopee card shows a **Short URL connection** section with:

* The credential label.
* The credential status, for example **Available**.
* The feature status, for example **Active**.
* The last verification time.
* An **Update** button.
* A **Disconnect** button.

The raw key and a masked version of the key are not shown on the card.

### Manage the Short URL connection

#### Update the credential

1. Press **Update** on the Shopee card.
2. The first screen shows the current connection information.
3. Press **Update again** to start changing the setup.
4. Select another credential through the three-step flow.

The app does not open the credential picker immediately after you press **Update**. This lets you review the current status before making changes.

#### Disable Short URL with Disconnect

When you press **Disconnect**, the app shows a confirmation dialog. Disconnect will:

* Stop automatic short URL generation.
* Keep the credential so you can enable the feature again quickly.
* Not delete the credential.

Select **Cancel** to keep the current setup, or **Disconnect** to confirm that you want to disable the feature.

<figure><img src="../../.gitbook/assets/image (288).png" alt=""><figcaption></figcaption></figure>

#### Enable Short URL again

When the feature is **Disabled**:

* If the current credential is still **Available**, press **Enable** to turn the feature on quickly.
* If the credential is no longer available, the app opens the **Update** flow so you can choose or create another credential.

#### Delete a credential

In the credential list, the **Delete** button appears only when the credential can be deleted.

* A credential that is **Active** and currently used by the task must be disconnected first, so the Delete button is hidden.
* A credential that is **Disabled** but still linked to the task is unlinked first and then deleted.
* A credential that is not used by the task can be deleted after confirmation.

> Deleting a credential from the app **does not delete your teleURL account**. To delete the teleURL account itself, use teleURL.com separately.

### Common statuses

| Status                     | Meaning                                                               | What you should do                           |
| -------------------------- | --------------------------------------------------------------------- | -------------------------------------------- |
| **Not set up**             | No credential is linked to the task                                   | Select **Setup auto gen shortURL**           |
| **Available**              | The credential has been verified and can be used                      | Select the credential or enable Short URL    |
| **Active**                 | Short URL generation is enabled                                       | Use **Update** or **Disconnect**             |
| **Disabled**               | The credential is kept, but the feature is turned off                 | Press **Enable** or **Update**               |
| **Credential unavailable** | The credential is no longer ready or its metadata could not be loaded | Verify it again or select another credential |

### Troubleshooting

#### The credential I just created is not visible

1. Check whether the credential screen reported a successful verification.
2. Return to the **Credential** step.
3. Press **Retry** to reload the list.
4. Only credentials with an **Available** status are displayed.

#### The key cannot be verified

* Check that you copied the correct `SECURE_API_KEY_VALUE`.
* Generate a new key in teleURL **Settings** if the previous key has expired or is invalid.
* Create a new credential in the app and press **Verify credential**.
* The previous raw key cannot be viewed or edited in the app.

#### The Shopee card did not update after saving

After a successful operation, the app returns to the previous screen and refreshes the Shopee card. If the status is not updated:

1. Wait for the save request to finish.
2. Check your Internet connection.
3. Close and reopen the Affiliate Monetization screen.
4. If the issue continues, open **Update** and check the credential.

#### Short URLs are not being generated

Check the following:

* Short URL has an **Active** status.
* The credential has an **Available** status.
* The Shopee card is enabled.
* The input URL is a valid Shopee affiliate link.

### Frequently asked questions

#### Do I need to enter a Shopee Affiliate ID before setup?

No. You can create and verify a teleURL credential independently of the Shopee Affiliate ID. However, the input data still needs to contain a suitable Shopee affiliate link for a short URL to be generated.

#### Does the app store or show `SECURE_API_KEY_VALUE` again?

The app does not show the raw key again after submission. Keep the key secure when you generate and copy it.

#### Does Disconnect delete the credential?

No. Disconnect only turns off automatic short URL generation. The credential is kept so you can enable the feature again.

#### Does Delete remove my teleURL account?

No. Delete only removes the credential saved in the app. Your teleURL account remains available on [teleURL.com](https://teleurl.com/).

#### Can I switch to another credential?

Yes. Select **Update** → **Update again**, choose another credential on the **Credential** step, and complete the flow.

### Image checklist

| ID | Image to add                                                  |
| -- | ------------------------------------------------------------- |
| 01 | Affiliate Monetization screen with the Shopee setup button    |
| 02 | teleURL Settings, API management section, and Generate button |
| 03 | Create teleURL credential screen                              |
| 04 | Credential selection step                                     |
| 05 | Credential review step                                        |
| 06 | Setup confirmation step                                       |
| 07 | Shopee card after successful connection                       |
| 08 | Disconnect confirmation dialog                                |
| 09 | Delete button and delete confirmation dialog                  |

{% hint style="warning" %}
Before publishing this page, replace every image box with a real screenshot. Hide the complete `SECURE_API_KEY_VALUE` and any other sensitive account information.
{% endhint %}
