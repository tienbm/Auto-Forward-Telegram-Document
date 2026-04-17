---
icon: hexagon-nodes
---

# News Digest

### Overview

News Digest automatically collects messages from your source groups during the day, then uses AI to summarize them into a single structured report at your chosen time. Instead of forwarding every individual message, your audience receives one clean, well-organized digest.

#### What It Does

* Accumulates incoming messages from source groups throughout the day
* At your scheduled time, sends all collected messages to an AI model
* AI generates a single summarized digest based on your prompt
* Forwards the finished digest to your target chats

#### Key Benefits

✅ **Reduce noise** — One digest instead of dozens of individual messages\
✅ **Structured output** — AI organizes content into readable sections\
✅ **Flexible scheduling** — Run daily, on specific days, or multiple times per day\
✅ **Custom AI prompt** — Control exactly how the AI formats the summary\
✅ **Your own AI model** — Use your own API key (OpenAI, Claude, etc.)

***

### Getting Started

#### Requirements

* Active **Platinum** (or Platinum Trial) plan
* At least one forwarding task with source groups configured
* An **AI API Key** added to your account (Settings → API Keys)

#### Quick Setup

1. Open a task → **AI Mode** → **News Digest**
2. Toggle **Enable News Digest** to ON
3. Select which **days** to run the digest
4. Add one or more **schedule times** (e.g., 6:00 PM)
5. Choose your **AI model**
6. Choose **System** or **Custom** prompt
7. Tap **Save & Apply**

***

### Configuration

#### Enable / Disable

The main toggle turns News Digest on or off for this task.

* **OFF**: Messages are forwarded individually as usual
* **ON**: Messages are collected silently and summarized at the scheduled time

***

#### Schedule Days

Select which days of the week to generate the digest.

* Tap individual day circles to toggle them (Sun through Sat)
* Select all days for a daily digest
* Select only weekdays (Mon–Fri) to skip weekends
* You must select **at least one day** before saving

***

#### Schedule Times

Set what time(s) each day the digest is generated and sent.

* Tap **Add Time** to open a time picker
* You can add **multiple times** per day (e.g., 12:00 PM and 8:00 PM)
* Added times appear as chips — tap **×** on any chip to remove it
* You must add **at least one time** before saving

**Example schedules:**

| Goal               | Days        | Times             |
| ------------------ | ----------- | ----------------- |
| End-of-day summary | Mon–Fri     | 6:00 PM           |
| Twice-daily digest | Every day   | 12:00 PM, 9:00 PM |
| Weekly roundup     | Sunday only | 10:00 AM          |

***

#### Max Messages to Digest

Controls how many recent messages are sent to the AI for summarization.

* **Range**: 10 – 500 messages
* **Default**: 50
* Tap the field to enter a number

**Guidelines:**

| Volume                             | Recommended Setting |
| ---------------------------------- | ------------------- |
| Low-traffic source (< 20 msgs/day) | 20–30               |
| Medium traffic (20–100 msgs/day)   | 50–100              |
| High traffic (100+ msgs/day)       | 100–300             |

Setting this too low may cause important messages to be left out. Setting it too high may exceed your AI model's context window.

***

#### AI Model

Select which AI model to use for generating the digest.

1. Tap the **Model** selector
2. You are taken to your **API Keys** list
3. Choose the API key / model to use
4. The selected model appears in the field with its provider icon

**Supported providers:** OpenAI (GPT-4, GPT-3.5), Anthropic (Claude), and others you've added to your account.

> If no model is selected, saving will show an error: _"Please select an AI model for News Digest"_

***

#### Digest Prompt Template

The prompt instructs the AI on how to format and style the digest.

**System Prompt (Default)**

The app uses a built-in optimized prompt that summarizes and structures messages automatically. Recommended for most users — no configuration needed.

**Custom Prompt**

Write your own prompt to control the output format, tone, language, and structure.

**How to switch:**

1. Tap the **Custom Prompt** chip
2. A text field appears — enter your instructions
3. Tap a **Quick Suggestion** chip to auto-fill a starting template

**Quick Suggestions available:**

* _Summarize all messages into a structured daily news bulletin with key topics and highlights_
* _Create a brief digest grouping messages by topic, highlighting important updates and action items_
* _Write a concise news summary focusing on the most important announcements and trending discussions_
* _Generate a professional newsletter-style summary with sections for each major topic covered_

Tap any suggestion to paste it into the text field, then customize as needed.

**Custom prompt tips:**

* Specify the **output language** if your audience is not English-speaking (e.g., _"Write the summary in Vietnamese"_)
* Define **sections**: e.g., _"Use sections: Breaking News, Market Updates, Community Highlights"_
* Control **length**: e.g., _"Keep the summary under 300 words"_
* Set **tone**: e.g., _"Write in a professional, neutral tone"_

***

### Saving Settings

Tap **Save & Apply** when you are done configuring. The button is disabled while saving.

If any required field is missing, you will see an error:

* _"Please add at least one schedule time"_ — Add a time in Schedule Times
* _"Please select at least one day of the week"_ — Select a day in Schedule Days
* _"Please select an AI model for News Digest"_ — Choose a model in the AI Model selector

***

### How the Digest Flow Works

```
Source Groups → Messages collected silently
                        ↓
              Scheduled time arrives
                        ↓
     Last N messages sent to AI model (up to Max Messages)
                        ↓
          AI generates summary using your prompt
                        ↓
         Digest forwarded to your target chats
```

Messages collected **before the schedule time** are included. After the digest is sent, the collection resets for the next cycle.

***

### Use Cases

#### Daily News Bulletin

Aggregate news from 5 Telegram news channels. Send a clean bullet-point summary to your channel every evening at 7 PM.

**Settings:**

* Days: Mon–Fri
* Time: 7:00 PM
* Max Messages: 100
* Prompt: _"Summarize all messages into a structured daily news bulletin with key topics and highlights"_

***

#### Crypto Market Summary

Collect signals and analysis from multiple crypto groups. Generate a morning and evening market recap.

**Settings:**

* Days: Every day
* Times: 9:00 AM, 9:00 PM
* Max Messages: 150
* Prompt: _"Create a brief market digest grouping messages by topic: price movements, new launches, community sentiment"_

***

#### Weekly Team Update

Collect messages from team Telegram groups all week and send a Monday morning roundup.

**Settings:**

* Days: Monday only
* Time: 9:00 AM
* Max Messages: 300
* Prompt: _"Generate a professional newsletter-style weekly summary with sections for each major topic discussed"_

***

### Troubleshooting

#### Digest not being sent

**Check:**

* [ ] Enable News Digest toggle is ON
* [ ] At least one day and one time are configured
* [ ] An AI model is selected
* [ ] Your API key is still valid (check Settings → API Keys)
* [ ] Your Platinum plan is still active

***

#### AI output is poor quality

**Solutions:**

* Switch to **Custom Prompt** and write more specific instructions
* Try a different **Quick Suggestion** as a starting point
* Use a more capable model (e.g., GPT-4 instead of GPT-3.5)
* Reduce **Max Messages** — fewer messages can produce cleaner summaries
* Add language instructions if output is in wrong language

***

#### Digest is missing recent messages

Most likely the messages arrived **after** the scheduled time and will be included in the next digest cycle.

If this happens consistently:

* Add a **second schedule time** later in the day
* Increase the **Max Messages** limit
* Adjust schedule times to better match when content peaks

***

#### "Please select an AI model" error when saving

You need to add an API key first:

1. Go to **Settings → API Keys**
2. Add your OpenAI or Claude API key
3. Return to News Digest → tap the Model selector
4. Choose your key and save

***

### Tips & Best Practices

**Match Max Messages to your source volume** — Check how many messages your sources send per day. Set Max Messages slightly higher than that to avoid missing content.

**Use Custom Prompt for non-English output** — The system prompt defaults to English. If your audience reads in another language, specify it in a custom prompt: _"Write the digest in Spanish"_.

**Test with a manual review first** — Enable News Digest, set a time 5–10 minutes from now, and verify the output quality before committing to a daily schedule.

**Avoid very high Max Messages on low-tier models** — Models like GPT-3.5 have smaller context windows. If you need to process 300+ messages, use GPT-4 or Claude.

**Use multiple times for busy sources** — For very active source groups, schedule 2–3 digest times per day to keep summaries manageable in length.

***

### Frequently Asked Questions

#### Does it forward original messages too?

**No.** When News Digest is enabled, original messages are collected silently and not individually forwarded. Only the AI-generated digest is sent at the scheduled time.

#### What happens if the AI fails to respond?

The digest for that cycle is skipped. Your next scheduled cycle will attempt again with messages collected since the last successful digest.

#### Can I use News Digest on multiple tasks?

**Yes**, each task has its own News Digest configuration with independent schedules, models, and prompts.

#### Is my message content sent to the AI provider?

**Yes.** Messages are sent to whichever AI provider's API you configure (e.g., OpenAI, Anthropic). Review that provider's data privacy policy before using with sensitive content.

#### Can I trigger a digest manually?

The **Run Now** button is coming soon. Currently, digests only run on their scheduled times.

#### What's the minimum and maximum for Max Messages?

* **Minimum**: 10 messages
* **Maximum**: 500 messages

#### Does it work with media messages?

News Digest processes **text content**. Media files (images, videos) are typically not sent to the AI — only any caption text or surrounding text messages.

***

**Last Updated**: March 2026\
**App Version**: 1.0.44+\
**Required Plan**: Platinum
