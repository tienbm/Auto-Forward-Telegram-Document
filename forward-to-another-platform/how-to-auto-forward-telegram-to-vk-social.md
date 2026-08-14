# VK Social Publisher

### What it is

VK publishing has been improved to make destination setup easier and more accurate.

You can now choose whether your destination is a **VK Profile** or a **VK Community/Page**, then paste a VK URL or ID and let the app normalize it automatically.

### Where to find it

You will see these improvements in:

* the **Publish** task creation flow
* the **Publish** task detail flow
* the **Add Platform Account** flow for VK connection

### How to set it up

1. Open **Publish**.
2. Create a new publish task or edit an existing one.
3. Select **VK** as the publishing platform.
4. Choose the destination type:
   * `VK Profile`
   * `VK Community/Page`
5. Paste a VK URL or enter a VK ID.
6. Review the destination preview.
7. Save the task.

### How it works

AutoForward now interprets VK input more intelligently.

For example:

* a VK profile stays a positive user ID
* a VK community or page is normalized into the correct community target ID

This reduces manual setup mistakes and makes destination handling more reliable.

### Examples

#### VK Profile

Input:

```
https://vk.com/id647480210
```

Normalized target:

```
647480210
```

#### VK Community/Page

Input:

```
https://vk.com/public216874049
```

Normalized target:

```
-216874049
```

### Why it is useful

* It makes VK publishing easier to configure.
* It reduces destination mistakes.
* It helps you verify where your content will be published before saving.
* It improves the overall VK connection experience on both mobile and web.

### Notes

* VK Profile uses a positive ID.
* VK Community/Page uses the normalized community target format.
* If the input is invalid, AutoForward will ask you to correct it before saving.
