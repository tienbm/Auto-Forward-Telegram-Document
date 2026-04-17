---
icon: puzzle-piece
---

# AlphaGardeners Extract

### Overview

AlphaGardeners Extract automatically extracts cryptocurrency contract addresses from alphagardeners.xyz URLs in forwarded messages. Perfect for crypto signal channels that share token launches via AlphaGardeners links.

#### What It Does

* Detects alphagardeners.xyz links in messages
* Visits the link and extracts the contract address
* Adds extracted data to your forwarded message
* Optionally formats as full DEXScreener URL
* Works automatically with every message

#### Key Benefits

✅ **Automatic extraction** - No manual copy/paste\
✅ **Fast processing** - Configurable timeout (5-30s)\
✅ **Two output modes** - Contract only or full DEX URL\
✅ **Seamless integration** - Works with forwarding workflow\
✅ **Time-saving** - Process 100s of signals automatically

***

### Getting Started

#### Prerequisites

1. ✅ **Crypto Filter must be enabled** in your task (required)
2. ✅ Purchase AlphaGardeners Extract addon
3. ✅ Source messages contain alphagardeners.xyz links

#### Quick Setup

**Step 1: Enable Crypto Filter**

1. Open your task settings
2. Find **Crypto Filter** section
3. Toggle **Enable Crypto Filter** to ON
4. Save task

**Important**: AlphaGardeners Extract will NOT work without Crypto Filter enabled.

**Step 2: Purchase & Enable Addon**

1. Menu → My Addons → AlphaGardeners Extract → Unlock
2. Return to task settings
3. Find **AlphaGardeners Extract Settings**
4. Toggle **Enable** to ON

**Step 3: Configure Extract Mode**

Choose your preferred output:

**Contract Only** (recommended for advanced users):

* Returns just the contract address
* Example: `0x1234abcd5678ef90...`
* Clean, minimal output

**Full DEX URL** (recommended for most users):

* Returns clickable DEXScreener link
* Example: `https://dexscreener.com/ethereum/0x1234abcd...`
* Users can click directly to chart

**Step 4: Set Timeout**

**Timeout** (seconds): How long to wait for extraction

* Range: 5-30 seconds
* Default: 10 seconds
* **Recommended**: 10s for normal speed, 15-20s if often timing out

**Step 5: Save & Test**

Save settings and forward a test message with alphagardeners.xyz link. Extracted data appears in forwarded message.

***

### Configuration Details

#### Extract Modes

**Contract Only Mode**

**Output format**:

```
Contract Address: 0x742d35Cc6634C0532925a3b844Bc9e7595f0bEb2
```

**Best for**:

* Advanced crypto users who know what to do with addresses
* Integration with trading bots
* Clean, data-focused output
* Users who manually go to DEXScreener/DEXTools

**Full URL Mode**

**Output format**:

```
📊 DEXScreener: https://dexscreener.com/ethereum/0x742d35Cc6634C0532925a3b844Bc9e7595f0bEb2
```

**Best for**:

* General audience (easy one-click access)
* Users unfamiliar with contract addresses
* Maximum convenience
* Higher engagement (clickable links)

**Recommendation**: Use **Full URL mode** unless you have specific reason to use Contract Only.

#### Timeout Configuration

**What it does**: Maximum time bot waits for alphagardeners.xyz page to load and extract address.

**Timing guidance**:

* **5s**: Very fast, may timeout on slow connections
* **10s**: Default, works 95% of the time
* **15s**: Safer for slower sources or networks
* **20-30s**: Very safe but slows message forwarding

**If you get frequent timeouts**: Increase by 5s increments until successful.

***

### How It Works

#### Processing Flow

1. **Message arrives** with alphagardeners.xyz link
2. **Bot detects** the AlphaGardeners URL
3. **Bot visits** the URL in background
4. **Page loads** and bot extracts contract address from the page
5. **Format output** based on your Extract Mode setting
6. **Add to message** - extracted data appended to forwarded message
7. **Forward** complete message with contract address/link

**Processing time**: 3-10 seconds typically (depends on timeout and AlphaGardeners site speed)

#### Requirements Check

Before extraction, bot verifies:

* ✅ Crypto Filter is enabled
* ✅ AlphaGardeners Extract is enabled
* ✅ Message contains alphagardeners.xyz URL
* ✅ Addon hasn't expired

If any check fails, message forwards normally without extraction.

***

### Common Use Cases

#### Crypto Signal Channel

**Setup**:

```
Extract Mode: Full DEX URL
Timeout: 10s
```

**Result**: Followers get one-click access to token charts.

#### Trading Bot Integration

**Setup**:

```
Extract Mode: Contract Only
Timeout: 10s
```

**Result**: Clean contract addresses for bot processing.

#### Multi-Chain Support

**Note**: AlphaGardeners Extract works for any chain AlphaGardeners supports (Ethereum, BSC, etc.). DEXScreener link automatically includes correct chain.

***

### Troubleshooting

#### Issue: Extraction Not Working

**Check**:

* [ ] Crypto Filter is enabled (required)
* [ ] AlphaGardeners Extract is enabled
* [ ] Message contains alphagardeners.xyz URL (not other sites)
* [ ] Addon hasn't expired

**Fix**: Enable both Crypto Filter and addon. Test with known AlphaGardeners link.

***

#### Issue: Timeout Errors

**Symptoms**: Message forwards without extracted address, or you see timeout error.

**Causes**:

* AlphaGardeners site is slow
* Network connection issues
* Timeout setting too low

**Fix**:

* Increase timeout to 15-20s
* Check your internet connection
* Try again later if AlphaGardeners site is having issues

***

#### Issue: Wrong/Invalid Address

**Rare but possible causes**:

* AlphaGardeners page structure changed
* Link leads to invalid/deleted token page
* Extraction parsing error

**Fix**:

* Verify the AlphaGardeners link works in browser
* Contact support if issue persists with valid links
* Check for app updates (extraction logic may be updated)

***

#### Issue: Slowing Down Forwarding

**Explanation**: Extraction adds 3-10s per message (normal behavior).

**If too slow**:

* Reduce timeout to 5-8s (accept more timeouts)
* Or accept the delay (ensures successful extraction)

**Trade-off**: Speed vs. reliability. Most users prefer reliability (10s timeout).

***

### Best Practices

#### Always Enable Crypto Filter First

AlphaGardeners Extract will not work without Crypto Filter. Enable it before purchasing the addon.

#### Use Full URL Mode for Better Engagement

Clickable DEX links get more user engagement than raw contract addresses.

#### Set Realistic Timeouts

10s is optimal for most cases. Only reduce if speed is critical and you can tolerate occasional timeouts.

#### Test with Real Links

Before going live, test with actual alphagardeners.xyz links from your sources to verify extraction works.

#### Monitor Extraction Success Rate

Check forwarded messages occasionally to ensure addresses are extracting correctly.

#### Combine with Button Clone

Extract contract address + Clone "Buy" buttons = complete trading info for your audience.

***

### Limitations

#### Only AlphaGardeners Links

Currently supports **alphagardeners.xyz only**. Other crypto sites:

* DEXScreener - not supported
* DEXTools - not supported
* Poocoin - not supported
* Others - not supported

**Future**: More sites may be added based on user demand.

#### Requires Internet Access

Bot must load AlphaGardeners page, so it requires active internet connection.

#### Subject to AlphaGardeners Changes

If AlphaGardeners changes their page structure, extraction may break temporarily until addon is updated.

***

### Frequently Asked Questions

#### Does it work for all blockchains?

Yes, as long as AlphaGardeners supports that blockchain. DEXScreener link includes correct chain automatically (Ethereum, BSC, Polygon, etc.).

#### What if AlphaGardeners link is broken/deleted?

Extraction fails and message forwards without extracted address. No error message shown to avoid confusion.

#### Can I extract from multiple links in one message?

Yes! If message has multiple alphagardeners.xyz links, bot extracts all of them.

#### Does it slow down forwarding significantly?

Adds 3-10s per message. For high-volume forwarding (100+ msg/hour), this is noticeable but usually acceptable.

#### Can I disable temporarily without losing settings?

Yes, toggle "Enable" to OFF. All settings preserved. Toggle back ON anytime.

#### What happens when addon expires?

Extraction stops. Messages forward normally without extraction. Your settings are saved for when you renew.

***

### Getting Help

If extraction isn't working:

1. Verify Crypto Filter is enabled (most common issue)
2. Test timeout at 15s or 20s
3. Try with a known-working AlphaGardeners link
4. Check Addons FAQ
5. Contact support with:
   * The AlphaGardeners link you're testing
   * Your current settings (Extract Mode, Timeout)
   * What happens vs. what you expect

**Support**: Menu → Help & Support or support@autoforwardtelegram.com

***

### Summary

AlphaGardeners Extract automates contract address extraction:

✅ **Requirement**: Crypto Filter must be enabled first\
✅ **Two modes**: Contract Only or Full DEXScreener URL\
✅ **Configurable timeout**: Balance speed and reliability\
✅ **Automatic**: Works on every message with AlphaGardeners links\
✅ **Perfect for**: Crypto signal channels, trading groups, token launch alerts

**Next steps**:

1. Enable Crypto Filter
2. Purchase AlphaGardeners Extract
3. Choose Full URL mode (recommended)
4. Set 10s timeout
5. Test with real AlphaGardeners links

***

**Last Updated**: March 2026\
**Addon Version**: 1.0\
**App Version**: 1.0.44+
