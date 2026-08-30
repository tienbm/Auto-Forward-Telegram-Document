---
icon: whatsapp
---

# How to Auto Forward Telegram to WhatsApp

{% hint style="info" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

AutoForward can send new messages from one or more Telegram sources to a WhatsApp contact, group, or newsletter. Connect your WhatsApp account by scanning a QR code, choose the destination, create a **Publish Task**, and send a test message.

This guide uses AutoForward's current QR-based WhatsApp connection. You do not need to enter a Phone number ID or Access token in this connection flow.

### What you need

Before you begin, prepare:

* An AutoForward account that is signed in and connected to Telegram.
* Access to the Telegram channel, group, or chat that you want to monitor.
* An active **External Publish** addon.
* An active WhatsApp account on the phone that you will use to scan the QR code.
* Permission to view and send messages to the WhatsApp contact, group, or newsletter that should receive the messages.

### How it works

```
Telegram source(s) → AutoForward Publish Task → WhatsApp connection → WhatsApp destination
```

WhatsApp Publish has a few important rules:

* It publishes **new messages only** after the task is created.
* Each task uses one WhatsApp destination: a **Contact**, **Group**, or **Newsletter**.
* WhatsApp receives the message text or caption. Telegram binary media files are not sent.
* Telegram message edits and deletes are not mirrored to WhatsApp.
* AutoForward supports one WhatsApp connection. If a WhatsApp connection already exists, it is reused.

### 1. Open Publish and manage connections

1. Open AutoForward and go to **Home**.

<figure><img src="../.gitbook/assets/image (325).png" alt=""><figcaption></figcaption></figure>

1. Select **Publish**.
2. On the Publish Tasks page, select **Manage Accounts**.
3. Confirm that the **Platform Accounts** page opens.
4. Select **Add Account**.

If **External Publish** is not active, complete the addon unlock flow and return to **Publish**.

<figure><img src="../.gitbook/assets/image (326).png" alt=""><figcaption></figcaption></figure>

### 2. Add a WhatsApp connection

On the account form:

1. Under **Select Platform**, choose **WhatsApp**.
2. Enter an **Account Name**, such as `Main WhatsApp`.
3. Read the connection note, then select **Add connection**.

AutoForward creates the connection and opens the WhatsApp QR screen. The QR code is temporary and may expire while you are setting up the connection.

Only one WhatsApp connection is supported. If AutoForward finds an existing WhatsApp connection, it reuses that connection instead of creating a second one.

<figure><img src="../.gitbook/assets/image (328).png" alt=""><figcaption></figcaption></figure>

### 3. Link WhatsApp by scanning the QR code

When the **WhatsApp connection** screen displays the QR code:

1. Keep the AutoForward QR screen open.

<figure><img src="../.gitbook/assets/image (329).png" alt=""><figcaption></figcaption></figure>

1. On your primary phone, open WhatsApp.
2. Open **Linked devices**:
   * **Android**: open the menu, then select **Linked devices → Link a device**.
   * **iPhone**: open **Settings**, then select **Linked devices → Link a device**.
3. If WhatsApp asks you to verify your identity, complete the verification on your phone.
4. Point the phone at the QR code shown by AutoForward.
5. Wait for the connection status to change to **Connected**.

WhatsApp's menu names can vary slightly by device and app version. See the official [WhatsApp Help Center instructions for linking a device](https://faq.whatsapp.com/1317564962315842/?cms_platform=android) if you cannot find **Linked devices**.

<figure><img src="../.gitbook/assets/image (330).png" alt=""><figcaption></figcaption></figure>

#### If the QR code expires

The QR code has a limited lifetime. If it expires before you scan it:

1. On the WhatsApp connection screen, select **Retry** or **Reconnect**, depending on the status shown.
2. Wait for a new QR code.
3. Repeat the phone steps above.

If the connection shows **Reconnect required**, select **Reconnect** and scan the new QR code. Do not create another WhatsApp account.

When the account is connected, return to **Platform Accounts** or continue to the Publish Task wizard.

### 4. Create a WhatsApp Publish Task

On the Publish Tasks page, select **Create Publish Task**. AutoForward opens a four-step wizard:

1. **Provider**
2. **Connection**
3. **Source and recipient**
4. **Review**

#### Step 1 — Choose WhatsApp as the provider

1. On the **Provider** step, select **WhatsApp**.
2. Select **Next**.

<figure><img src="../.gitbook/assets/image (331).png" alt=""><figcaption></figcaption></figure>

#### Step 2 — Choose the WhatsApp connection

1. On the **Connection** step, select the WhatsApp account with the **Connected** status.
2. If no connection is available, select **Add connection**, complete the QR flow, and return to the wizard.
3. If the connection shows **Reconnect required**, select **Reconnect connection**, scan a new QR code, and refresh the connection list.
4. Select **Next** after the account is connected.

Only a connected WhatsApp account can be used for a Publish Task.

<figure><img src="../.gitbook/assets/image (332).png" alt=""><figcaption></figcaption></figure>

#### Step 3 — Select Telegram sources and a WhatsApp destination

**Select Telegram sources**

1. On **Source and recipient**, open the Telegram source selector.
2. Select one or more Telegram channels, groups, or chats.
3. Confirm that the required sources appear as selected.

**Choose the WhatsApp destination**

1. In **Where should messages be published?**, select **Choose WhatsApp destination**.
2. In the **Select WhatsApp destination** screen, choose one destination:
   * **Contact**
   * **Group**
   * **Newsletter**
3. Use **Search by name or ID** when the destination list is long.
4. You can also filter the list by **Contact**, **Group**, or **Newsletter**.
5. Select the destination row.
6. Select **Use this destination**.

The selected destination appears in the task form. To replace it, select **Change destination** and choose another destination. The current flow stores one WhatsApp destination per task.

If the destination picker is empty, confirm that the WhatsApp connection is **Connected**, refresh the list, and try again.

<figure><img src="../.gitbook/assets/image (333).png" alt=""><figcaption></figcaption></figure>

WhatsApp settings are intentionally limited to the supported delivery policy:

* **New messages only** is enabled.
* Telegram edits and deletes are not mirrored.
* Telegram binary media is not sent; only message text or a media caption can be delivered.

#### Step 4 — Review and create the task

On **Review**, check:

* The **Task Name**, for example `Telegram Announcements to WhatsApp`.
* **Provider**: WhatsApp.
* **Connection**: the correct account with **Connected** status.
* **Source and recipient**: the correct Telegram source count and names.
* **Target**: the intended WhatsApp contact, group, or newsletter.
* **New messages only**.

Select **Create Publish Task** when the configuration is correct.

<figure><img src="../.gitbook/assets/image (334).png" alt=""><figcaption></figcaption></figure>

### 5. Test the forwarding flow

After creation, AutoForward opens the Publish Task detail screen.

1. Confirm that the task status is **Running**.
2. Send a new text test message to one of the selected Telegram sources.
3. Open the selected WhatsApp destination.
4. Confirm that the message appears.

For a media test, send a message with a caption and confirm that the text or caption is delivered. The Telegram binary media file itself is not forwarded to WhatsApp.

If the task is **Stopped**, select **Start Publish**, wait for the status to change to **Running**, and send a new test message. Messages sent before the task was created are not automatically reposted.

### Manage the connection and task

#### Reconnect WhatsApp

If the connection expires or shows **Reconnect required**:

1. Open **Publish → Manage Accounts**.
2. Find the WhatsApp account in **Platform Accounts**.
3. Select **Reconnect** or open the account and select the reconnect action.
4. Scan the new QR code with WhatsApp.
5. Wait for **Connected**, then refresh the Publish Task connection list.

WhatsApp can also be reconnected from the **Connection** step by selecting **Reconnect connection**.

#### Stop or start the task

* **Stop Publish** pauses the task. It does not forward messages while stopped.
* **Start Publish** resumes the task.

Stopping a task does not unlink the WhatsApp account.

#### Change the source or destination

1. Open the task from **Publish Tasks**.
2. Select the edit icon or **Edit Publish Task**.
3. Update the Telegram source or select **Change destination**.
4. Select **Update**.

#### Delete the task

1. Open the task detail screen.
2. Open the task actions and select **Delete**.
3. Confirm the deletion.

Deleting a Publish Task removes the automation from AutoForward. It does not delete your WhatsApp account, contacts, groups, or newsletters.

### Common statuses

| Status or action       | Meaning                                                              | What to do                                                  |
| ---------------------- | -------------------------------------------------------------------- | ----------------------------------------------------------- |
| **Connected**          | AutoForward can use the WhatsApp connection.                         | Continue creating or running the task.                      |
| **Pending**            | The WhatsApp connection is waiting for QR pairing to finish.         | Keep the QR screen open and scan it from the primary phone. |
| **Reconnect required** | The WhatsApp session needs to be linked again.                       | Select **Reconnect** and scan a new QR code.                |
| **Running**            | The Publish Task is monitoring Telegram and publishing new messages. | Send a new test message.                                    |
| **Stopped**            | The Publish Task is paused.                                          | Select **Start Publish**.                                   |

### Troubleshooting

#### The QR code is not displayed

Wait for the connection screen to finish loading. If the screen shows an error, select **Refresh connections** or return to the account form and select **Add connection** again. If an existing WhatsApp connection is present, open that connection and select **Reconnect** instead of creating another one.

#### WhatsApp cannot scan the QR code

Check that:

1. WhatsApp is open on the primary phone.
2. You used **Linked devices → Link a device**.
3. The QR code is fully visible on the AutoForward screen.
4. The QR code has not expired.
5. The phone camera can focus on the screen.

If the QR code has expired, select **Retry** or **Reconnect** to generate a new one.

#### The destination list is empty

1. Confirm that the WhatsApp account shows **Connected**.
2. Open **Choose WhatsApp destination** again.
3. Pull down to refresh the destinations.
4. Clear the search field and set the filter to **All**.
5. Confirm that the desired contact, group, or newsletter is available to the linked WhatsApp account.

#### The task is running but no WhatsApp message arrives

1. Confirm that the task status is **Running**.
2. Send a new message after the task was created; older messages are not reposted.
3. Confirm that the message was sent to one of the selected Telegram sources.
4. Confirm that the intended WhatsApp destination is still selected.
5. Test with a plain text message first.
6. Remember that Telegram binary media is not sent to WhatsApp.

#### The WhatsApp connection shows Reconnect required

Open **Platform Accounts**, select **Reconnect**, scan the new QR code, and wait for **Connected**. Then refresh the connection list in the Publish Task. Do not delete and recreate the task unless the task configuration itself is no longer needed.

### Frequently asked questions

#### Can I send to a WhatsApp contact, group, or newsletter?

Yes. Choose one destination in **Select WhatsApp destination** and confirm it with **Use this destination**.

#### Can one task send to multiple WhatsApp destinations?

The current WhatsApp flow uses one destination per task. Create separate Publish Tasks when you need different WhatsApp destinations.

#### Can I forward old Telegram messages?

No. WhatsApp Publish starts with new messages after the task is created.

#### Are photos, videos, and files forwarded?

No. WhatsApp Publish sends text or a media caption only. Telegram binary media files are not sent.

#### Do Telegram edits and deletes update WhatsApp?

No. The WhatsApp delivery policy processes new messages only and does not mirror source edits or deletes.

#### Do I need a Phone number ID or Access token?

No. The current AutoForward WhatsApp connection uses QR pairing from **WhatsApp → Linked devices → Link a device**.

### Security and privacy reminders

* Treat every QR code as a temporary session credential. Never share or publish a live QR code.
* Do not send screenshots containing private WhatsApp chats, phone numbers, profile names, or linked-device details.
* Only connect a WhatsApp account that you are authorized to use.
* Review WhatsApp's linked devices regularly and remove any device you do not recognize.
* Use a harmless test message before enabling a production forwarding task.
