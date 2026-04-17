---
icon: puzzle-piece
---

# Auto Clone Button

### Overview

Auto Clone Button automatically copies inline buttons from source messages to your forwarded messages. This preserves call-to-action (CTA) buttons, purchase links, sign-up forms, and any interactive elements that make your content engaging.

#### What Problem Does It Solve?

When forwarding messages that contain buttons, you face these challenges:

❌ **Buttons disappear** when forwarding normally\
❌ **CTAs are lost** - your audience can't click through to products/services\
❌ **Affiliate links don't transfer** - you lose tracking and commissions\
❌ **User engagement drops** - no easy way for audience to take action\
❌ **Manual button creation** is tedious and error-prone

Auto Clone Button solves all of these automatically.

#### Key Benefits

✅ **Preserve engagement** - Keep all interactive elements\
✅ **Maintain affiliate links** - Don't lose referral commissions\
✅ **Replace URLs automatically** - Convert source links to your own\
✅ **Filter buttons selectively** - Choose which buttons to keep\
✅ **Smart deduplication** - Remove duplicate buttons automatically\
✅ **Flexible layouts** - Control max buttons and rows

***

### How It Works

#### Processing Flow

1. **Message arrives** from source with inline buttons
2. **Bot analyzes** button structure (text, URL, type)
3. **Filters applied** based on your whitelist/blacklist rules
4. **URLs replaced** if you configured replacement patterns
5. **Buttons cloned** to the forwarded message
6. **Deduplication** removes any duplicate buttons (optional)
7. **Layout optimized** within your max buttons/rows limits

#### Technical Details

* **Button types supported**: URL buttons (most common), callback buttons (limited)
* **Per message limit**: Up to 10 buttons / 5 rows (configurable)
* **Processing time**: < 1 second per message (instant for users)
* **URL validation**: Automatic checks for valid URLs
* **Merge modes**: Append to existing buttons or replace completely

***

### Getting Started

#### Prerequisites

Before you can use Auto Clone Button:

1. ✅ Purchase the addon using credits
2. ✅ Have an active forwarding task
3. ✅ Source messages contain inline buttons

#### Quick Start (Recommended for Most Users)

For most users, the "All Buttons Mode" is perfect:

**Step 1: Purchase & Enable**

1. **Menu → My Addons → Auto Clone Button → Unlock**
2. Open your task settings
3. Find **Button Settings** section
4. Toggle **Auto Clone Button** to ON

**Step 2: Choose "All Buttons" Mode**

1. In Button Settings, select Mode: **All Buttons**
2. This will clone every button from source messages
3. No filters needed - simplest setup

**Step 3: Save & Test**

1. Tap **Save**
2. Forward a message with buttons through your task
3. Verify buttons appear in forwarded message
4. Done! 🎉

***

### Operating Modes

Auto Clone Button has **two operating modes**. Choose based on your needs:

#### Mode 1: All Buttons (Recommended)

**What it does**: Clones every button from the source message.

**Best for:**

* Most users who just want to preserve buttons
* Simple, no-configuration-needed setup
* General content forwarding
* Maintaining all CTAs

**Pros:**

* Easiest to set up (5 seconds)
* No configuration needed
* No missed buttons

**Cons:**

* Can't filter out unwanted buttons
* No selective control

**Configuration required**: NONE - just toggle ON

***

#### Mode 2: URL Only (Advanced)

**What it does**: Clones only buttons that match your URL filtering rules.

**Best for:**

* Affiliate marketers who need specific links
* Content curators who filter spam/unwanted links
* Advanced users who need precise control
* Replacing URLs with your own

**Pros:**

* Full control over which buttons appear
* Filter spam or competitor links
* Replace URLs with your tracking links

**Cons:**

* Requires configuration (whitelist/blacklist)
* More complex to set up
* Risk of filtering too much if patterns are wrong

**Configuration required**: Whitelist and/or Blacklist patterns

***

### Configuration Guide: All Buttons Mode

Since this mode requires minimal configuration, focus on these optional settings:

#### Max Buttons

**Default**: 10\
**Range**: 1-20\
**Purpose**: Limit total buttons per message

**When to use:**

* Source sends too many buttons (cluttered appearance)
* You want clean, minimal messages
* Mobile users prefer fewer options

**Example:**

* Source has 15 buttons
* Max Buttons = 5
* First 5 buttons are cloned, rest are ignored

***

#### Max Rows

**Default**: 5\
**Range**: 1-10\
**Purpose**: Limit button rows (Telegram displays buttons in rows)

**How Telegram arranges buttons:**

* Usually 1-3 buttons per row (depends on text length)
* Long button text = 1 button per row
* Short text = 2-3 buttons per row

**Example:**

* Source has 8 buttons arranged in 6 rows
* Max Rows = 3
* First 3 rows are kept (5-6 buttons typically)

***

#### Deduplicate

**Default**: OFF\
**Options**: ON/OFF\
**Purpose**: Remove duplicate buttons automatically

**When to enable:**

* Source sometimes sends same button multiple times
* Multiple similar buttons (e.g., "Buy Now", "BUY NOW", " Buy Now")
* Want clean, non-repetitive interface

**How it works:**

* Compares button URLs (not text)
* If URL matches, button is removed
* First occurrence is kept

***

#### Merge Mode

**Default**: Append\
**Options**: Append / Replace\
**Purpose**: How to handle existing buttons in your forwarded message

**Append** (recommended):

* Cloned buttons are added after any existing buttons
* Useful if you manually add your own buttons to tasks
* Combines source buttons + your custom buttons

**Replace**:

* Cloned buttons replace all existing buttons
* Use if you only want source buttons, nothing else

**Most users**: Keep on **Append**

***

### Configuration Guide: URL Only Mode (Advanced)

This mode gives you powerful filtering and replacement capabilities.

#### Whitelist Patterns

**Purpose**: Only clone buttons whose URLs match these patterns.

**When to use:**

* You want specific domains only (e.g., only Amazon links)
* Filtering for partner/affiliate links
* Only official website buttons

**How to configure:**

1. Enter patterns, separated by commas
2. Use `*` as wildcard

**Pattern examples:**

```
t.me/*
```

**Matches:**

* ✅ t.me/yourchannel
* ✅ t.me/joinchat/abc123
* ❌ telegram.me/channel (different domain)

```
*.example.com/*
```

**Matches:**

* ✅ shop.example.com/product
* ✅ www.example.com/page
* ✅ blog.example.com/article
* ❌ example.org (different TLD)

```
amazon.com/*, amazon.co.uk/*
```

**Matches:**

* ✅ amazon.com/dp/B08XYZ
* ✅ amazon.co.uk/gp/product/123
* ❌ ebay.com (not in pattern)

**Multiple patterns:**

```
t.me/*, *.yoursite.com/*, partner.com/affiliate/*
```

Buttons matching ANY pattern will be cloned.

***

#### Blacklist Patterns

**Purpose**: Exclude buttons whose URLs match these patterns.

**When to use:**

* Remove competitor links
* Filter spam or shortener links
* Block specific domains

**Priority**: Blacklist is checked AFTER whitelist. If a URL matches both, blacklist wins (button is blocked).

**Pattern examples:**

```
bit.ly/*, tinyurl.com/*
```

**Blocks**: All URL shortener links

```
competitor.com/*
```

**Blocks**: All links to competitor.com

```
*.spam-site.com/*
```

**Blocks**: All subdomains of spam-site.com

**Combined example (Whitelist + Blacklist):**

```
Whitelist: t.me/*, *.yoursite.com/*
Blacklist: bit.ly/*, competitor.com/*
```

**Result:**

* ✅ Clones: t.me/yourchannel, shop.yoursite.com/product
* ❌ Blocks: bit.ly/abc, competitor.com/offer
* ❌ Blocks: anyothersite.com (not whitelisted)

***

#### URL Replacement

**Purpose**: Automatically replace parts of button URLs with your own.

**Use cases:**

* Insert your affiliate ID into product links
* Change source channel links to your channel
* Update old domains to new domains
* Add tracking parameters

**How to configure:**

Add replacement rules with **From** and **To** fields:

**Example 1: Affiliate Links**

```
From: exchange.com/trade
To: exchange.com/trade?ref=YOUR_AFFILIATE_ID
```

**Original button**: `https://exchange.com/trade/BTC-USD`\
**Replaced button**: `https://exchange.com/trade/BTC-USD?ref=YOUR_AFFILIATE_ID`

**Example 2: Channel Redirect**

```
From: t.me/oldchannel
To: t.me/yourchannel
```

**Original**: `https://t.me/oldchannel`\
**Replaced**: `https://t.me/yourchannel`

**Example 3: Domain Update**

```
From: shop.oldsite.com
To: shop.newsite.com
```

All buttons pointing to old domain will use new domain.

**Example 4: Tracking Parameters**

```
From: product.com/item
To: product.com/item?utm_source=telegram&utm_campaign=forward
```

Adds Google Analytics tracking to all product links.

***

#### Advanced Replacement Rules

**Multiple replacements**: Add as many rules as needed. Each is applied independently.

**Processing order**:

1. Whitelist/Blacklist filters buttons
2. Remaining buttons have URL replacements applied
3. Buttons are cloned with new URLs

**String matching**:

* Replacements are **exact substring matches**
* Case-sensitive
* Not regex (wildcards don't work in replacements)

**Example - Multiple rules:**

```
Rule 1: 
From: amazon.com
To: amazon.com?tag=yourID

Rule 2:
From: t.me/source
To: t.me/yourname
```

Both rules apply independently to matching URLs.

***

### Common Use Cases

#### Add Affiliate Links

**Example**: Insert referral codes into trading buttons

```
Mode: All Buttons
URL Replacement:
  From: binance.com/trade
  To: binance.com/trade?ref=YOUR_ID
```

#### Filter Trusted Sources Only

**Example**: News aggregation - official sites only

```
Mode: URL Only
Whitelist: *.reuters.com/*, *.bbc.com/*
Blacklist: telegra.ph/*, bit.ly/*
```

#### Replace Links

**Example**: Redirect competitor links to your service

```
Mode: All Buttons
URL Replacement:
  From: competitor.com
  To: yoursite.com
```

#### Add Tracking Parameters

**Example**: Add UTM parameters for analytics

```
URL Replacement:
  From: shop.com/
  To: shop.com/?utm_source=telegram
```

***

### Advanced Features

#### Button Deduplication Logic

When enabled, the system:

1. **Extracts URLs** from all buttons
2. **Normalizes URLs** (removes trailing slashes, converts to lowercase)
3. **Compares** each button URL to previous buttons
4. **Removes** duplicates (keeps first occurrence)

**Example:**

```
Original buttons:
1. "Shop Now" → https://shop.com/product
2. "Buy Here" → https://shop.com/product  (duplicate URL)
3. "View Product" → https://shop.com/item  (different URL)

After deduplication:
1. "Shop Now" → https://shop.com/product  (kept)
3. "View Product" → https://shop.com/item  (kept)
```

***

#### Pattern Matching Deep Dive

**Wildcard rules:**

`*` matches any characters:

* `t.me/*` matches anything starting with `t.me/`
* `*.example.com/*` matches any subdomain of example.com

**Exact matching:**

* No wildcard = must match exactly
* `example.com` matches only `example.com`, not `www.example.com`

**Common mistakes:**

❌ `example.com` (too strict - misses `https://example.com/page`)\
✅ `example.com/*` (correct - matches all pages)

❌ `t.me` (too strict - misses `https://t.me/channel`)\
✅ `t.me/*` (correct - matches all Telegram links)

**Testing your patterns:**

1. Use Preview or test with a few messages first
2. Check which buttons appear/don't appear
3. Adjust patterns if needed

***

#### Merge Mode In-Depth

**Scenario comparison:**

**Setup**: You manually added a "Subscribe to Our Channel" button to your task.

**Append Mode:**

* Your custom button appears first
* Source buttons appear after
* Total: Your button + all cloned buttons

**Replace Mode:**

* Your custom button is removed
* Only source buttons appear
* Total: Only cloned buttons

**Best practice**: Use Append unless you specifically want source buttons only.

***

### Troubleshooting

#### Issue: No Buttons Appearing

**Checklist:**

* [ ] Auto Clone Button is enabled in task settings
* [ ] Addon hasn't expired (check My Addons)
* [ ] Source message actually contains buttons
* [ ] In URL Only mode, check whitelist/blacklist aren't too restrictive
* [ ] Max Buttons isn't set to 0

**Fix:**

1. Switch to "All Buttons" mode temporarily to test
2. If buttons appear now, your filters are too strict
3. Review whitelist/blacklist patterns
4. Test with more permissive patterns

***

#### Issue: Wrong Buttons Are Cloned

**Cause**: Whitelist/Blacklist patterns are too broad or too narrow.

**Fix:**

* **Too many buttons**: Add blacklist patterns to filter unwanted ones
* **Too few buttons**: Broaden whitelist or check blacklist isn't blocking good buttons

**Debug method:**

1. Temporarily use "All Buttons" mode
2. Note which buttons appear
3. Switch back to URL Only
4. Craft patterns to match desired buttons

***

#### Issue: URL Replacement Not Working

**Common causes:**

**1. "From" string doesn't match exactly**

```
❌ From: amazon.com (missing protocol/path)
✅ From: amazon.com/

Button URL: https://amazon.com/dp/B08XYZ
```

**2. Case sensitivity**

```
❌ From: Amazon.com (wrong case)
✅ From: amazon.com

Button URL: https://amazon.com/...
```

**3. Not a substring of URL**

```
❌ From: shop.com
Button URL: https://greatshop.com (doesn't contain "shop.com")
```

**Fix**: Use the exact substring that appears in button URLs.

**Testing tip**: Check source button URLs first, then craft your "From" pattern to match.

***

#### Issue: Pattern Syntax Errors

**Invalid patterns:**

❌ `*.com` (too broad - matches everything)\
❌ `t.me` (missing path - should be `t.me/*`)\
❌ `example.com, www.example.com` (space after comma - should be no space)

**Valid patterns:**

✅ `*.example.com/*`\
✅ `t.me/*,telegram.me/*` (no spaces)\
✅ `amazon.com/*,amazon.co.uk/*`

**Validation**: App will warn you if pattern syntax is invalid when you save.

***

#### Issue: Too Many Buttons (Cluttered)

**Solutions:**

**Option 1: Reduce Max Buttons**

* Set Max Buttons to 3-5 for cleaner appearance
* First few buttons are usually most important

**Option 2: Use URL Only Mode**

* Whitelist only critical button URLs
* Filter out secondary/less important buttons

**Option 3: Reduce Max Rows**

* Set Max Rows to 2-3
* Limits vertical space used by buttons

***

#### Issue: Buttons Showing in Wrong Order

**Explanation**: Auto Clone Button preserves source button order. It doesn't reorder.

**If you need custom order:**

* This isn't possible with Auto Clone Button
* Consider manually creating buttons in task settings
* Or request priority button feature from support

***

#### Issue: Some Button Text Looks Strange

**Explanation**: The addon clones button text exactly as source sends it.

**Common issues:**

* **Emoji issues**: Some emojis may not display correctly
* **Language encoding**: Rare character encoding problems
* **Long text**: Button text might be truncated by Telegram

**These are Telegram limitations**, not addon issues. The addon preserves whatever the source sends.

***

### Best Practices

#### Start with All Buttons Mode

Use this for most cases. Only switch to URL Only mode if you need filtering or URL replacement.

#### Test Before Production

Create a test task, send 5-10 test messages, verify buttons appear correctly, then apply to main task.

#### Pattern Tips

* Use wildcards: `t.me/*`, `*.example.com/*`
* Test patterns with actual source messages first
* Document your working patterns for future reference

#### URL Replacement Tips

* Match exact substrings from button URLs
* Case-sensitive matching
* Test with actual buttons to verify replacement works

#### Use Responsibly

* Don't mislead users with replaced links
* Follow Telegram Terms of Service
* Be transparent about affiliate links
* Respect content creators' rights

#### Combine with Other Addons

* **Crypto**: Auto Clone Button + AlphaGardeners Extract
* **Marketing**: Auto Clone Button + Smart Image Crop + Dialog Broadcast
* **News**: Auto Clone Button + Caption filters

***

### Performance Considerations

#### Processing Speed

* **All Buttons mode**: <0.5s per message (instant)
* **URL Only mode**: \~1s per message (pattern matching)
* **URL Replacement**: +0.5s per replacement rule

**Total**: Usually 1-2s - negligible delay users won't notice.

#### High-Volume Usage

If forwarding 100+ messages/hour:

* **All Buttons** is faster than URL Only
* Keep replacement rules minimal (3-5 max)
* Monitor task performance in Statistics

#### Button Limits

**Telegram's limits** (not addon limits):

* Max \~100 buttons per message (theoretical)
* Practical limit: 10-20 buttons for good UX
* Max text length per button: \~64 characters

**Recommendation**: Set Max Buttons to 5-10 for best user experience.

***

### Frequently Asked Questions

#### Can I clone buttons and modify button text?

**No**. The addon clones buttons exactly as they appear (text and URL). You can replace URLs but not button text.

**Workaround**: Manually create custom buttons in task settings with your preferred text.

#### Do callback buttons work?

**Limited support**. URL buttons (most common) work perfectly. Callback buttons (buttons that trigger bot commands) may not work as expected.

**Why**: Callback buttons are tied to the source bot. When cloned to your message, they won't function (no bot to handle the callback).

**Best for**: URL buttons, which work everywhere.

#### Can I add my own buttons in addition to cloned ones?

**Yes!** Use **Merge Mode: Append**.

1. Add your custom buttons in task settings
2. Enable Auto Clone Button with Append mode
3. Your buttons appear first, cloned buttons appear after

#### Does it work with media groups (albums)?

**Yes**, but buttons apply to the whole group, not individual photos. Telegram limitation.

#### Can I clone buttons from one source to multiple targets?

**Yes!** Configure the addon once in your task. All targets in that task receive the same cloned buttons.

#### What if source changes their button URLs?

**URL Replacement rules still apply** - they replace whatever substring matches, regardless of full URL.

**Example**:

* Rule: From `shop.com/` To `shop.com/?ref=123`
* Works for: `shop.com/productA`, `shop.com/productB`, `shop.com/any-page`

No need to update rules unless domain completely changes.

#### Can I temporarily disable without losing configuration?

**Yes**! Toggle "Auto Clone Button" OFF. All your patterns, replacements, and settings are saved. Toggle back ON anytime to resume with same settings.

#### How do I know which buttons were cloned vs filtered?

**Testing method**:

1. Forward message to a test channel
2. Check which buttons appear
3. Compare with source message
4. Adjust filters if needed

No built-in log, but easy to verify visually.

***

### Getting Help

If you're stuck after reading this guide:

1. **Review Addons FAQ** - More Q\&A
2. **Check Quick Reference** - Pattern examples
3. **Test in isolation** - Create test task, send test messages
4. **Contact support** with:
   * Your whitelist/blacklist patterns
   * Example source message/buttons
   * What you expected vs. what happened
   * Screenshots

**Support channels**:

* In-app: Menu → Help & Support
* Email: support@autoforwardtelegram.com
* Community: Telegram group for user tips

***

### Summary

Auto Clone Button gives you powerful control over button forwarding:

✅ **Preserve engagement** - Keep CTAs and interactive elements\
✅ **Flexible filtering** - Whitelist/blacklist patterns for precision\
✅ **URL replacement** - Automatically insert your affiliate links\
✅ **Smart deduplication** - Clean, non-repetitive button layouts\
✅ **Combine modes** - Use with other addons for powerful workflows

**Key decision**: Start with **All Buttons** mode (simple). Upgrade to **URL Only** mode when you need advanced filtering and replacement.

**Next steps:**

1. Purchase the addon from My Addons
2. Enable in task settings
3. Start with All Buttons mode
4. Test with a few messages
5. Upgrade to URL Only if you need filtering/replacement

**Related documentation:**

* All Addons Overview
* Addons Quick Reference
* Addons FAQ

***

**Last Updated**: March 2026\
**Addon Version**: 1.0\
**App Version**: 1.0.44+
