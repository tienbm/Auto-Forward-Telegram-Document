---
icon: sack-dollar
---

# Replace Affiliate Marketing Amazon,Shopee, Awin, eBay, Ali,..

### 1. What is Affiliate Monetization?

Affiliate Monetization automatically processes affiliate links when forwarding messages. Enter your affiliate ID for each platform, and the system will automatically replace the corresponding tracking ID in supported links.

You do not need to configure every platform. Enable only the platforms you use.

### UI Structure

<div><figure><img src="../../.gitbook/assets/image (265).png" alt="" width="563"><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/image (267).png" alt="" width="558"><figcaption></figcaption></figure></div>

### 2. Supported Platforms

| Platform   | Required information             | Example      |
| ---------- | -------------------------------- | ------------ |
| Amazon     | Amazon Affiliate Tag             | `mystore-20` |
| Awin       | Awin Affiliate ID / Publisher ID | `123456`     |
| eBay       | eBay Campaign ID                 | `12345678`   |
| AliExpress | AliExpress Tracking ID           | `ABC123`     |
| Shopee     | Shopee Affiliate ID              | `99999911`   |

### 3. How to Set It Up

1. Open the message forwarding task.
2. Open the feature settings and select **Affiliate Monetization**.
3. Enable the affiliate platform you want to use.
4. The full configuration section will appear automatically.
5. Enter the correct affiliate ID in the corresponding field.
6. For Amazon, optionally enable **Auto Fetch Product Info** to automatically retrieve the product title, price, and image from Amazon links.
7. Tap **Save**.

### 4. How to Find Your Shopee Affiliate ID

{% embed url="https://youtu.be/QRyj6Ye5los" %}

Some Shopee links contain the affiliate ID in this format:

```
utm_source=an_99999911
```

The Affiliate ID is:

```
99999911
```

Do not include the `an_` prefix when the field requires a numeric Affiliate ID. This format is described in Shopee’s affiliate link guide. [View Shopee’s guide](https://help.shopee.co.id/portal/10/article/184879-\[Shopee-Affiliate-Program]-Pedoman-Pembuatan-Link-Pendek-Affiliate)

{% hint style="info" %}
#### Optional: Set Up Automatic Short URLs For Shopee URL

Automatic short URL generation creates shortened links for Shopee affiliate URLs while your content is being processed. The feature uses a verified teleURL credential. [Checkout](set-up-automatic-short-urls-for-shopee-url.md)
{% endhint %}

<figure><img src="../../.gitbook/assets/image (289).png" alt=""><figcaption></figcaption></figure>

### 5. After Saving

When the task receives a message containing a link from an enabled platform, the system automatically processes the link using the affiliate ID you entered.

Only enabled platforms are applied. Disabled platforms will not have their affiliate IDs added or replaced.

### 6. Common Issues

#### The affiliate ID was not applied

Check the following:

* The corresponding platform is enabled.
* The affiliate ID is correct.
* You tapped **Save** after making changes.
* The link belongs to a supported platform.

#### The configuration cannot be saved

Every enabled platform must have a corresponding affiliate ID. Enter all required information before saving.

#### Amazon product information is not displayed

Product information depends on the Amazon link and the data provided by Amazon. Make sure the link is a valid product link.

### 7. Notes

* Each platform has its own affiliate ID.
* Do not use a Shop ID or Product ID instead of an Affiliate ID.
* Copy the ID directly from your affiliate account to avoid mistakes.
* Commission tracking depends on each affiliate platform’s policies.

