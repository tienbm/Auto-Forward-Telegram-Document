---
icon: puzzle-piece
---

# Cross-Group CA Matching

### Overview

Cross-Group CA Matching (Contract Address Matching) is a specialized addon for crypto signal aggregators. It forwards messages only when the same contract address (CA) appears in multiple source groups within a time window, indicating genuine projects with cross-community validation.

#### What It Does

* **Detects contract addresses** - Automatically extracts CAs from messages
* **Cross-group validation** - Checks if CA appears in multiple source groups
* **Time window** - CA must appear in X groups within Y hours
* **Duplicate prevention** - Blocks repeated CA forwards from same group
* **Cooldown period** - Prevents spam after initial forward
* **Quality signals** - Only forwards CAs validated by multiple communities

#### Key Benefits

✅ **Reduce noise** - Only forward CAs mentioned by multiple groups\
✅ **Validation signal** - Multiple mentions = stronger signal\
✅ **Prevent spam** - Block duplicate CA posts from same source\
✅ **Trend detection** - Catch tokens gaining multi-group attention\
✅ **Auto-aggregation** - No manual cross-checking needed\
✅ **Scam reduction** - Less likely scam if multiple groups mention it

***

### Getting Started

#### Prerequisites

1. ✅ Purchase Cross-Group CA Matching addon
2. ✅ Have a forwarding task with **multiple source groups** (2+ groups)
3. ✅ Sources discuss crypto tokens with contract addresses
4. ✅ Understand basic crypto concepts (CA, tokens, chains)

**Important**: This addon requires **2 or more source groups** to work. Single-source tasks won't benefit from cross-group matching.

#### Quick Setup

**Step 1: Purchase & Enable**

1. Menu → My Addons → Cross-Group CA Matching → Unlock
2. Open your task settings (must have multiple source groups)
3. Find **Cross-Group CA Matching** section
4. Toggle **Enable CA Matching** to ON

**Step 2: Configure Minimum Groups**

**Min Groups**: How many different groups must mention the CA

* **2 groups** (default): CA must appear in at least 2 different sources
* **3-5 groups**: Higher validation, fewer but higher quality signals
* **6-10 groups**: Very strict, only widely-discussed tokens

**Recommended**: Start with 2-3 groups, increase if too many signals.

**Step 3: Set Time Window**

**Time Window**: How long to wait for CA to appear in required groups

* **1-6 hours**: Fast-moving markets, trending tokens
* **12-24 hours**: Moderate pace, daily trending topics
* **48-168 hours** (2-7 days): Long-term validation, slower markets

**Recommended**: 12-24 hours for balanced signal quality.

**Step 4: Configure Cooldown**

**Cooldown Period**: After forwarding a CA, how long to block additional forwards of same CA

* **30 minutes - 2 hours**: Allow multiple mentions if news develops
* **6-12 hours**: Standard, prevents spam but allows significant updates
* **24+ hours**: Strict, only one mention per day per CA

**Recommended**: 12 hours for good spam prevention.

**Step 5: Duplicate Prevention**

**Auto Duplicate Prevention**: ON (recommended)

* Blocks repeated CA posts from the **same source group**
* Prevents single group from spamming same CA
* Cross-group mentions still counted

***

### Configuration Details

#### How CA Detection Works

The addon automatically detects contract addresses in messages:

**Ethereum-like CAs** (Ethereum, BSC, Polygon, etc.):

```
0x742d35Cc6634C0532925a3b844Bc9e7595f0bEb
0xdAC17F958D2ee523a2206206994597C13D831ec7
```

Format: `0x` followed by 40 hexadecimal characters

**Solana CAs**:

```
EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v
Es9vMFrzaCERmJfrF4H2FYD4KCoNkY11McCe8BenwNYB
```

Format: Base58 string, typically 32-44 characters

**Bitcoin/Other**: May vary by implementation

**Auto-extraction**: No manual configuration needed. Addon scans all incoming messages for CA patterns.

#### Minimum Groups Logic

**How it works**:

1. Message arrives with CA `0xABC...`
2. Addon checks: "Has `0xABC...` appeared in other source groups?"
3. Counts unique groups that mentioned this CA within time window
4. If count >= minimum groups → Forward
5. If count < minimum groups → Hold (wait for more mentions)

**Example (Min Groups = 2)**:

```
10:00 - Group A mentions CA 0xABC... → Count: 1 → Hold
10:30 - Group B mentions CA 0xABC... → Count: 2 → FORWARD ✅
11:00 - Group C mentions CA 0xABC... → Count: 3 → Already forwarded (cooldown)
```

**Example (Min Groups = 3)**:

```
10:00 - Group A mentions CA 0xABC... → Count: 1 → Hold
10:30 - Group B mentions CA 0xABC... → Count: 2 → Hold
11:00 - Group C mentions CA 0xABC... → Count: 3 → FORWARD ✅
```

**Key point**: The message forwarded is typically the **first message** where threshold is reached (from the group that pushed count to minimum).

#### Time Window

**Definition**: How long to track CA mentions across groups.

**Short window (1-6 hours)**:

* **Use case**: Fast-moving markets, trending tokens, pumps
* **Pro**: Catch quick trends, timely signals
* **Con**: May miss slower consensus-building

**Medium window (12-24 hours)**:

* **Use case**: Daily crypto discussion, balanced pace
* **Pro**: Captures most legitimate multi-group interest
* **Con**: Slightly delayed for very fast trends

**Long window (48-168 hours)**:

* **Use case**: Long-term holds, project research phase
* **Pro**: High confidence (sustained multi-day interest)
* **Con**: Very delayed, may miss entry opportunities

**Recommendation**:

* Day trading / scalping: 3-6 hours
* Swing trading: 12-24 hours
* Research / investing: 48+ hours

#### Cooldown Period

**Purpose**: After forwarding a CA once, prevent forwarding it again for X time.

**Why needed**:

* Same CA can be mentioned many times
* Without cooldown, you'd forward duplicates
* Creates spam in target

**How it works**:

```
10:00 - CA 0xABC forwarded after meeting min groups
10:00-22:00 - Cooldown active (12 hours)
       - Any mention of 0xABC from ANY group is blocked
22:00 - Cooldown expires
22:01 - If 0xABC mentioned again and meets min groups → Can forward again
```

**Setting guidelines**:

* **Short (1-2 hours)**: If you want updates on developing news for same CA
* **Medium (6-12 hours)**: Standard spam prevention
* **Long (24+ hours)**: Strict "once per day" rule

**Interaction with duplicate prevention**:

* Cooldown is **global** (all groups)
* Duplicate prevention is **per source group**
* Both work together to reduce spam

#### Duplicate Prevention

**Auto Duplicate Prevention** (per source group):

**Scenario without prevention**:

```
10:00 - Group A mentions CA 0xABC → Count toward threshold
10:15 - Group A mentions CA 0xABC again → Count again? ❌
10:30 - Group B mentions CA 0xABC → Count toward threshold
```

**With prevention enabled** (recommended):

* Each source group can only contribute **once** per CA per time window
* Prevents single spammy group from triggering threshold alone
* Ensures genuine **cross-group** validation

**Example**:

```
Min Groups: 2
Duplicate Prevention: ON

10:00 - Group A posts CA 0xABC (3 times in 5 minutes) → Counted as 1
10:30 - Group B posts CA 0xABC (once) → Counted as 1
Total unique groups: 2 → FORWARD ✅
```

Without prevention, Group A's 3 mentions might be miscounted.

***

### Common Use Cases

#### Crypto Signal Aggregation

**Scenario**: Aggregate signals from 5 crypto alpha groups, only want tokens mentioned by multiple groups.

**Setup**:

```
Min Groups: 2-3
Time Window: 12 hours
Cooldown: 12 hours
Duplicate Prevention: ON
```

**Result**: Forward only CAs gaining multi-group attention = stronger signals.

***

#### Scam Reduction

**Scenario**: Many groups post scam CAs, but legit projects get multi-group coverage.

**Setup**:

```
Min Groups: 3-4 (higher threshold)
Time Window: 24 hours
Cooldown: 24 hours
Duplicate Prevention: ON
```

**Result**: Scams typically only in 1-2 groups, legit projects in many groups. Higher threshold filters scams.

***

#### Trending Token Detection

**Scenario**: Catch tokens starting to trend across crypto community.

**Setup**:

```
Min Groups: 2
Time Window: 6 hours (short, catch trends early)
Cooldown: 6 hours
Duplicate Prevention: ON
```

**Result**: Quickly detect CAs getting multi-group traction, potentially before major pumps.

***

#### Long-Term Project Research

**Scenario**: Research phase, only interested in CAs with sustained multi-day interest.

**Setup**:

```
Min Groups: 3-5 (high confidence)
Time Window: 72 hours (3 days)
Cooldown: 72 hours (once per 3 days)
Duplicate Prevention: ON
```

**Result**: Only forward CAs discussed across multiple groups over multiple days = high-quality project leads.

***

#### Pump Group Coordination Detection

**Scenario**: Detect when multiple pump groups coordinate on same CA.

**Setup**:

```
Min Groups: 3+ (pump groups)
Time Window: 1-3 hours (pumps happen fast)
Cooldown: 6 hours
Duplicate Prevention: ON
```

**Result**: Catch coordinated pump activity early (can be entry signal or warning depending on your strategy).

***

### Troubleshooting

#### Issue: No Messages Being Forwarded

**Check**:

* [ ] You have **multiple source groups** (2+) in task
* [ ] Min groups threshold isn't too high (try 2 first)
* [ ] Time window isn't too short (try 12-24 hours)
* [ ] Source groups actually discuss CAs in compatible format
* [ ] Addon is enabled and active

**Test**: Look at source groups manually, verify CAs appear in multiple groups within time window.

***

#### Issue: Too Many Signals (Too Noisy)

**Problem**: Forwarding too many CAs, hard to keep up.

**Solutions**:

* **Increase min groups**: 2 → 3 → 4 (more validation)
* **Shorten time window**: Only recent trending CAs
* **Increase cooldown**: Prevent rapid re-mentions
* **Combine with other filters**: Use keyword filter to only track specific chains (e.g., "Solana", "SOL")

***

#### Issue: Missing Good CAs

**Problem**: Known good CAs mentioned in multiple groups but not forwarded.

**Check**:

* [ ] CA format is recognized (ETH: 0x..., Solana: Base58)
* [ ] Messages arrived within time window
* [ ] Not blocked by cooldown from previous forward
* [ ] Duplicate prevention not miscounting groups

**Test**: Reduce min groups to 2, expand time window to 24 hours, verify CA forwarding works at all.

***

#### Issue: Same CA Forwarded Multiple Times

**Check**:

* [ ] Cooldown period is set (not 0)
* [ ] Cooldown is long enough (try 12+ hours)
* [ ] Messages aren't coming after cooldown expires

**If issue persists**: May be different messages with same CA after cooldown. This is expected behavior if cooldown expired.

***

#### Issue: Can't Detect Certain CA Formats

**Problem**: CAs from less common chains not detected.

**Limitation**: Addon primarily supports:

* Ethereum-like (0x... format)
* Solana (Base58 format)

**Workaround**: Contact support to request additional chain support, or use standard keyword filter instead.

***

#### Issue: Single Group Triggering Threshold

**Problem**: One spammy group posting same CA multiple times triggers threshold alone.

**Solution**: Ensure **Duplicate Prevention is ON**. This prevents single group from counting multiple times.

***

### Best Practices

#### Start with Conservative Settings

Initial setup:

```
Min Groups: 2
Time Window: 24 hours
Cooldown: 12 hours
Duplicate Prevention: ON
```

Adjust over 1-2 weeks based on signal quality.

#### Use Multiple Source Groups (5-10+)

More sources = better validation:

* 2-3 sources: Limited validation (addon still useful but less powerful)
* 5-10 sources: Good validation, diverse perspectives
* 10+ sources: Excellent validation, very strong signals

#### Balance Min Groups with Source Count

**Rule**: Min Groups should be 20-40% of total sources

* 5 sources → Min Groups: 2
* 10 sources → Min Groups: 3-4
* 20 sources → Min Groups: 5-8

Too high = miss good signals. Too low = too noisy.

#### Adjust Time Window to Market Pace

* **Bull market / High volatility**: Shorter windows (3-12 hours)
* **Bear market / Low volatility**: Longer windows (24-72 hours)
* **Trending news**: Shorter windows
* **Research phase**: Longer windows

#### Combine with Sender Filters

Improve signal quality:

1. Use sender filter to block known spam groups
2. Then apply CA matching on remaining quality sources
3. \= Higher quality cross-group validation

#### Monitor and Tune

After 1 week of use:

* Count signals received per day
* Check signal quality (how many were good trades/leads)
* Adjust min groups / time window / cooldown accordingly
* Too many signals → Increase min groups, shorten window
* Too few signals → Decrease min groups, lengthen window

#### Use with Keyword Filters

Combine for chain-specific tracking:

* **Keyword filter**: "Solana" OR "SOL"
* **CA Matching**: Min 3 groups, 12 hours
* \= Only Solana CAs with 3+ group mentions

#### Document Your Sources

Keep list of source groups and their quality:

* Premium alpha groups: High weight
* Public aggregators: Medium weight
* Meme groups: Lower weight Helps you understand why certain CAs meet threshold.

***

### Frequently Asked Questions

#### What chains are supported?

**Confirmed**:

* Ethereum (0x... format)
* Binance Smart Chain (0x... format)
* Polygon (0x... format)
* Other EVM chains (0x... format)
* Solana (Base58 format)

**Potentially supported**: Other chains with standard CA formats. Contact support to verify.

#### Does it check CA legitimacy (scam detection)?

**No**, addon only checks if CA appears in multiple groups. It does NOT verify if CA is legitimate, safe, or scam-free. Always DYOR (do your own research) before trading.

#### What if same CA has different formats?

Example: `0xABC...` vs `0xabc...` (case difference)

**Usually normalized**: Most implementations treat CAs case-insensitively for matching. But verify by testing.

#### Can it track CA across different messages about same project?

**Yes**, addon extracts CA from message content. Doesn't matter if messages have different text, as long as they contain same CA.

Example:

* Group A: "Token ABC launching! CA: 0x123..."
* Group B: "New gem found, 0x123... check it out" Both counted toward same CA: `0x123...`

#### Does it work with media messages?

**Yes**, if message contains CA in caption text. CAs in images/screenshots may not be detected (depends on implementation).

#### Can I whitelist/blacklist specific CAs?

**Not directly in this addon**, but you can combine with keyword filter:

* **Blacklist CA**: Use keyword filter to block specific 0x... addresses
* **Whitelist CA**: Harder, but you can block all CAs using keyword filter, then manually allow specific ones

#### What happens if CA appears in 2 groups simultaneously?

If two groups post same CA at exactly same time (within seconds/minutes):

* Both counted toward threshold
* First message reaching threshold triggers forward
* Other message blocked by duplicate prevention and cooldown

#### Does cooldown reset if CA mentioned again after expiry?

**Yes**, if cooldown expires and CA meets threshold again (X groups within time window), it can be forwarded again and cooldown resets.

#### Can I use with single source group?

**Technically yes, but pointless**. Cross-group matching requires multiple source groups to provide value. Single source = no cross-validation.

#### How is time window calculated?

**Rolling window**: If time window is 12 hours, at any given moment, addon looks back 12 hours to count group mentions.

Example (12-hour window, current time: 10:00):

* Checks mentions from 22:00 (previous day) to 10:00 (now)
* Rolling basis, not fixed daily/hourly reset

***

### Performance Tips

#### Optimize Source Group Count

* **Too few** (<3): Limited validation, addon underutilized
* **Optimal** (5-15): Good balance, meaningful cross-group signals
* **Too many** (20+): May slow processing, increases false positives if many low-quality sources

#### Use Quality Sources

One high-quality alpha group > Five meme/spam groups

* Select reputable source groups
* Avoid spam-heavy sources
* Better sources = better cross-group validation = better signals

#### Balance Time Window

* **Too short**: Miss legitimate multi-group consensus (**false negatives**)
* **Too long**: Stale signals, less actionable (**delayed signals**)
* **Sweet spot**: 12-24 hours for most crypto use cases

#### Set Reasonable Min Groups

* **Too low** (1): No cross-validation, just spam (**false positives**)
* **Too high** (≥50% of sources): Miss good signals (**false negatives**)
* **Sweet spot**: 20-40% of total source groups

***

### Getting Help

If CA matching isn't working as expected:

1. Verify you have **multiple source groups** (2+)
2. Check source groups actually post CAs in supported formats
3. Test with very low threshold (min groups: 2, time window: 24 hours)
4. Verify addon is enabled and active
5. Check Addons FAQ
6. Contact support with:
   * Your CA matching configuration
   * Source group count and names
   * Example CA that should be forwarded but wasn't
   * Expected vs actual behavior

**Support**: Menu → Help & Support or support@autoforwardtelegram.com

***

### Summary

Cross-Group CA Matching provides intelligent crypto signal aggregation:

✅ **Multi-group validation** - Only forward CAs mentioned by X groups\
✅ **Time-based tracking** - CA must appear within time window\
✅ **Spam prevention** - Cooldown and duplicate blocking\
✅ **Auto-detection** - Automatically extracts CAs from messages\
✅ **Quality signals** - Multiple mentions = stronger validation\
✅ **Scam reduction** - Less likely to forward single-group spam

**Perfect for**: Crypto signal aggregation, alpha group consolidation, scam reduction, trend detection, multi-source validation, project research.

**Quick start**:

1. Enable addon in task with **multiple source groups**
2. Set min groups: 2-3
3. Set time window: 12-24 hours
4. Set cooldown: 12 hours
5. Enable duplicate prevention: ON
6. Monitor for 1 week and adjust

**Pro tip**: Combine with keyword filters (chain names, "CA:", "Contract:") and sender filters (block spam groups) for best results.

***

**Last Updated**: March 2026\
**Addon Version**: 1.0\
**App Version**: 1.0.44+
