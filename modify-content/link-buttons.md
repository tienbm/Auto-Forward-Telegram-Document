---
icon: link
---

# Link Buttons

{% hint style="success" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

### How to Add and Manage Link Buttons

This feature allows you to create interactive buttons within your Telegram messages, which is not supported by default in Telegram.

{% hint style="warning" %}
**Important: This feature requires** [**Bot Sender**](setup-sender-for-task.md)**. You must use Bot Sender mode in your task —Telegram does not allow link buttons with personal accounts.**
{% endhint %}

{% embed url="https://youtu.be/aMM17T86lX4" %}

#### **Step 1: Access the Link Buttons Feature**

1. Open an existing  Task.
2. Scroll down to the "features" section.
3. Select "Link Buttons".

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

#### **Step 2: Adding New Buttons**

1. Click on "Add now" to add a new button.
2. Enter the desired button title (e.g., "Buy Now", "Learn More") in the "Title" field.
3. Enter the URL you want the button to link to in the "URL" field.
4. Click "Add" to save the button.

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

#### **Step 3: Customizing Button Layout**

You can arrange the buttons in several layout styles:

* Vertical Linear Layout: Buttons will be stacked on top of each other vertically.
* Grid Layout: Display a specific number of buttons per row (e.g., two or three buttons). You can select the number of buttons per row from a dropdown menu.
* Custom Mode: Provides full control. You can set the exact number of buttons per row and arrange them by dragging and dropping. Each row will have an "Add Row" button to create new rows and drag buttons into them.

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

#### **Step 4: Editing and Deleting Buttons**

* Edit: Click on a button to edit its title or URL.
* Delete: Click on the trash to delete it. In Custom Mode, you can also delete entire rows using a similar icon next to the row.

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

#### **Step 5: Customize Display Settings**

* "Hide when replying": By default, the buttons will be hidden if the message is sent as a reply to another message. You can toggle this setting off to keep the buttons visible even in replies. A checkbox controls this option.

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

#### **Step 6: Message Button Filters**

**Message Button Filters** allow you to control when inline buttons appear on forwarded messages. You can hide buttons based on specific message types, giving you precise control over button visibility.

<figure><img src="../.gitbook/assets/image (2) (1).png" alt="" width="435"><figcaption></figcaption></figure>

**Key Features**

* **Selective Button Display**: Show/hide buttons based on message content type
* **19 Filter Options**: Comprehensive filters for all Telegram message types
* **Smart Detection**: Automatically detects message characteristics
* **Combine Filters**: Use multiple filters together for complex rules

**Available Filters**

**Media Filters**

| Filter              | Description                  | Example             |
| ------------------- | ---------------------------- | ------------------- |
| **Photo Only**      | Single photo without caption | Product image       |
| **Photo with Text** | Photo with caption           | Image + description |
| **Photos**          | Multiple photos (2-10)       | Photo gallery       |
| **Album**           | Media album (mixed media)    | Photos + videos     |
| **Video**           | Video file                   | Tutorial video      |
| **Animation**       | GIF/animated image           | Funny GIF           |
| **Sticker**         | Telegram sticker             | Emoji sticker       |
| **Audio**           | Audio file                   | Music track         |
| **Document**        | File attachment              | PDF, ZIP file       |
| **Video Note**      | Round video message          | Video message       |

**Message Type Filters**

| Filter         | Description           | Example           |
| -------------- | --------------------- | ----------------- |
| **Text**       | Text-only message     | "Hello world"     |
| **Emoji Only** | Only emoji characters | "🎉😊👍"          |
| **Link**       | Contains URL          | Message with link |
| **Poll**       | Poll/quiz message     | Vote poll         |

**Message Context Filters**

| Filter               | Description              | Example                     |
| -------------------- | ------------------------ | --------------------------- |
| **Forwards**         | Forwarded message        | "Forwarded from X"          |
| **Reply**            | Reply to another message | Reply chain                 |
| **Button**           | Message with buttons     | Message with inline buttons |
| **Without Username** | Anonymous sender         | No sender info              |
| **Outgoing**         | Sent by you              | Your own messages           |

**How It Works**

**Basic Logic**

```
IF message matches ANY selected filter
THEN hide buttons
ELSE show buttons
```

**Example:**

* Enable: "Photo Only" + "Video"
* Result: Buttons hidden on photos and videos, shown on text/other media

**Once you have finished adding and arranging your link buttons, you need to save your changes.**

***

### **Replace Links with Affiliate Links (Crypto)**

This is where the money comes in.

Let’s say the original message contains button link this:

<figure><img src="https://cdn-images-1.medium.com/max/800/1*5LYvgEGuE3r8aC3AXJjAVw.png" alt=""><figcaption></figcaption></figure>

```
https://mevx.io/solana/tokenxyz?ref=NNjWO5SCjGDB
```

With AutoForward, you can **automatically clone these buttons**, and even better — **replace their links with your own affiliate/referral links.**

Here’s how to do it:

#### **Step 1: Access the Link Buttons Feature**

1. Open an existing Task.
2. Scroll down to the “features” section.
3. Select “Link Buttons”.

<figure><img src="https://cdn-images-1.medium.com/max/800/0*QpjMR4japTCcAqIq" alt=""><figcaption></figcaption></figure>

#### **Step 2: Adding New Buttons**

1. Click on “Add now” to add a new button.
2. Enter the desired button title (e.g., “Buy Now”) in the “Title” field.
3. Enter the URL you want the button to link to in the “URL” field (e.g., “https://mevx.io/solana/tokenxyz?ref=yourusername”).
4. Click “Add” to save the button.

<figure><img src="https://cdn-images-1.medium.com/max/800/1*HFrV99OCW6UrxNDd7uqLXQ.png" alt=""><figcaption></figcaption></figure>

> _✅ You can use the special shortcode \[\[CONTRACT\_ADDRESS]] to dynamically insert the token address detected from the original message or button._

> _This saves time and ensures every button always points to the correct token, even if you’re forwarding multiple tokens across different messages._

#### Finalizing and Saving Your Settings

After you have added your link buttons and customized their layout, be sure to scroll to the bottom of the page and click the "Done" or "Save" button. This action will save all of your changes and apply the button configuration to your auto post task.

Once saved, all new posts created by this task will include the link buttons you just set up.
