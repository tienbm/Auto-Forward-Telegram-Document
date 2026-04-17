---
icon: puzzle-piece
---

# Smart Image Crop

### Overview

Smart Image Crop is an addon that automatically crops images before forwarding them to your target channels. This is perfect for removing unwanted watermarks, channel stamps, promotional banners, or any edges you want to eliminate from images.

#### What Problem Does It Solve?

When forwarding images from other channels, you often encounter:

* **Channel watermarks** at the top or bottom of images
* **Promotional banners** advertising the source channel
* **Unwanted borders** that make images look unprofessional
* **Screenshots with UI elements** like status bars or navigation
* **Inconsistent image dimensions** that need standardization

Smart Image Crop removes these automatically before the image reaches your audience.

#### Key Benefits

✅ **Automatic processing** - No manual editing required\
✅ **Precise control** - Set exact pixel or percentage values for each edge\
✅ **Live preview** - See exactly what will be cropped before activating\
✅ **Batch processing** - Apply to all images in your forwarding task\
✅ **Non-destructive** - Original images remain unchanged in source\
✅ **Preserve quality** - No compression or quality loss during crop

***

### How It Works

#### Processing Flow

1. **Message arrives** from source channel containing an image
2. **Bot downloads** the image temporarily
3. **Crop algorithm** applies your configured crop values
4. **New image** is created with specified edges removed
5. **Forwarded image** is sent to targets with the crop applied
6. **Temporary files** are cleaned up automatically

#### Technical Details

* **Processing time**: 1-3 seconds per image (minimal delay)
* **Supported formats**: JPEG, PNG, WebP (standard Telegram photo formats)
* **Not supported**: GIFs, stickers, videos, documents
* **Maximum resolution**: Up to 10MB image file size
* **Aspect ratio**: Can be preserved or adjusted based on your settings

***

### Getting Started

#### Prerequisites

Before you can use Smart Image Crop:

1. ✅ Purchase the addon using credits
2. ✅ Have an active forwarding task
3. ✅ Ensure your task forwards photo messages

#### Step-by-Step Setup

**Step 1: Purchase the Addon**

1. Open AutoForward app
2. Navigate to **Menu → My Addons**
3. Search for "Smart Image Crop" or find it in **Content Tools** category
4. Tap **Unlock**
5. Choose duration (30/90/365 days - longer = better value)
6. Confirm purchase with your credits

**Step 2: Enable in Your Task**

1. Open **Tasks** screen
2. Select the task where you want to use image cropping
3. Tap to edit the task
4. Scroll to **Image Settings** or **Content Settings** section
5. Find **Smart Image Crop** settings
6. Toggle **Enable Image Crop** to ON

**Step 3: Configure Crop Values**

Choose your **Crop Mode**:

**Option A: Pixels Mode** (best for consistent image sizes)

```
Top: 50 pixels
Bottom: 100 pixels
Left: 0 pixels
Right: 0 pixels
```

**Option B: Percent Mode** (best for varying image sizes)

```
Top: 5%
Bottom: 10%
Left: 0%
Right: 0%
```

**Step 4: Preview Your Crop**

1. Tap **Preview** button
2. The preview shows red overlay on areas that will be cropped
3. Adjust values if needed
4. Preview updates in real-time

**Step 5: Save and Test**

1. Tap **Save** to apply settings
2. Send a test image through your source channel
3. Check the forwarded result in your target
4. Fine-tune crop values if needed

***

### Configuration Details

#### Crop Mode Selection

**Pixels Mode**

**When to use:**

* You know exact dimensions of unwanted elements (e.g., "50-pixel watermark")
* Source images are mostly the same size
* You need precise control

**How it works:**

* Removes exact number of pixels from each edge
* Example: Top=50 removes top 50 pixels regardless of image size
* 1920x1080 image with Top=50, Bottom=50 becomes 1920x980

**Pros:**

* Exact precision
* Predictable results

**Cons:**

* May crop too much on small images
* May crop too little on large images

**Percent Mode**

**When to use:**

* Source images vary in size
* You want proportional cropping
* You're removing watermarks at relative positions

**How it works:**

* Removes percentage of total dimension
* Example: Top=10% removes top 10% of height
* 1920x1080 (10% top) = removes 108 pixels
* 960x540 (10% top) = removes 54 pixels

**Pros:**

* Scales with image size
* Works for any resolution
* Consistent appearance

**Cons:**

* Less precise for exact pixel counts

#### Edge Configuration

You can set different crop values for each edge independently:

**Top Edge**

* Removes pixels/percentage from the **top** of the image
* Common uses: Remove channel names, timestamps, headers
* Typical values: 5-15% or 50-150 pixels

**Bottom Edge**

* Removes pixels/percentage from the **bottom** of the image
* Common uses: Remove watermarks, promotional text, footers
* Typical values: 5-15% or 50-150 pixels

**Left Edge**

* Removes pixels/percentage from the **left** of the image
* Common uses: Remove side stamps, date overlays
* Typical values: 0-10% or 0-100 pixels

**Right Edge**

* Removes pixels/percentage from the **right** of the image
* Common uses: Remove side stamps, logos
* Typical values: 0-10% or 0-100 pixels

#### Validation Rules

The system enforces these limits to prevent invalid crops:

**Percent Mode:**

* Top + Bottom must be **< 100%**
  * ✅ Valid: Top 40% + Bottom 40% = 80%
  * ❌ Invalid: Top 60% + Bottom 50% = 110%
* Left + Right must be **< 100%**
  * ✅ Valid: Left 30% + Right 30% = 60%
  * ❌ Invalid: Left 70% + Right 40% = 110%

**Pixels Mode:**

* All values must be **≥ 0**
  * ✅ Valid: Top 50, Bottom 0
  * ❌ Invalid: Top -10, Bottom 50

**Why these rules?** Cropping 100% or more from any dimension would leave no image.

#### Preserve Aspect Ratio

**Option**: Toggle ON/OFF

**When enabled:**

* The image's width-to-height ratio stays the same after cropping
* Useful for maintaining screen-friendly proportions
* May result in additional automatic cropping to maintain ratio

**When disabled:**

* Image dimensions change based only on your crop values
* Final aspect ratio may be different from original
* Gives you exact control over final dimensions

**Recommendation**: Leave **OFF** for most use cases. Enable only if you need specific aspect ratios (e.g., 16:9 for videos, 1:1 for Instagram-style posts).

***

### Common Use Cases

#### Remove Bottom Watermark

**Example**: Channel adds 80px watermark at bottom

```
Mode: Pixels
Bottom: 80
```

#### Remove Header & Footer

**Example**: 10% header, 15% footer (varying image sizes)

```
Mode: Percent
Top: 10%, Bottom: 15%
```

#### Clean Screenshot Edges

**Example**: Remove status bar and navigation

```
Mode: Pixels
Top: 50, Bottom: 100
```

#### Multiple Sources

Create separate tasks with different crop settings for each source channel.

***

### Advanced Features

#### Real-Time Preview

The preview feature helps you visualize crops before activating:

**How to use:**

1. Configure your crop values
2. Tap **Preview** button
3. View a sample image with **red overlay** showing crop areas
4. Adjust values and preview updates instantly

**Preview tips:**

* Red areas = what will be removed
* White/clear areas = what remains in final image
* If you can't see preview, toggle "Enable Image Crop" ON first
* Preview uses a standard test image, actual results may vary slightly

#### Dynamic Adjustment

You can change crop values anytime:

1. Edit task settings
2. Update Smart Image Crop values
3. Save changes
4. New crop applies to **all future images** immediately
5. Previously forwarded images are not affected

**Use cases:**

* Source channel changes watermark size
* Seasonal adjustments (holiday branding)
* A/B testing different crop approaches

#### Combining with Other Features

Smart Image Crop works seamlessly with:

✅ **Caption filters** - Crop image + modify text\
✅ **URL replacement** - Clean image + change links\
✅ **Button cloning** - Crop image + preserve buttons\
✅ **Media filters** - Only process specific media types

***

### Troubleshooting

#### Issue: Preview Shows But Nothing Crops

**Possible causes:**

* ✅ Check "Enable Image Crop" toggle is ON
* ✅ Verify addon hasn't expired (check My Addons)
* ✅ Save settings after making changes
* ✅ Test with a new image (old images won't be reprocessed)

**Fix:**

1. Open task settings
2. Confirm toggle is ON
3. Tap Save
4. Send a fresh test image through source channel

***

#### Issue: Too Much Is Being Cropped

**Possible causes:**

* Values are too high
* Using pixels on varying image sizes
* Aspect ratio preservation causing extra crop

**Fix:**

**If using Pixels:**

* Reduce pixel values by 50% and test
* Consider switching to Percent mode

**If using Percent:**

* Lower percentages (try 5% instead of 10%)

**If Aspect Ratio ON:**

* Try turning it OFF
* The system may be auto-cropping to maintain ratio

***

#### Issue: Not Cropping Enough

**Possible causes:**

* Values are too low
* Wrong crop mode for your needs
* Not all edges configured

**Fix:**

1. Increase values gradually (add 5% or 20 pixels at a time)
2. Check all four edges - you may need to crop multiple sides
3. Use Preview to see exactly what's being removed
4. Test with actual source images, not test images

***

#### Issue: Images Look Distorted

**Possible causes:**

* "Preserve Aspect Ratio" is ON but shouldn't be
* Cropping uneven amounts from width vs height

**Fix:**

1. Turn "Preserve Aspect Ratio" **OFF**
2. Review crop values - try to keep proportional if maintaining shape
3. Example for square crop: If Top+Bottom = 20%, also do Left+Right = 20%

***

#### Issue: "Invalid Crop Percent" Error

**Cause:** Your crop values exceed 100% on an axis

**Fix:** Check your math:

* Top 60% + Bottom 50% = 110% ❌ (reduce to Top 50% + Bottom 40%)
* Left 70% + Right 40% = 110% ❌ (reduce to Left 60% + Right 30%)

**Rule**: Top+Bottom < 100% and Left+Right < 100%

***

#### Issue: Some Images Not Cropping

**Possible causes:**

* Image is not a photo (videos, GIFs, stickers are not processed)
* Image is sent as document/file instead of photo
* Image exceeds size limits

**Fix:**

1. Check source sends images as **photos** not **documents**
2. Smart Image Crop only works on standard photo messages
3. For other media types, source must send as photo

***

#### Issue: Cropped Images Look Low Quality

**Note:** Smart Image Crop does NOT compress or reduce quality. If you're seeing quality issues:

**Actual causes:**

* Telegram's own compression (happens on all photos)
* Source image was already low quality
* Extreme cropping makes artifacts more visible

**Not caused by Smart Image Crop:**

* The addon performs lossless cropping
* Output quality = input quality (minus cropped areas)

**Workaround:**

* Request source use higher quality images
* No control over Telegram's automatic compression

***

### Best Practices

#### Start Small, Adjust Gradually

Begin with conservative values (5%, 50px) and increase until watermark is removed.

#### Use Percent for Mixed Sizes

When images vary in size, Percent mode ensures consistent proportional cropping.

#### Test Before Production

Create a test task forwarding to your private channel first. Test 5-10 images before applying to main task.

#### Common Crop Values

| Watermark Position | Typical Crop               |
| ------------------ | -------------------------- |
| Bottom watermark   | Bottom: 10-20% or 80-150px |
| Top header         | Top: 5-15% or 50-100px     |
| Side stamps        | Left/Right: 5-10%          |

#### Combine with Other Addons

Works well with Auto Clone Button, Caption filters, and other content tools.

***

### Frequently Asked Questions

#### Does it work on all image types?

**Photos**: ✅ Yes\
**GIFs**: ❌ No\
**Stickers**: ❌ No\
**Videos**: ❌ No\
**Documents sent as images**: ❌ No (must be sent as photo)

#### Can I crop different amounts on different tasks?

**Yes!** Each task has independent Smart Image Crop settings. Configure separately for each task/source.

#### Will it reprocess old images if I change settings?

**No.** Only new images (received after you save settings) are cropped. Previously forwarded images remain unchanged.

#### Can I temporarily disable without losing settings?

**Yes!** Just toggle "Enable Image Crop" to OFF. Your crop values are saved and ready when you toggle back ON.

#### Does it slow down forwarding?

**Minimal impact.** Processing adds 1-3 seconds per image. Most users won't notice the delay.

#### What if I accidentally crop too much?

**Solution:**

1. Go back to task settings
2. Reduce crop values
3. Save changes
4. Forward a new test image
5. Old images cannot be uncropped (they're already sent)

#### Can I see what will be cropped before activating?

**Yes!** Use the **Preview** feature. It shows red overlay on areas that will be removed.

#### Does cropping reduce image quality?

**No.** Cropping is lossless. The remaining image maintains original quality. Any compression is from Telegram, not the addon.

#### Can I use it with Button Clone and other addons?

**Yes!** Smart Image Crop works seamlessly with all other addons. Process independently.

#### What happens when the addon expires?

* Cropping stops immediately
* Your settings are preserved
* Images forward without crop applied
* Renew to reactivate with same settings

#### Can I export/import crop settings between tasks?

**Not directly**, but you can:

1. Note down your settings
2. Manually apply to new tasks
3. Use same values for consistency

***

### Performance Optimization

#### For High-Volume Forwarding

If you forward many images per day:

**Best practices:**

* Use **Percent mode** (faster than Pixels for varying sizes)
* Keep crop values moderate (extreme crops process slower)
* Consider multiple tasks to distribute load
* Monitor bot performance in Task Statistics

#### For Mixed Content

If your source sends photos + other media:

**Setup:**

* Enable Smart Image Crop
* Photos will be cropped automatically
* Other media (GIFs, videos, stickers) pass through unchanged
* No configuration needed for mixed handling

***

### Getting Help

If you're still experiencing issues:

1. **Re-read relevant sections** above for your specific problem
2. **Check Addons FAQ** for more Q\&A
3. **Test in isolated environment** (new task, single target, test images)
4. **Contact support** with:
   * Screenshots of your crop settings
   * Example original and cropped images
   * Task configuration details
   * What you expected vs. what happened

**Support channels:**

* In-app: Menu → Help & Support
* Email: support@autoforwardtelegram.com
* Community: Telegram group

***

### Summary

Smart Image Crop is a powerful tool for professional content curation. Key takeaways:

✅ Removes unwanted watermarks, headers, footers automatically\
✅ Works with both fixed pixel and dynamic percentage cropping\
✅ Live preview shows exactly what will be removed\
✅ Processes images in 1-3 seconds with no quality loss\
✅ Configure independently per task for different sources\
✅ Combines seamlessly with other AutoForward features

**Next steps:**

1. Purchase the addon if you haven't yet
2. Test on a small task with known images
3. Gradually expand to production forwarding
4. Monitor and adjust as sources change

**Related documentation:**

* All Addons Overview
* Addons Quick Reference
* Addons FAQ

***

**Last Updated**: March 2026\
**Addon Version**: 1.0\
**App Version**: 1.0.44+
