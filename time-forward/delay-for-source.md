---
icon: calendar-clock
---

# Delay For Source

{% hint style="warning" %}
The **Delay For Sources** feature is designed to delay messages from a source chat before they are forwarded to target chats. This helps manage the timing of message delivery, ensuring a smoother distribution of messages across target chats, and also reduces the risk of Telegram account limitations.
{% endhint %}

{% hint style="success" %}
### **Download Mobile App or use Web**

✅ **iOS** → [App Store](https://apps.apple.com/us/app/autoforward-for-telegram/id6447486093)\
✅ **Android** → [Google Play](https://play.google.com/store/apps/details?id=com.autoforward.telegramforward)\
✅ **Web** → [web.autoforwardtelegram.com](https://web.autoforwardtelegram.com/)
{% endhint %}

{% tabs %}
{% tab title="Instructions" %}
**Follow these steps**

1. Open application **AutoForward for Telegram**
2. At list Task Forward **choose Task you want set Delay For Source**
3. At screen detail Task choose **Set** **Delay Feature**

<div align="left"><figure><img src="../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure></div>

4. **Next choose Delay for Source**

<div align="left"><figure><img src="../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure></div>

5. **At here choose Mode and enter delay second want set and click Done**

{% code title="Delay Mode" overflow="wrap" %}
```
Normal Mode: Bot will used by same Boost Performance configuration

Delay Mode: This mode is used by default. On this mode, Delay messages exactly the time they are received + delayed amount. This means that if the source sends 100 messages at once, with a 10 second delay bot will send 100 messages after 10 seconds.

Spread Mode: In this mode, Bot will spread messages evenly. This means that if the source sends 100 messages and you have a delay of 10 seconds set. Bot will delay each message 10 second from the last one.

Separate Mode: In this mode, each message has its own independent delay. For example, if you set 5 minutes, a message received at 9:00 will be sent at 9:05, while a message received at 9:01 will be sent at 9:06.
```
{% endcode %}

<div align="left"><figure><img src="../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure></div>

And that's it!
{% endtab %}
{% endtabs %}
