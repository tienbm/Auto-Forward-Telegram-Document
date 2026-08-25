---
description: >-
  Use Smart AI Rewrite to evaluate token alert messages against configured
  thresholds and add a PASS, REVIEW, or REJECT verdict before the next
  forwarding or review step.
---

# Use Smart AI Rewrite to Evaluate Token Alerts

### What does this feature do?

This workflow adds a quality check before a token message is sent to the destination chat:

1. A token message arrives in the source chat.
2. **Smart AI Rewrite** reads the metrics included in the message.
3. AI adds a verdict to the first line: `PASS`, `REVIEW`, or `REJECT`.

For example, a token with sufficient liquidity and volume, a favorable buyer-to-seller ratio, and acceptable holder concentration can receive `PASS`. A token that fails a rule or has missing data receives a different verdict for the next workflow step.

{% hint style="warning" %}
`PASS` only means that the message passed the data rules configured in the prompt. It is not a guarantee that the token is safe, a price prediction, or investment advice.
{% endhint %}

### Before you start

* Create or open a forwarding task with the correct **source chat** and **destination chat**.
* Define the thresholds you want to use. The thresholds in this guide are examples.
* Prepare a test message that does not contain private information.
* Decide how your workflow should handle `PASS`, `REVIEW`, and `REJECT` after AI processing.
* If you use screenshots for documentation or support, hide chat names, IDs, account details, and private content.

{% hint style="warning" %}
Do not put API keys, passwords, access tokens, private IDs, or account information in the prompt or screenshots. Use a sample message and a placeholder token address in documentation and demos.
{% endhint %}

### Processing flow

```
Source chat
    ↓
Smart AI Rewrite
    ↓
PASS / REVIEW / REJECT
    ↓
Destination chat
```

### 1. Open Smart AI Rewrite

<figure><img src="../.gitbook/assets/image (298).png" alt=""><figcaption></figcaption></figure>

1. Open the forwarding task you want to configure.
2. Open **Smart AI Rewrite**.
3. Turn on the **Smart AI Rewrite** toggle.
4. Check the selected model in **Model**.

You do not need to change the model if you want to keep the current configuration. Model names and versions may change as the system is updated.

The app may warn that using AI can cause a slight delay in message forwarding. This delay is expected because the message must be processed before the next forwarding or review step.

<figure><img src="../.gitbook/assets/image (297).png" alt=""><figcaption></figcaption></figure>

### 2. Enter the token evaluation prompt

In **Rewrite Instructions**, enter a prompt. The example below uses demonstration thresholds and tells AI to use only the data explicitly included in the message.

```
You are a strict token-quality classifier.

Analyze only the explicit metrics included in the incoming token alert. Do not browse external links, do not make price predictions, and do not provide financial advice.

For this demo, return PASS only when all mandatory conditions are satisfied:

- Liquidity is at least $10K
- Volume is at least $100K
- Token age is at least 30 minutes
- 1H price change is positive
- Buyers are greater than or equal to sellers
- Top-holder concentration is no more than 25%
- Developer holding is no more than 5%
- Ghost-wallet percentage is no more than 10%
- All mandatory values are explicitly present

If all conditions pass, the first line must be exactly:
PASS

If the data is incomplete or uncertain, the first line must be exactly:
REVIEW

If one or more explicit risk thresholds fail, the first line must be exactly:
REJECT

The second line must contain a short metric summary in this format:
AI Check: [metric] ✓ | [metric] ✓ | [metric] ✗

After the first two lines, reproduce the original message exactly as received. Preserve all links, emojis, Markdown formatting, token address, and line breaks. Do not translate, summarize, rewrite, or add any content before the verdict line.
```

#### How can I change the thresholds?

You can change values such as `$10K`, `$100K`, `30 minutes`, and `25%` to match your strategy. Whenever you change a threshold, test the workflow with both a passing and a failing message.

Do not ask AI to open links in the message unless your product provides a separate verified data source. This prompt is designed to evaluate only the metrics that are explicitly visible in the incoming message.

<figure><img src="../.gitbook/assets/image (299).png" alt=""><figcaption></figcaption></figure>

### 3. Save and apply the configuration

1. Review the prompt in **Rewrite Instructions**.
2. Click **Save & Apply**.
3. Wait for the configuration to be saved before sending a test message.

After saving, send a new message to the source chat. Use a new test message for each check so that you can distinguish the current result from an earlier configuration.

### 4. Test with a passing message

Use a sanitized sample message with all real links and addresses removed:

```
[Token alert - demo]
Name: Example Token
Liquidity: $17.4K
Volume: $371K
Age: 2h
1H: +40.1%
Buyers: 1.9K
Sellers: 1.2K
Top-holder concentration: 21%
Developer holding: 0%
Ghost wallets: 1.3%
Contract: EXAMPLE_TOKEN_ADDRESS
```

Expected result:

```
PASS
AI Check: LIQ 17.4K ✓ | VOL 371K ✓ | AGE 2h ✓ | 1H +40.1% ✓ | B/S 1.9K/1.2K ✓ | TOP 21% ✓ | DEV 0% ✓ | GHOST 1.3% ✓

[Original demo message]
```

When the first line is `PASS`:

1. AI Rewrite has added the verdict.
2. The message is ready for the next forwarding or review step in your workflow.

<figure><img src="../.gitbook/assets/image (301).png" alt=""><figcaption></figcaption></figure>

### 5. Test with a failing message

Use a second sample message with one or more values outside the thresholds:

```
[Token alert - demo]
Liquidity: $4K
Volume: $35K
Age: 12m
1H: -18%
Buyers: 200
Sellers: 800
Top-holder concentration: 42%
Developer holding: 18%
Ghost wallets: 16%
Contract: EXAMPLE_TOKEN_ADDRESS_2
```

Expected result:

```
REJECT
AI Check: LIQ 4K ✗ | VOL 35K ✗ | AGE 12m ✗ | 1H -18% ✗ | B/S 200/800 ✗ | TOP 42% ✗ | DEV 18% ✗ | GHOST 16% ✗

[Original demo message]
```

Because the message is labeled `REJECT`, it can be excluded from forwarding or sent for review according to your task configuration.

If a mandatory metric is missing, the expected result is `REVIEW`, not `PASS`:

```
REVIEW
AI Check: LIQ 17.4K ✓ | VOL 371K ✓ | AGE 2h ✓ | TOP HOLDER DATA MISSING ?
```

### After setup

The workflow is configured correctly when it produces these states:

| Message content                                      | Verdict  | Recommended handling                                 |
| ---------------------------------------------------- | -------- | ---------------------------------------------------- |
| All thresholds pass and all required data is present | `PASS`   | Continue with the next forwarding or review step     |
| Required data is missing or uncertain                | `REVIEW` | Hold for manual review or route to a review workflow |
| One or more risk thresholds fail                     | `REJECT` | Exclude from the next step or review manually        |

### Manage the configuration

#### Change the evaluation thresholds

1. Open **Smart AI Rewrite**.
2. Edit the thresholds in **Rewrite Instructions**.
3. Click **Save & Apply**.
4. Run both the PASS and REJECT tests again.

If you keep the `PASS`, `REVIEW`, and `REJECT` labels, update only the prompt and rerun the test cases.

#### Change the verdict format

If you want to use a different label, such as `TOKEN_PASS`, update all of the following:

1. The prompt in **Rewrite Instructions**.
2. Your test cases and related internal documentation.

If you change the verdict format, update any downstream workflow that reads the verdict.

#### Disable Smart AI Rewrite

Turn off the **Smart AI Rewrite** toggle when you no longer want AI to process messages.

When AI is disabled, messages no longer receive an AI-generated verdict. Review any downstream workflow that expects `PASS`, `REVIEW`, or `REJECT` before disabling the feature.

### Common statuses

| Status                          | Meaning                                                    | What to do                                               |
| ------------------------------- | ---------------------------------------------------------- | -------------------------------------------------------- |
| **Smart AI Rewrite** enabled    | Messages are processed by AI before forwarding.            | Check the prompt and selected model.                     |
| `PASS`                          | All mandatory conditions passed according to the prompt.   | Continue with the next forwarding or review step.        |
| `REVIEW`                        | Data is missing or the result is not sufficiently certain. | Review the message manually or send it to a review chat. |
| `REJECT`                        | One or more risk thresholds failed.                        | Exclude it from the next step or review it manually.     |
| Forwarding is slower than usual | AI needs additional time to process the message.           | Wait briefly before checking the destination chat.       |

### Troubleshooting

#### A token receives an unexpected verdict

Check the following:

1. **Smart AI Rewrite** is enabled.
2. You clicked **Save & Apply** after editing the prompt.
3. The AI result has the expected verdict on the first line.
4. All mandatory metrics are explicitly present in the test message.
5. The source and destination chats are still correct and the account still has access.

#### Every message receives the same verdict

A common cause is that the prompt thresholds are too strict, required metrics are missing, or AI added an explanation before the verdict. Keep the requirement that the first line must contain only `PASS`, `REVIEW`, or `REJECT`, and check the actual output.

#### AI returns `PASS` when data is missing

Add or keep this condition in the prompt:

```
Never output PASS when a mandatory value is missing.
```

Click **Save & Apply**, then test with a message that intentionally omits one mandatory metric.

#### The original content changes

The prompt asks AI to preserve links, emojis, Markdown, the token address, and line breaks. If the output is still summarized or rewritten:

1. Check the selected model.
2. Reinforce the instruction `reproduce the original message exactly`.
3. Test with a new sample message.

If the content still changes, confirm with the product team whether Smart AI Rewrite supports a prepend-only mode that adds a verdict without rewriting the original message.

### Frequently asked questions

#### Does `PASS` mean that the token is safe?

No. `PASS` only means that the token met the data thresholds in the prompt. It does not check every contract risk, liquidity risk, mint or freeze authority, developer behavior, or external data source.

#### Does AI open DEX, Solscan, or chart links automatically?

Do not assume that it does. This guide asks AI to read only the metrics already present in the message. If you need external verification, the product must provide a separate data source or verification step.

#### Do I have to use all three verdicts: `PASS`, `REVIEW`, and `REJECT`?

No, but a fixed format makes the output predictable and manual review easier. If you change a verdict label, update the prompt and any downstream workflow together.

#### Can AI slow down forwarding?

Yes. The Smart AI Rewrite screen warns that using AI may cause a slight delay during message forwarding.

#### Can I write the prompt in another language?

Yes, as long as the prompt defines the output format clearly and requires the verdict on the first line. The English prompt in this guide is provided as a stable example.

### Notes to confirm before release

> The available reference materials confirm the **Model**, **Smart AI Rewrite**, **Rewrite Instructions**, and **Save & Apply** components. Confirm the following in the app version that will be released:
>
> * Where the rewritten message appears after Smart AI Rewrite processes it.
> * Whether the original links, emojis, Markdown, token address, and line breaks are preserved.
> * Whether the model can consistently place only the verdict on the first line.
> * How `PASS`, `REVIEW`, and `REJECT` should be handled by the rest of the forwarding workflow.
