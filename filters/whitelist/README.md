---
icon: badge-check
---

# Whitelist

{% hint style="success" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

The **Whitelist** feature allows you to define a list of **approved users, groups, or channels** whose messages will be forwarded. This ensures that only content from specific sources is included in the forwarding process, helping you filter and control message flow effectively.

***

### **How It Works**

* When you add a user, group, or channel to the **Whitelist**, their messages will be forwarded.
* Messages from sources **not on the Whitelist** will be ignored.
* If no Whitelist is set up, messages from all sources are forwarded (unless other filters like Blacklist are applied).

***

### **1. Accessing the Replace Feature** <a href="#id-1.-accessing-the-replace-feature" id="id-1.-accessing-the-replace-feature"></a>

**On Mobile App**

1. Open the [Auto Forward mobile app](https://docs-v2.autoforwardtelegram.com/mobile-app/how-to-download-app-for-mobile).
2. Go to the **Dashboard**.
3. Tap on the  **Whitelist** icon (highlighted below).

<div align="left"><figure><img src="../../.gitbook/assets/image (42).png" alt="" width="375"><figcaption></figcaption></figure></div>

**On Web Dashboard**

1. Log in to the [Auto Forward Web](https://web.autoforwardtelegram.com/) Dashboard.
2. In the left-hand menu under **Features**, click on **Whitelist**.

<div align="left"><figure><img src="../../.gitbook/assets/image (41).png" alt="" width="375"><figcaption></figcaption></figure></div>



Next Tap on the **Add New** button (as shown in the image below):

<div align="left"><figure><img src="../../.gitbook/assets/image (44).png" alt="" width="375"><figcaption></figcaption></figure></div>

## **2. Create Whitelist Rule**

<figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

#### **Options for Blacklist Apply To**

1.  **Post:**&#x20;

    ```
    Check each message one by one — both original posts and replies.
    ```
2.  **Reply:**&#x20;

    <pre data-overflow="wrap"><code>Check only the first post in a thread. If it matches, all its replies will be forwarded
    </code></pre>

#### **Options Whitelist Type**

You can choose one of the following **Whitelist Types**:

* **Basic**: Add simple words or phrases to the whitelist.
* **Regex**: Use Regular Expressions (Regex) for advanced filtering.
* **Whitelist by User**: Whitelist messages from specific users.

### **1.  Enter a Label**

* Add a **Label** to identify your whitelist rule.
* Example: `trusted_words` or `filter_links`.

### **2.**  Select Whitelist Type

* **Basic**: Enter one or more words (separate them with commas).
  * Example: `hello,cat,dog`.
* **Regex**: Use a regex pattern for advanced filtering.
  * Example: `\bhello\b` (matches the word "hello" fully).

### **3.**  Full Content (Optional)

* You can paste the original content to test or match against the rule.

### **4.**  Apply to Tasks (Optional)

* In the **Apply For Task** field, select a specific task if needed.

### **5. Save the Rule**

* Tap **Create Whitelist** to save and activate the rule.

## **4. Whitelist Type**

### **1. Basic Whitelist**

The **Basic Whitelist** allows you to forward messages containing specific words or phrases.

#### **Steps to Use**

1. Go to **Whitelist** → Tap **Add New**.
2. Select **Basic** in the **Whitelist Type** dropdown.
3. Add the words/phrases to the **Content Whitelist** field.
4. Tap **Create Whitelist** to save.

<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

**Example Scenarios**

* **Forward messages containing "news" or "alert"**
  * **Content Whitelist**: `news,alert`
  *   **Example Message**:

      ```csharp
      Breaking news: Market is rising fast!  
      ```
  * **Result**: Forwarded ✅
* **Forward messages containing "update" or "report"**
  * **Content Whitelist**: `update,report`
  *   **Example Message**:

      ```sql
      Daily update: Please check the sales report.  
      ```
  * **Result**: Forwarded ✅

***

### **2. Regex Whitelist**

The **Regex Whitelist** is used for advanced matching. allows you to match complex patterns, not just exact words — giving you more control and flexibility when filtering.

{% hint style="info" %}
Using Regex requires basic knowledge of regular expressions. If you’re unsure, use Simple Mode instead.

> Need help with Regex? Test patterns at [regex101.com](https://regex101.com) or learn from [regexone.com](https://regexone.com)
{% endhint %}

If you’re not confident with writing regular expressions, you can ask AI platforms to help you generate them.

Recommended tools:

*   🧠 [ChatGPT](https://chat.openai.com) – just ask:

    > _E.g: “Write a regex to match hashtags starting with # and ending with space.”_
* 🤖 [Google Gemini](https://gemini.google.com)

🔍 These tools can explain, test, and even fix your regex patterns for you.

#### **Steps to Use**

1. Go to **Whitelist** → Tap **Add New**.
2. Select **Regex** in the **Whitelist Type** dropdown.
3. Enter the **Regex pattern** in the **Content Whitelist** field.
4. Tap **Create Whitelist** to save.

<figure><img src="../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

**Combine with many condition AND, OR**

<figure><img src="../../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>

**What are AND and OR Conditions?**

1. **AND Condition**:
   * Ensures that all specified conditions must be met for a message to pass the Whitelist filter.
   * Example: A message must contain **"BUY"** **and** **"SL: 13213"**.
2. **OR Condition**:
   * Ensures that any one of the specified conditions is met for a message to pass the Whitelist filter.
   * Example: A message must contain **"BUY"** **or** **"SELL"**.

***

**Add AND/OR Conditions**

1.  **To Add an AND Condition**:

    * Tap the **+ AND** button to add another condition that must also be met.
    * Example: After entering `BUY`, add `SL: 13213`.

    **Result**: The message must include both **"BUY"** **and** **"SL: 13213"** to pass the filter.
2.  **To Add an OR Condition**:

    * Tap the **+ OR** button to add another condition where either can be met.
    * Example: After entering `BUY`, add `SELL`.

    **Result**: The message must include either **"BUY"** **or** **"SELL"** to pass the filter.

<figure><img src="../../.gitbook/assets/image (206).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
If your pattern includes special characters (like ., +, or spaces), escape them with \\. Example: x5\\+, hello\ world.
{% endhint %}

#### [**Checkout Example Scenarios**](faq.md)

***

## **5.** Apply/Disable Replace For a Task

The **Whitelist** feature allows you to control which messages are forwarded based on **keywords, regex patterns, or specific users**. This guide explains how to apply or disable Whitelist rules for individual tasks or globally across all tasks.

#### **Step 1: Access the Whitelist List**

1. From the **Dashboard**, select the **Whitelist** feature.
2. You will see a list of all previously created **Whitelist rules**.

<figure><img src="../../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

***

#### **Step 2: Select a Whitelist Rule**

1. Locate the Whitelist rule you want to manage.
2.  Tap or click on the rule.

    A **popup window** will appear, displaying the details of the selected Whitelist rule.

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

***

#### **Step 3: Manage the Whitelist Rule for Tasks**

In the popup window, the following options are available:

1. **Activate/Deactivate For Task** (Green Button)
   * Use this option to enable or disable the Whitelist rule for a specific task.
   * If the rule is already **active**, clicking this will deactivate it for the selected task.
   * If the rule is **inactive**, clicking this will activate it for the selected task.

***

2. **Apply For All Tasks** (Blue Button)
   * This option allows you to apply the Whitelist rule to **all existing tasks**.
   * Use this feature when you want the Whitelist rule to work globally across all tasks.

***

3. **Edit Whitelist** (Orange Button)
   * Tap this option to **edit the Whitelist rule**.
   * You can update the label, content keywords, regex patterns, or user-specific rules.

***

4. **Delete** (Red Button)
   * Use this option to **delete** the Whitelist rule permanently.
   * Be cautious: once deleted, the rule cannot be recovered.

## **6. Tips for Using Whitelist**

1. Use **Basic** for simple word-based filtering.
2. Use **Regex** for more complex patterns (e.g., URLs, mentions, or exact word matches).
3. Be precise with Regex to avoid matching unintended content.
4. Test your Regex patterns on [regex101.com](https://regex101.com) before applying them.
5. Add clear and descriptive **Labels** for easier rule management.

***

### **Why Use Whitelist?**

* Ensure only relevant content is forwarded.
* Filter messages based on specific words, patterns, or trusted users.
* Improve control and accuracy of message forwarding.

