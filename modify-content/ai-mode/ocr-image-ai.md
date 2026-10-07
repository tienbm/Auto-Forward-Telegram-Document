---
icon: cards-blank
---

# OCR Image AI

## 📸 OCR Image AI – UI Guide

The OCR Image AI feature allows AutoForward to automatically extract text from any image and include it as part of the forwarded message. This is ideal for screenshots, flyers, or images containing important written information.

***

### ⚙️ Feature Walkthrough

#### 📲 Step-by-Step Walkthrough

1. **Select the Task you want to apply AI MODE to**

<figure><img src="../../.gitbook/assets/image (218).png" alt=""><figcaption></figcaption></figure>

2. **Select the AI MODE option inside the bot**

<figure><img src="../../.gitbook/assets/image (220).png" alt=""><figcaption></figcaption></figure>

3. **Select OCR Image AI**

<figure><img src="../../.gitbook/assets/image (350).png" alt=""><figcaption></figcaption></figure>

**4. Initial Screen (Feature Disabled)**

* ✅ Model: You must first select an AI model (e.g., gpt-4o, gemini-pro)&#x20;
* Toggle: The “OCR Image AI” toggle is off by default.

> ⚠️ You must choose a model that supports image input and text extraction.

***

#### 🔘 OCR Image AI Enable

* Toggle the switch to enable/disable OCR functionality.
* When enabled, AutoForward will process incoming images through the selected model and extract text.

> 💡 Note: Using AI may introduce slight delays in forwarding due to image processing time.

#### 🔘 Read Text in Stickers with AI

Sticker OCR lets a task read text from Telegram stickers and pass the recognized text into its content-processing flow. Use it when source stickers contain signals, announcements, or wording you want to process as text.

Unlike Sticker Replace, OCR does not require an ID rule for each sticker. Results depend on the image content and the selected AI model’s recognition capabilities.

***

#### 🧠 Prompt Options

You can choose how the AI interprets and formats the extracted content:

*   System Prompt (default)

    A pre-configured prompt optimized for clean and actionable OCR output.
*   Custom Prompt

    Define your own instruction, such as:

    > “Extract only numbers and email addresses from the image.”

    > “Summarize the main points in bullet form.”

Use this to tailor the AI’s output to your use case.

***

#### ✍️ Text Output Position

Select where the extracted text will appear in the forwarded message:

*   Prepend to Caption

    Adds the OCR result before the existing message content.

    _Example_:

```
[Extracted Text from Image]
---
Original forwarded message content

```

* (Future options may include: _Append to Caption_, _Replace Message Content_, etc.)

***

### 🔒 Requirements

* Must have a valid OpenAI API key with access to vision models.
* Your chosen model must support both image inputs and textual outputs.
