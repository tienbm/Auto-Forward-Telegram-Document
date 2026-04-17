---
icon: users
---

# Whitelist Users

{% hint style="success" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

The **Whitelist By User** feature allows you to forward messages only from specific users, channels, or groups that you select. By using a Whitelist, you can specify which users' messages should be forwarded using their **USER\_ID** or **USERNAME**.

***

#### **How to Use Whitelist By User**

To forward messages only from selected users, follow these steps:

1.  **Find the User ID** of the users you want to whitelist:

    * Open the chat where you want to forward messages from specific users.
    * Use the command **`/getid`** in the chat.
    * Note down the **User ID** that appears in the response.



    <div align="left"><figure><img src="../.gitbook/assets/ezgif-4-1f4543bdbc.gif" alt=""><figcaption></figcaption></figure></div>



    **Example**:

    ```
    /getid

    ➡️ User ID: 123456789
    ```



    **Note**<mark style="color:orange;">: Make sure you are using a Telegram account connected to the</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**AutoForward Telegram Bot**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">to execute the</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**/getid**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">command.</mark>


2. **Create a Whitelist Rule** in the app:
   * Go to **Dashboard** → Tap on **Whitelist** → **Add New**.
   * Select **Whitelist By User** as the **Whitelist Type**.
   * In the **Content Whitelist** field:
     * Enter the **User ID** (e.g., `123456789`) or the **Username** (e.g., `@trusted_user`).
   * Tap **Create Whitelist** to save the rule.

<div align="left"><figure><img src="../.gitbook/assets/image (48).png" alt="" width="563"><figcaption></figcaption></figure></div>

***

#### **Example Scenario**

**Use Case**: Forward messages only from a trusted user.

* **Content Whitelist**: `123456789` or `@trusted_user`
*   **Example Message**:

    ```
    Hello, here is the latest report.  
    ```
* **Result**:
  * If sent by the whitelisted user (`123456789` or `@trusted_user`): Forwarded ✅
  * If sent by any other user: Blocked ❌

***

#### **Why Use Whitelist By User?**

* Allows you to control and limit message forwarding to trusted users only.
* Ensures your forwarded messages are from verified and relevant sources.
* Enhances filtering accuracy by targeting specific **User IDs** or **Usernames**.
