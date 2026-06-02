---
description: Automatically delete forwarded target messages after a configurable delay
icon: puzzle
---

# Auto Delete Messages

Automatically delete forwarded target messages after a configurable delay. This addon helps keep destination chats clean, remove outdated content automatically, and manage temporary announcements, countdowns, promotions, and event notifications without manual intervention.

### How It Works

When a message is successfully forwarded, Auto Delete Messages can schedule it for automatic removal after a specified delay.

The addon only affects messages sent to destination chats. Original source messages are never modified or deleted.

### Features

#### Automatic Message Deletion

Configure a default delay and all forwarded messages will be automatically deleted after the specified time.

Examples:

* Delete after 5 minutes
* Delete after 1 hour
* Delete after 24 hours
* Delete after 7 days

Supported delay range:

* Minimum: 60 seconds
* Maximum: 30 days

***

#### Keyword-Based Delete Rules

Create custom keyword rules that apply different deletion timers to specific messages.

The system checks the forwarded message text or media caption and applies the first enabled matching rule.

Examples:

| Keywords  | Delete After |
| --------- | ------------ |
| countdown | 10 minutes   |
| sale      | 30 minutes   |
| event     | 1 hour       |
| giveaway  | 6 hours      |

This is especially useful for:

* Countdown messages
* Flash sales
* Promotions
* Temporary announcements
* Event reminders
* Limited-time offers

***

#### Flexible Keyword Matching

Each rule supports two matching modes:

**Any Match**

The rule is triggered when at least one keyword is found.

Example:

Keywords:

* sale
* discount
* promo

Message:

Massive discount available today!

Result:

* Rule matches

**All Match**

The rule is triggered only when every configured keyword is present.

Example:

Keywords:

* bitcoin
* signal

Message:

New bitcoin signal available

Result:

* Rule matches

Message:

New bitcoin update

Result:

* Rule does not match

***

#### Case Sensitive Matching

Enable case-sensitive matching when exact capitalization matters.

Example:

Keyword:

* VIP

Message:

* VIP Access → Match
* vip access → No Match

When disabled, matching ignores letter casing.

***

#### Default Behavior for Unmatched Messages

Choose how messages should be handled when they do not match any keyword rule.

**Delete Unmatched Messages (Recommended)**

Messages that do not match any keyword rule will be deleted using the default delay.

Example:

Default Delay:

* 24 hours

Message:

Daily market update

Result:

* Deleted after 24 hours

**Keep Unmatched Messages**

Only messages matching a keyword rule are deleted.

All other messages remain permanently in destination chats.

***

#### Content Type Filtering

Choose which message types should be processed by the addon.

Supported content types:

* Text
* Photo
* Video
* Document
* Audio
* Voice
* Animation
* Sticker
* Album / Media Groups
* Other Message Types

You can also select All Content Types to apply deletion rules to every supported message.

Examples:

* Delete only promotional photos
* Delete only video announcements
* Delete only text countdown messages
* Apply to all forwarded content

***

#### Automatic Mapping Cleanup

After a message is successfully deleted, the addon can automatically remove its stored forwarding record.

Benefits:

* Reduced database storage
* Improved long-term performance
* Cleaner message mapping data

This option is enabled by default.

***

#### Target-Only Deletion

Auto Delete Messages only deletes messages that were sent to destination chats.

The original source message remains untouched.

This ensures:

* Source channels stay intact
* Source groups remain unchanged
* No accidental source-message deletion
* Safe operation across all forwarding tasks

### Typical Use Cases

#### Temporary Promotions

Forward promotional campaigns and automatically remove them when the offer expires.

#### Countdown Messages

Send countdown updates and automatically remove outdated countdown posts.

#### Event Notifications

Forward event announcements and clean them up after the event has finished.

#### Trading Signals

Automatically delete expired signals after a configured period.

#### Auto-Clean Destination Channels

Keep destination channels organized by removing old content automatically.

### Benefits

* Keep destination chats clean and organized
* Automatically remove expired content
* Support advanced keyword-based retention policies
* Different deletion timers for different message types
* Reduce manual moderation work
* Safe source-message protection
* Fully configurable on a per-task basis

### Configuration Limits

| Setting                | Limit          |
| ---------------------- | -------------- |
| Maximum Keyword Rules  | 20             |
| Keywords Per Rule      | 20             |
| Maximum Keyword Length | 120 Characters |
| Minimum Delete Delay   | 60 Seconds     |
| Maximum Delete Delay   | 30 Days        |

### Example Configuration

Default Delay:

* 24 Hours

Delete Unmatched:

* Enabled

Rule 1:

* Keywords: sale, promo
* Match Mode: Any
* Delete After: 30 Minutes

Rule 2:

* Keywords: event, countdown
* Match Mode: All
* Delete After: 10 Minutes

Results:

Message:

Flash sale starts now

→ Deleted after 30 minutes

Message:

Event countdown begins

→ Deleted after 10 minutes

Message:

Daily market update

→ Deleted after 24 hours

Short Marketplace Description

Automatically delete forwarded messages after a configurable delay. Create keyword-based retention rules, target specific content types, and keep destination chats clean without affecting source messages.
