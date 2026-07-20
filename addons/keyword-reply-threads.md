---
icon: puzzle
---

# Keyword Reply Threads

Keyword Reply Threads keeps forwarded trading signals and their updates organized in one Telegram reply thread.

When a new trade signal is detected, it is forwarded normally to your target chat. Later updates for that trade are forwarded as replies to the original signal, making them easy to follow.

### Example

Your source channel sends:

> Gold Sell Now 3994

This message is forwarded to your target chat as a normal message and becomes the main message for this trade.

Later, the source sends:

> Stop loss moved to entry\
> Running profit: 30 pips

These updates are forwarded as replies to the original “Gold Sell Now 3994” message.

When the source sends:

> All target complete done

This message is also forwarded as a reply, then the trade thread is closed.

### How to set it up

1. Open the Auto Forward app.
2. Select the forwarding task you want to set up.
3. At section **Addons**.
4. Choose **Keyword Reply Threads**.
5. Follow the setup questions.

### Settings explained

#### Start keywords

These words or phrases identify a new trade signal and open a reply thread.

Example:

`sell now|buy now`

Any source message containing “sell now” or “buy now” can start a new thread.

#### Close keywords

These words or phrases close the current trade thread after the message is forwarded.

Example:

`done|target complete|all target complete`

#### Max reply messages

This sets how many later messages can be attached to a trade thread.

* Enter `10` to allow up to 10 updates.
* Enter `0` for no message limit.

#### Time limit

This sets how long a thread stays active before it closes automatically.

Recommended setting:

`24`

This means the thread remains active for 24 hours.

#### Max active trades

This controls how many trade threads can be open at the same time.

For most users, use:

`1`

Use `2` or more only when your source provider sends updates as replies to the original trade signal, or to a message already inside that trade’s reply chain.

### Recommended first setup

* Start keywords: `sell now|buy now`
* Close keywords: `done|target complete|all target complete`
* Max reply messages: `10`
* Time limit: `24` hours
* Max active trades: `1`

### Important note for multiple trades

If more than one trade is active, the system needs the source reply structure to identify which update belongs to which trade.

For example:

1. Source sends: `Gold Sell Now 3994`
2. Source sends: `Gold Buy Now 3996`
3. An update replying to the Sell signal will be forwarded as a reply to the Sell thread.
4. An update replying to the Buy signal will be forwarded as a reply to the Buy thread.

If the source sends a normal message that does not reply to either trade, the system will not guess which thread it belongs to. This prevents updates from being attached to the wrong trade.

### Before and after

Before using Keyword Reply Threads, forwarded updates appear as separate messages and can be difficult to follow.

After configuring the addon, updates are grouped as replies under the correct forwarded trade signal—when the source reply chain identifies that trade.
