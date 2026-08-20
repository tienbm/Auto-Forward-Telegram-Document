---
icon: envelope
---

# How to Auto Forward Telegram to Email

{% embed url="https://youtu.be/WGN_kvynF7s" %}

AutoForward can send new messages from Telegram to an email address automatically.

The feature is configured from **Publish**. You connect an email account once, choose the Telegram sources to monitor, enter the recipient email address, and create a Publish Task.

<figure><img src="../.gitbook/assets/image (268).png" alt="" width="497"><figcaption></figcaption></figure>

### What you need

Before you begin, prepare:

* A Telegram account connected to AutoForward.
* Access to the Telegram channel, group, or chat that you want to use as a source.
* An email account that can send messages through Gmail or SMTP.
* The recipient email address.

For Gmail, you need a **Gmail App Password**. Do not use your normal Google account password.

### How email publishing works

```
Telegram source(s) → AutoForward Publish Task → Email recipient
```

Email Publish:

* Sends **new messages only**.
* Can monitor one or more selected Telegram sources.
* Does not repost old messages when the task is created.
* Does not mirror Telegram message edits or deletes.
* Supports email attachments up to **8 MiB per file** and **20 MiB per source message**.

### Step 1: Open Publish

1. Open AutoForward.
2. Open **Publish**.
3. Tap or click **Create Publish Task**.

<figure><img src="../.gitbook/assets/image (269).png" alt=""><figcaption></figcaption></figure>

> Capture the Publish list with the **Create Publish Task** button visible. The screenshot should show the page title and the button location on both mobile and web if both versions are documented.

### Step 2: Add an email connection

<figure><img src="../.gitbook/assets/image (270).png" alt=""><figcaption></figcaption></figure>

You need a connected email account before you can create an Email Publish Task.

<figure><img src="../.gitbook/assets/image (271).png" alt=""><figcaption></figcaption></figure>

1. Open **Platform accounts** or **Manage accounts**.
2. Select **Add account**.
3. In **Choose platform**, select **Email**.
4. Enter an account name, such as `Company Gmail` or `Support SMTP`.
5. Choose **Gmail** or expand **Advanced settings** to use **Custom SMTP**.

After saving, AutoForward verifies the connection. Only a connection with the status **Connected** can be selected in a Publish Task.

> **Security note:** Credentials are used to verify and send email. They are not displayed again after the account is saved. When a connection needs to be repaired, enter the secret again instead of expecting it to be pre-filled.

#### Option A: Gmail

Enter the following information:

<figure><img src="../.gitbook/assets/image (272).png" alt=""><figcaption></figcaption></figure>

| Field             | What to enter                                                   |
| ----------------- | --------------------------------------------------------------- |
| **Email address** | The Gmail address that will send the email.                     |
| **App password**  | The 16-character App Password generated in your Google Account. |
| **Sender name**   | Optional name shown to email recipients.                        |

The Gmail SMTP server, port, and security settings are configured automatically. You do not need to enter them.

**Get a Gmail App Password**

1. Turn on [**2-Step Verification** for your Google Account.](https://myaccount.google.com/security)
2. Open **Google Account → Security →** [**App passwords**](https://myaccount.google.com/u/2/apppasswords).
3. Create a new App Password and name it `AutoForward`.
4. Copy the generated code and paste it into the **App password** field.

Use the App Password instead of your normal Gmail password. If Google does not show the **App passwords** option, check that 2-Step Verification is enabled and that your Google Workspace administrator allows App Passwords.

<figure><img src="../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure>

#### Option B: Custom SMTP

Expand **Advanced settings** and choose **Custom SMTP**. Enter:

| Field            | What to enter                                                                                                                     |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **SMTP host**    | A public DNS hostname, such as `smtp.example.com`. `localhost`, private IP addresses, and local-only hostnames are not supported. |
| **Port**         | `465` or `587`.                                                                                                                   |
| **Security**     | Use **TLS** with port `465`, or **STARTTLS** with port `587`.                                                                     |
| **Username**     | The username provided by your SMTP provider.                                                                                      |
| **Password**     | The SMTP password for that username.                                                                                              |
| **Sender email** | The email address shown in the From field.                                                                                        |
| **Sender name**  | Optional name shown to recipients.                                                                                                |

The supported security pairs are:

* `465 + TLS`
* `587 + STARTTLS`

Save the account and wait for the status to become **Connected**.

<figure><img src="../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>

### Step 3: Choose the email connection

Return to **Create Publish Task**.

The flow has four steps:

1. **Provider**
2. **Connection**
3. **Source and recipient**
4. **Review**

On the **Connection** step:

1. Select **Email** as the provider if it is not already selected.
2. Choose the email connection with the **Connected** status.
3. If there is only one connected Email account, AutoForward selects it automatically.
4. If the account shows **Reconnect required**, reconnect it before continuing.

If no account is available, select **Add connection**. If the connection list cannot be loaded, use **Refresh connections** and try again.

<figure><img src="../.gitbook/assets/image (276).png" alt=""><figcaption></figcaption></figure>

### Step 4: Choose Telegram sources and recipient

<figure><img src="../.gitbook/assets/image (277).png" alt=""><figcaption></figcaption></figure>

On **Source and recipient**:

#### Select Telegram sources

1. Tap or click the source selector.
2. Select one or more Telegram chats.
3. Confirm the selection.

You must select at least one source. Multiple selected sources are included in the same Email Publish Task.

#### Enter the email recipient

Enter the address that should receive messages from the selected Telegram sources.

The recipient address is separate from the connected sender account. For example:

* Connected sender: `notifications@your-company.com`
* Recipient: `team@your-company.com`

AutoForward validates the address before the task can be created.

Email Publish always uses these content rules:

* **New messages only**.
* Attachments up to **8 MiB per file**.
* Up to **20 MiB of attachments per source message**.
* Telegram edits and deletes are not mirrored.
* Old Telegram messages are not automatically sent after setup.

### Step 5: Review and create the task

On the **Review** step:

1. Enter a clear task name, such as `Telegram News to Email`.
2. Check the provider: **Email**.
3. Check the selected connection.
4. Check the number and names of Telegram sources.
5. Check the Email recipient.
6. Confirm the content rules and attachment limits.
7. Select **Create Publish Task**.

After creation, AutoForward opens the Publish Task detail screen. The task is ready to run according to its current status.

<figure><img src="../.gitbook/assets/image (278).png" alt=""><figcaption></figcaption></figure>

### Manage the Email Publish Task

Open the task from the Publish list to view its details.

#### Start or stop publishing

Use the task status controls in the detail screen:

* **Start Publish** starts the task.
* **Stop Publish** pauses the task.
* A stopped task does not send messages until it is started again.

#### Change the email recipient

Open **Edit Publish Task**, update the Email recipient in the Source and recipient step, then save the task.

#### Customize the email subject

Email tasks can have their subject generated in three ways from the Email subject section in task details:

* **Smart**: AutoForward chooses a useful subject automatically.
* **Task label**: Uses the Publish Task name.
* **Custom prefix**: Adds your prefix before the first line of the Telegram message.

Save the subject settings after making a change. The task's other destinations and source settings remain unchanged.

#### Reconnect an email account

If the task or connection shows **Reconnect required**:

1. Open the task detail or **Platform accounts**.
2. Select the affected Email connection.
3. Choose **Reconnect** or **Edit**.
4. Enter the Gmail App Password or SMTP password again.
5. Save and wait until the status becomes **Connected**.
6. Return to the task and start it if it was stopped.

### Troubleshooting

#### Gmail says the password is invalid

Make sure you entered a Gmail **App Password**, not your regular Google password. Confirm that 2-Step Verification is enabled and generate a new App Password if necessary.

#### The Email connection cannot be selected

Only connections with the **Connected** status can be selected. Open **Platform accounts**, refresh the list, and reconnect the account if it shows **Reconnect required**.

#### The task was created but no email arrived

Check the following:

1. The task status is running.
2. The recipient address is correct.
3. The email is not in Spam or Junk.
4. The connected Gmail or SMTP account is still Connected.
5. The new Telegram message is within the attachment limits if it includes files.

#### Older Telegram messages were not sent

This is expected. Email Publish sends new messages only and does not replay messages that existed before the task started.

#### Custom SMTP cannot be saved

Check that:

* The SMTP host is a public DNS hostname.
* Port `465` is paired with **TLS**.
* Port `587` is paired with **STARTTLS**.
* The username and password are correct.
* The Sender email is a valid email address.

### Security reminders

* Never share your Gmail App Password or SMTP password.
* Do not include credentials in screenshots or support messages.
* Use a dedicated sending account when possible.
* If you think a credential has been exposed, revoke it with your email provider and reconnect the account with a new credential.
