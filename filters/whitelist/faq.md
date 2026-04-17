---
description: >-
  Here are some useful Regex patterns to help you filter and forward messages
  based on specific content.
icon: comments-question-check
---

# FAQ

{% hint style="warning" %}
Note:

* Always enable Regex Mode when using these patterns.
* Use \bword\b to match a full word only.
* Escape special characters like . → \\. when needed.
{% endhint %}

#### 🔗 Q: How do I forward messages that contain Telegram links?

Regex Pattern:

```
(telegram\.me|t\.me)/\w+
```

Example Message:

> Join us at https://t.me/example\_channel.

✅ Result: Message will be forwarded.

***

#### ⚫ Q: How do I forward messages that contain either “black” or “white”?

Regex Pattern:

```
(black|white)
```

Example Message:

> The shirt is black, and the shoes are white.

✅ Result: Message will be forwarded.

***

#### **📌 Q: How to match the word “es” as a whole word only?**

Regex Pattern:

```
\bes\b
```

Example Message:

> This is es.

✅ Result: Message will be forwarded.

***

#### 🧠 **Q: How to forward messages that contain both “work1” and “work2”?**

Regex Pattern:

```
^(?=.*\bwork1\b)(?=.*\bwork2\b).*
```

Example Messages:

* ✅ _I have work1 to do and work2 as well._
* ✅ _work1 and work2 are both important._
* ❌ _Only work1 is complete._ → Not forwarded

***

🎨 Q: How do I forward messages that contain either “red” or “blue”?

Regex Pattern:

```
(red|blue)
```

Example Message:

> The car is blue.

✅ Result: Message will be forwarded.

***

