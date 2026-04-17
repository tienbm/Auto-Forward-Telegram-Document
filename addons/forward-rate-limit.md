---
icon: puzzle-piece
---

# Forward Rate Limit

### Overview

Forward Rate Limit controls the number of messages your task forwards within a specific time window. When the limit is exceeded, the task automatically pauses to prevent spam flags, respect channel rules, or manage your forwarding volume.

#### What It Does

* Sets maximum forwards per time period (hourly, daily, or custom)
* Automatically pauses task when limit is reached
* Sends warning notification before reaching limit
* Resumes automatically when time window resets
* Prevents spam flags and rate limit issues

#### Key Benefits

✅ **Prevent spam flags** - Stay under Telegram's radar\
✅ **Respect channel rules** - Honor posting limits\
✅ **Control volume** - Manage output quantity\
✅ **Auto-pause** - No manual monitoring needed\
✅ **Warning system** - Get notified before limit hits\
✅ **Flexible windows** - Hourly, daily, or custom periods

***

### Getting Started

#### Prerequisites

1. ✅ Purchase Forward Rate Limit addon
2. ✅ Have an active forwarding task
3. ✅ Know your desired forwarding limits

#### Quick Setup

**Step 1: Purchase & Enable**

1. Menu → My Addons → Forward Rate Limit → Unlock
2. Open your task settings
3. Find **Forward Rate Limit** section
4. Toggle **Enable Rate Limit** to ON

**Step 2: Configure Time Window**

Choose your time period:

* **Hourly**: Limit forwards per hour (e.g., max 50/hour)
* **Daily**: Limit forwards per day (e.g., max 500/day)
* **Custom**: Set custom hours (e.g., max 100 per 6 hours)

**Step 3: Set Maximum Forwards**

Enter the maximum number of forwards allowed within your time window:

* Conservative: 10-50 per hour, 100-500 per day
* Moderate: 50-100 per hour, 500-1000 per day
* Aggressive: 100+ per hour, 1000+ per day (higher spam risk)

**Step 4: Configure Warnings (Optional)**

**Warning Threshold**: Get notified when you've used X% of your limit

* Example: Set 80% to get warning at 80/100 forwards
* Helps you prepare for pause

**Warning Notification**: Choose how to be notified

* In-app notification
* Telegram message to your account

**Step 5: Auto-Resume Settings**

**Auto-resume when window resets**: ON/OFF

* **ON**: Task automatically resumes when new time window starts
* **OFF**: Task stays paused until you manually resume

***

### Configuration Details

#### Time Window Options

**Hourly Window**

**Best for**: High-volume sources with steady flow

```
Max Forwards: 50
Time Window: 1 hour
Result: Up to 50 forwards/hour, then pause for remainder of hour
```

**Use case**: News channels with constant updates, crypto signals

**Daily Window**

**Best for**: Moderate volume, daily quotas

```
Max Forwards: 500
Time Window: 24 hours (1 day)
Result: Up to 500 forwards/day, then pause until midnight
```

**Use case**: Content aggregation, daily digests

**Custom Window**

**Best for**: Specific requirements or testing

```
Max Forwards: 100
Time Window: 6 hours
Result: Up to 100 forwards per 6-hour period
```

**Use case**: Special requirements, gradual rollout, A/B testing

#### Maximum Forwards Guidelines

**Recommended limits by target type**:

| Target Type     | Hourly Limit | Daily Limit | Risk Level |
| --------------- | ------------ | ----------- | ---------- |
| Public Channels | 20-50        | 200-500     | Low-Medium |
| Private Groups  | 50-100       | 500-1000    | Medium     |
| Contacts (DMs)  | 5-10         | 20-50       | High       |
| Mixed           | 30-70        | 300-700     | Medium     |

**Factors affecting limits**:

* **Content type**: Media-heavy content = lower limits safer
* **Target size**: Larger audiences = lower limits recommended
* **Account age**: Older accounts can handle higher limits
* **Previous flags**: If flagged before, use conservative limits

#### Warning System

**How warnings work**:

1. You set threshold (e.g., 80%)
2. When 80% of limit reached (e.g., 80/100 forwards)
3. System sends notification
4. You have time to prepare or manually pause

**Notification options**:

* In-app badge on Tasks screen
* Telegram DM to your account
* Both (recommended)

**Why useful**:

* Prevents surprise pauses during important forwarding
* Lets you manually pause at better time
* Helps monitor your usage patterns

#### Auto-Resume Behavior

**When enabled**:

* Task pauses at limit
* Waits for time window to reset
* Automatically resumes forwarding
* Counter resets to 0

**When disabled**:

* Task pauses at limit
* Stays paused even after window resets
* You must manually resume via Tasks screen
* Useful for manual oversight

**Example (Hourly, Auto-Resume ON)**:

```
10:00 - Task starts, 0/50 forwards
10:45 - Reaches 50/50, auto-pauses
11:00 - New hour begins, auto-resumes, reset to 0/50
```

***

### Common Use Cases

#### Prevent Telegram Spam Flags

**Scenario**: You forward aggressively and got spam warnings before.

**Setup**:

```
Time Window: Hourly
Max Forwards: 30
Warning: 80% (24 forwards)
Auto-Resume: ON
```

**Result**: Stay safely under Telegram's radar with controlled pacing.

***

#### Respect Channel Posting Rules

**Scenario**: Your target channel limits posts to 100/day.

**Setup**:

```
Time Window: Daily
Max Forwards: 95 (buffer)
Warning: 90% (85 forwards)
Auto-Resume: ON
```

**Result**: Never exceed channel rules, avoid admin complaints.

***

#### Test New Source Gradually

**Scenario**: Testing a new source, don't want to flood audience.

**Setup**:

```
Time Window: Custom (6 hours)
Max Forwards: 20
Warning: None
Auto-Resume: OFF (manual review)
```

**Result**: Controlled rollout, manual review between batches.

***

#### High-Volume News Aggregation

**Scenario**: Aggregate from 10 news sources, high message volume.

**Setup**:

```
Time Window: Hourly
Max Forwards: 80
Warning: 75% (60 forwards)
Auto-Resume: ON
```

**Result**: Steady flow without overwhelming targets, auto-recovery.

***

### Troubleshooting

#### Issue: Task Pausing Too Often

**Problem**: Task hits limit and pauses frequently, missing messages.

**Solutions**:

* **Increase max forwards**: Raise limit by 50%
* **Change time window**: Switch from hourly to daily for more flexibility
* **Filter source better**: Use content filters to reduce volume
* **Split into multiple tasks**: Distribute load across tasks

***

#### Issue: Not Receiving Warnings

**Check**:

* [ ] Warning threshold is configured (not 100%)
* [ ] Notification method is selected
* [ ] In-app notifications are enabled (Settings)
* [ ] Telegram DM from bot isn't blocked

**Fix**: Re-configure warning settings, test with low threshold (50%) to verify.

***

#### Issue: Auto-Resume Not Working

**Check**:

* [ ] Auto-Resume is enabled in settings
* [ ] Task isn't manually stopped
* [ ] Addon hasn't expired
* [ ] Time window has actually reset (check timezone)

**Fix**: Check each item. Note: Time window resets based on server timezone (usually UTC).

***

#### Issue: Wrong Time Window

**Problem**: Time window doesn't align with your needs (e.g., resets at odd hours).

**Solution**:

* Use **Daily** window for midnight resets
* Use **Custom** window with precise hours
* Plan around server timezone (UTC typically)

***

#### Issue: Limit Too Conservative

**Problem**: Task pauses but I can forward more without issues.

**Solution**:

* Gradually increase limit by 20-30%
* Monitor for spam flags or complaints
* Find your account's safe threshold through testing
* Remember: Limit can be adjusted anytime

***

### Best Practices

#### Start Conservative, Scale Up

Begin with lower limits and increase gradually:

* Week 1: 30/hour or 300/day
* Week 2: 50/hour or 500/day
* Week 3: 70/hour or 700/day

Monitor for issues at each step.

#### Set Warnings at 75-90%

Gives you buffer time to:

* Check if important messages are pending
* Manually pause at better moment
* Adjust limit if needed
* Monitor usage patterns

#### Use Daily Windows for Simplicity

Unless you have specific needs, daily windows are easiest:

* Predictable reset (midnight)
* Easier to estimate daily quota
* Less frequent pauses

#### Combine with Content Filters

Reduce unnecessary forwards:

* Forward Rate Limit controls quantity
* Content filters control quality
* Together = optimized forwarding

#### Monitor First Week Closely

After enabling, watch for:

* How quickly you hit limits
* Whether limits are too high/low
* Spam flags or user complaints
* Optimal time windows for your sources

#### Account for Time Zones

If targets are in specific timezone:

* Daily window resets at server midnight (UTC)
* May be mid-day for your audience
* Consider Custom window aligned to your audience's timezone

***

### Frequently Asked Questions

#### Does it count only successful forwards?

**Yes**, only successfully forwarded messages count toward your limit. Failed forwards (errors, skipped messages) don't count.

#### Can I have different limits for different tasks?

**Yes!** Configure independently for each task. One task can have 50/hour, another 500/day.

#### What happens to queued messages when paused?

They remain in queue and forward when task resumes (unless they've expired or been deleted from source).

#### Does manual pause count toward time window?

**No**, timer only runs when task is active. Manual pauses don't consume your time window.

#### Can I temporarily disable without losing settings?

**Yes**, toggle "Enable Rate Limit" to OFF. Settings are preserved, toggle back ON anytime.

#### Do media-only vs text messages count the same?

**Yes**, each forward counts as 1 regardless of content type (text, photo, video, file, etc.).

#### What if I need more than the limit occasionally?

* Temporarily disable rate limit
* Or increase limit for short period
* Or use manual pause/resume to control when to forward

#### Does it work with scheduled forwarding?

**Yes**, works seamlessly with scheduled tasks. Limit applies to actual forward time, not schedule time.

***

### Performance Tips

#### For High-Volume Tasks

* Use hourly windows for finer control
* Set warnings at 70% for earlier notice
* Enable auto-resume for hands-off operation
* Monitor first few cycles closely

#### For Mixed Content Tasks

* Filter aggressively before rate limiting
* Use moderate limits (50/hour, 500/day)
* Combine with other content filters
* Prioritize quality over quantity

#### For Multiple Target Tasks

* Lower limits if broadcasting to many targets
* Each target counts as one forward
* Consider Dialog Broadcast addon for better control

***

### Getting Help

If rate limiting isn't working as expected:

1. Verify addon is active and enabled in task
2. Check your time window settings match expectations
3. Review warning threshold and notifications
4. Test with very low limit (5) to verify functionality
5. Check Addons FAQ
6. Contact support with:
   * Your rate limit configuration
   * Expected vs actual behavior
   * How many forwards you're seeing per window

**Support**: Menu → Help & Support or support@autoforwardtelegram.com

***

### Summary

Forward Rate Limit gives you precise control over forwarding volume:

✅ **Prevent spam** - Stay under Telegram's radar with safe limits\
✅ **Auto-management** - Set it and forget it, auto-pause/resume\
✅ **Flexible windows** - Hourly, daily, or custom periods\
✅ **Warning system** - Get notified before hitting limits\
✅ **Per-task control** - Different limits for different tasks\
✅ **Compliance** - Respect channel rules and rate limits

**Perfect for**: High-volume forwarding, spam prevention, channel rule compliance, controlled rollouts, testing new sources.

**Quick start**:

1. Enable addon in task
2. Choose daily window (simplest)
3. Set conservative limit (300/day)
4. Enable warnings at 80%
5. Turn on auto-resume
6. Monitor and adjust

***

**Last Updated**: March 2026\
**Addon Version**: 1.0\
**App Version**: 1.0.44+
