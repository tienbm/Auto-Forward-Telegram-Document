---
description: >-
  Use these patterns and logic conditions to block messages that match specific
  keywords, links, or combinations.
icon: comments-question-check
---

# FAQ

{% hint style="warning" %}
Note:

* Always enable Regex Mode when using these patterns.
* Use \bword\b to match a full word only.
* Escape special characters like . → \\. when needed.
{% endhint %}

#### 🚫 Q: How do I block messages containing any link?

Regex Pattern:

```
(http|https|www)\S+
```

Example Message:

> Visit https://example.com for more info.

❌ Result: Blocked

***

#### ⚠️ Q: How do I block messages with words like “scam” or “fraud”?

Regex Pattern:

```
(scam|fraud)
```

Example Message:

> This is a fraud alert.

❌ Result: Blocked

***

#### 🧠 Q: How do I block messages that contain both “buy” and “cheap”?

Regex Pattern:

```
^(?=.*\bbuy\b)(?=.*\bcheap\b).*
```

Example Message:

> Buy this product for a cheap price!

❌ Result: Blocked

***

#### ✅ Q: How to block messages that contain both “buy” AND “cheap”?

Setup:

* Condition 1: buy
* Add AND → cheap

Example Message:

> Buy this product for a cheap price!

❌ Result: Blocked

***

#### 🔁 Q: How to block messages that contain either “spam”OR “ad”?

Setup:

* Condition 1: spam
* Add OR → ad

Example Message:

> This is a spam message with an ad.

❌ Result: Blocked

***

#### 🧩 Q: How to combine multiple AND/OR conditions?

Setup:

* Condition 1: buy
* AND → cheap
* OR → scam

Example Messages:

| Message                             | Result        |
| ----------------------------------- | ------------- |
| Buy this product for a cheap price! | ❌ Blocked     |
| This is a scam message              | ❌ Blocked     |
| Buy now                             | ✅ Not blocked |
