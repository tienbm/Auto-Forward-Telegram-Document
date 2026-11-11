---
description: Match changing words, usernames, or links with a regular expression.
icon: wand-magic-sparkles
---

# Use Regex — Replace Text Patterns

Choose **Use Regex** when one rule should match several words or a changing text pattern. A regular expression (Regex) describes what to find; the replacement tells AutoForward what to put in its place.

### Create the rule

1. Open **Replace** from the Dashboard (mobile) or Features menu (web), then select **Add New** to open **Create Replace**.
2. Set **Replace Type** to **Use Regex**.
3. Enter a short **Label**, such as `change_words`, without spaces.
4. Enter `(good|perfect)` in **Original Words**. The vertical bar means “or”.
5. Enter `bad` in **New Words Replace**.
6. Paste a sample into **Full Content Original** if available, and check the matches before saving.
7. Choose the intended task under **Apply For Task**, then select **Create Replace**.

### Example: match either word

**Before:** This is a good day, everything is perfect.

**Pattern:** `(good|perfect)`\
**Replacement:** `bad`

**After:** This is a bad day, everything is bad.

### Example: replace links and mentions

**Pattern:** `(@|www|https?)S+`\
**Replacement:** `@Auto_Forward_Messages_Bot`

**Before:** Visit https://example.com or contact @username for more info.

**After:** Visit @Auto\_Forward\_Messages\_Bot or contact @Auto\_Forward\_Messages\_Bot for more info.

This example matches text starting with @, www, http, or https up to the next space. Test punctuation and actual message formatting; a hidden clickable link may not have the same text as its destination URL.

### Check the result

Confirm that the saved rule is applied to the intended task, then forward a sample message and inspect the destination. Turn off **Show Header Forwarder** for tasks using Replace. To stop using the rule for a task, deactivate its task assignment in the Replace list; the saved rule remains available.

### If the output is unexpected

Check capitalization and Regex options, then try a smaller pattern. Special characters such as `.`, `+`, and parentheses have special meanings in Regex. If you only need to change one fixed phrase, choose **Basic**. For capture groups and advanced formatting, see the examples on the parent Replace Content page.
