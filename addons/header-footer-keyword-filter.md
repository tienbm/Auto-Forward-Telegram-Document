---
icon: puzzle-piece
---

# Header/Footer Keyword Filter

### Overview

Header/Footer Keyword Filter lets you forward or block messages based on keywords found at the beginning (header) or end (footer) of messages. This is perfect for filtering spam signatures, forwarding only priority messages, or blocking content from specific sources.

#### What It Does

* **Header filtering**: Check first few lines of message for keywords
* **Footer filtering**: Check last few lines of message for keywords
* **Blacklist mode**: Block messages containing specific keywords
* **Whitelist mode**: Only forward messages containing specific keywords
* **Regex support**: Use advanced patterns for complex matching
* **Case options**: Case-sensitive or case-insensitive matching

#### Key Benefits

✅ **Block spam signatures** - Filter out messages with known spam footers\
✅ **Priority forwarding** - Only forward messages with specific headers ("URGENT:", "PREMIUM:")\
✅ **Source filtering** - Block/allow based on source signatures in footers\
✅ **Pattern matching** - Use regex for flexible filtering rules\
✅ **Separate control** - Different rules for headers vs footers\
✅ **Flexible logic** - Blacklist to block, whitelist to allow only

***

### Getting Started

#### Prerequisites

1. ✅ Purchase Header/Footer Keyword Filter addon
2. ✅ Have an active forwarding task
3. ✅ Know what keywords/patterns you want to filter

#### Quick Setup

**Step 1: Purchase & Enable**

1. Menu → My Addons → Header/Footer Keyword Filter → Unlock
2. Open your task settings
3. Find **Header/Footer Filter** section
4. Configure your filtering rules

**Step 2: Choose Header or Footer**

**Header Filter**: Scans the **first 2-3 lines** of message\
**Footer Filter**: Scans the **last 2-3 lines** of message

Or use **both** for comprehensive filtering.

**Step 3: Choose Blacklist or Whitelist**

**Blacklist (Block Mode)**:

* Enter keywords to BLOCK
* Messages containing these keywords will NOT be forwarded
* Use when you know what to block

**Whitelist (Allow-Only Mode)**:

* Enter keywords to ALLOW
* ONLY messages containing these keywords will be forwarded
* Use when you know what to forward

**Step 4: Enter Keywords**

Enter one keyword per line:

```
SPAM
Promotion
Join our channel
Click here
```

Or use **regex** for advanced patterns (enable "Use Regex" option):

```
promo.*discount
\d{10,}  (10+ digit numbers)
http[s]?://bit\.ly
```

**Step 5: Configure Options**

**Use Regex**: ON/OFF

* **OFF**: Plain text matching (simpler, faster)
* **ON**: Regex pattern matching (flexible, powerful)

**Ignore Case**: ON/OFF

* **ON**: "SPAM" matches "spam", "Spam", "SPAM"
* **OFF**: Must match exact case

***

### Configuration Details

#### Header vs Footer

**Header** (beginning of message):

* First 2-3 lines
* Typically contains: titles, labels, priorities, source identifiers
* Examples:
  * "🚨 URGENT SIGNAL"
  * "Premium Members Only"
  * "\[Verified Source]"

**Footer** (end of message):

* Last 2-3 lines
* Typically contains: signatures, credits, promotional links, channel tags
* Examples:
  * "Join @ChannelName for more"
  * "Powered by XYZ"
  * "👉 https://promo-link.com"

**Lines considered**: \~2-3 lines (implementation may vary), enough to catch typical headers/footers.

#### Blacklist Mode (Block)

**How it works**:

1. Check if header/footer contains any blacklisted keyword
2. If YES → Block (don't forward)
3. If NO → Forward normally

**When to use**:

* Block spam patterns: "Join our channel", "Free premium"
* Block specific sources: "\[SourceName]", "via @SpamChannel"
* Block promotional content: "discount", "click here", urls

**Example - Block spam footers**:

```
Footer Blacklist:
- Join @
- Subscribe to
- Click here
- http://bit.ly
```

Result: Any message ending with these patterns is blocked.

#### Whitelist Mode (Allow-Only)

**How it works**:

1. Check if header/footer contains any whitelisted keyword
2. If YES → Forward
3. If NO → Block (don't forward)

**When to use**:

* Forward only priority: "URGENT", "PREMIUM", "VIP"
* Forward only verified sources: "\[Verified]", "Official"
* Forward only specific categories: "NEWS", "ANALYSIS"

**Example - Only forward premium signals**:

```
Header Whitelist:
- PREMIUM
- VIP SIGNAL
- URGENT
- 🔥 HOT
```

Result: Only messages starting with these keywords are forwarded.

#### Combining Header & Footer Filters

You can use both simultaneously:

**Example - Premium signals without spam**:

```
Header Whitelist:
- PREMIUM
- VIP

Footer Blacklist:
- Join @
- Subscribe
```

Result: Forward only messages with premium headers AND without spam footers.

**Logic**: ALL conditions must be met:

* Header must match whitelist (if configured)
* Footer must match whitelist (if configured)
* Header must NOT match blacklist (if configured)
* Footer must NOT match blacklist (if configured)

#### Plain Text vs Regex

**Plain Text Matching** (Regex OFF):

* Simple substring search
* "spam" matches "This is spam message"
* Fast, easy to configure
* Recommended for simple keywords

**Regex Matching** (Regex ON):

* Advanced pattern matching
* `promo.*discount` matches "promo code discount", "promotional discount"
* `\d{10,}` matches any 10+ digit number
* `http[s]?://` matches URLs
* Flexible but complex
* Recommended for advanced users

**Common regex patterns**:

```
\b(spam|scam|fraud)\b     → Whole word match
\d{10,}                    → 10+ digit numbers (phone numbers)
http[s]?://bit\.ly         → bit.ly URLs
^\[.*\]                    → Messages starting with [brackets]
.*join.*channel.*          → "join...channel" in any order
```

#### Case Sensitivity

**Ignore Case ON** (recommended):

* "SPAM" matches "spam", "Spam", "SPAM", "SpAm"
* Easier to configure
* Catches more variations

**Ignore Case OFF**:

* "SPAM" only matches "SPAM"
* Useful for exact matching
* Stricter filtering

***

### Common Use Cases

#### Block Spam Signatures

**Scenario**: Source channels add promotional links at the end of every message.

**Setup**:

```
Footer Blacklist (plain text, ignore case ON):
- Join @channelname
- Subscribe to
- Click here
- t.me/
- bit.ly
```

**Result**: Messages with these spam signatures in footer are blocked.

***

#### Forward Only Premium Signals

**Scenario**: Mixed channel with free and premium content, only want premium.

**Setup**:

```
Header Whitelist (plain text, ignore case ON):
- PREMIUM
- VIP
- 💎
- PAID SIGNAL
```

**Result**: Only messages starting with premium indicators are forwarded.

***

#### Filter by Source Identifier

**Scenario**: Aggregator channel mixes multiple sources, only want specific ones.

**Setup (allow specific sources)**:

```
Footer Whitelist (plain text, ignore case ON):
- Source: TrustedChannel
- [Verified]
- Official Source
```

**Setup (block specific sources)**:

```
Footer Blacklist (plain text, ignore case ON):
- Source: SpamChannel
- [Unverified]
- Reposted from
```

**Result**: Control which sources get forwarded based on footer tags.

***

#### Block URL Spam (Regex)

**Scenario**: Block messages with shortened URLs in footer.

**Setup**:

```
Footer Blacklist (regex ON, ignore case ON):
- http[s]?://bit\.ly
- http[s]?://tinyurl\.com
- http[s]?://t\.me/\+
```

**Result**: Messages with these URL patterns in footer are blocked.

***

#### Priority-Only Forwarding

**Scenario**: Forward only urgent/important messages from busy source.

**Setup**:

```
Header Whitelist (plain text, ignore case ON):
- URGENT
- IMPORTANT
- CRITICAL
- 🚨
- ⚠️
```

**Result**: Only messages marked as priority are forwarded, noise is filtered.

***

### Troubleshooting

#### Issue: Not Blocking Expected Messages

**Check**:

* [ ] Addon is enabled in task settings
* [ ] Keywords are in correct section (header vs footer)
* [ ] Using blacklist (not whitelist)
* [ ] "Ignore Case" is ON if case varies
* [ ] Keywords match actual content (check source messages)

**Test**: Use very simple keyword you know exists (e.g., "test") to verify filtering works.

***

#### Issue: Blocking Too Many Messages

**Problem**: Whitelist is too strict, most messages blocked.

**Solutions**:

* Add more whitelist keywords
* Switch to blacklist mode (block only known bad patterns)
* Use regex for flexible matching (e.g., `.*premium.*` to catch variations)
* Check if keywords really appear in header/footer (not in middle of message)

***

#### Issue: Regex Not Working

**Check**:

* [ ] "Use Regex" option is enabled
* [ ] Regex syntax is correct (test with online regex tester)
* [ ] Special characters are escaped: `.` → `\.`, `?` → `\?`
* [ ] Regex matches content in header/footer (not full message)

**Common mistakes**:

* Forgetting to escape special chars: `http://` should be `http[s]?://`
* Regex too broad: `.*` matches everything
* Regex too specific: won't catch variations

**Test regex**: Use online tools like regex101.com before adding to addon.

***

#### Issue: Same Keyword in Header and Footer

**Problem**: Need different rules for header vs footer but keyword appears in both.

**Solution**:

* Use more specific keywords/patterns
* Add context: "Footer: keyword" vs just "keyword"
* Use regex anchors: `^keyword` (start), `keyword$` (end)
* Combine with other filters (content filter, sender filter)

***

#### Issue: Unclear What Counts as Header/Footer

**Header**: Approximately first 2-3 lines of message\
**Footer**: Approximately last 2-3 lines of message

**Tips**:

* Single-line messages: Entire message is both header and footer
* Long messages: Only edges are checked, middle is ignored
* Media captions: Caption text is checked (if present)

**Test**: Forward sample messages and check which get through to understand line boundaries.

***

### Best Practices

#### Start with Blacklist Mode

Easier to start with:

1. Forward everything initially
2. Notice spam patterns in footer
3. Add to blacklist incrementally
4. Monitor and adjust

Whitelist mode requires knowing ALL valid patterns upfront (harder).

#### Use Plain Text First

* Start with simple keyword lists
* Only use regex if plain text doesn't work
* Regex is powerful but complex and error-prone

#### Ignore Case by Default

Unless you have specific reason:

* Turn "Ignore Case" ON
* Catches more variations
* Easier to configure

#### One Keyword Per Line

Format:

```
spam
promotion
click here
```

NOT:

```
spam, promotion, click here
```

#### Test with Known Messages

Before going live:

1. Find sample messages you want to block/allow
2. Configure filter
3. Test with those specific messages
4. Adjust until correct

#### Combine with Other Filters

Header/Footer filter works best with:

* **Keyword filter**: Filter message body content
* **Sender filter**: Filter by source channel
* **Media filter**: Filter by media type Together = comprehensive filtering

#### Document Your Rules

Keep notes on why each keyword was added:

* "Join @" - blocks spam channel promotions
* "PREMIUM" - whitelist for paid signals Helps when revisiting settings months later.

***

### Frequently Asked Questions

#### What counts as header vs footer?

**Header**: First \~2-3 lines of message text\
**Footer**: Last \~2-3 lines of message text

Exact line count may vary by implementation. For single-line messages, the entire message is both header and footer.

#### Does it check media captions?

**Yes**, if message has media with caption, the caption text is checked for header/footer keywords.

#### Can I use multiple keywords?

**Yes**, enter one keyword per line. If ANY keyword matches, the rule triggers.

#### Does it work with forwarded message credits?

**Depends**. If forwarded message retains source credit as text (e.g., "Forwarded from ChannelName"), that text may be part of header/footer. Test to verify.

#### Blacklist vs whitelist - which is better?

**Blacklist** (block mode):

* Better when you know what to block
* Easier to start with
* Forwards everything except blacklist

**Whitelist** (allow-only mode):

* Better when you know exactly what to forward
* More restrictive
* Blocks everything except whitelist

**Recommend**: Start with blacklist, switch to whitelist if you have clear "allow only" criteria.

#### Can I use both blacklist and whitelist?

**Yes**, both header and footer can have separate blacklist and whitelist rules. All conditions must be met for message to forward.

#### Does order of keywords matter?

**No**, all keywords are checked equally. First match triggers the rule.

#### How do I match exact phrases?

**Plain text mode**: Enter the exact phrase, enable "Ignore Case" if needed

```
Join our channel
```

**Regex mode**: Use word boundaries for exact match

```
\bJoin our channel\b
```

#### Can it filter emojis?

**Yes**, emojis are treated as text. Copy-paste the emoji into keyword field:

```
🚫
💎
🚨
```

#### Does it slow down forwarding?

**Minimal impact**. Header/footer checking is very fast since only edges of message are scanned (not full message body).

***

### Performance Tips

#### Keep Keyword Lists Short

* 5-10 keywords per list is ideal
* 20+ keywords may slow down processing
* Use regex to consolidate similar patterns

#### Use Specific Keywords

More specific = fewer false positives:

* ✅ "Join @ChannelName for exclusive"
* ❌ "join" (too broad, matches "join the discussion")

#### Combine with Sender Filter

Don't rely on header/footer filter alone:

* Filter by sender first (faster)
* Then apply header/footer filter (precise)

#### Test Regex Performance

Complex regex can be slow:

* Test with online regex tools
* Avoid catastrophic backtracking patterns (e.g., `(.*)*`)
* Keep patterns simple

***

### Getting Help

If header/footer filtering isn't working as expected:

1. Verify addon is active and enabled in task
2. Check your keywords actually appear in header/footer (not middle of message)
3. Test with very simple keyword you know exists
4. Review blacklist vs whitelist logic
5. Check Addons FAQ
6. Contact support with:
   * Your filter configuration (keywords, regex, options)
   * Sample message that should be filtered but isn't (or vice versa)
   * Expected vs actual behavior

**Support**: Menu → Help & Support or support@autoforwardtelegram.com

***

### Summary

Header/Footer Keyword Filter provides precision filtering based on message edges:

✅ **Block spam** - Filter out promotional footers and signatures\
✅ **Priority forwarding** - Only forward messages with specific headers\
✅ **Source control** - Filter by source tags in headers/footers\
✅ **Flexible matching** - Plain text or regex patterns\
✅ **Dual modes** - Blacklist to block, whitelist to allow\
✅ **Case options** - Case-sensitive or insensitive matching

**Perfect for**: Spam filtering, priority message forwarding, source-based filtering, signature detection, promotional content blocking.

**Quick start**:

1. Enable addon in task
2. Decide header or footer filtering
3. Choose blacklist (block) or whitelist (allow-only)
4. Enter keywords (one per line)
5. Enable "Ignore Case"
6. Keep regex OFF (unless needed)
7. Test and refine

***

**Last Updated**: March 2026\
**Addon Version**: 1.0\
**App Version**: 1.0.44+
