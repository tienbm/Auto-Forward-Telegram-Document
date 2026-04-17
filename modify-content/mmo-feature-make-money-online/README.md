# 🪙 MMO Feature - Make Money Online

### Overview

**MMO Feature** allows users to automatically convert product links in forwarded messages into affiliate links, earning commission from supported e-commerce platforms.

### UI Structure

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### Supported Platforms

#### 1. Amazon Affiliate

* **Config**: Amazon Tag (e.g., `mystore-20`)
* **Auto Product Info**: Fetch product title, price, rating automatically
* **Color**: Orange

#### 2. Awin Affiliate

* **Config**: Awin Affiliate ID
* **Color**: Blue

#### 3. eBay Partner Network

* **Config**: eBay Campaign ID
* **Color**: Red (#E53238)

#### 4. AliExpress Affiliate

* **Config**: AliExpress Tracking ID
* **Color**: Red (#FF4747)

#### 5. Shopee Affiliate

* **Config**: Shopee Affiliate ID
* **Color**: Orange (#EE4D2D)

### How It Works

```
Original Message:
"Check this product: https://amazon.com/product/B08XYZ123"

After Processing:
"Check this product: https://amazon.com/product/B08XYZ123?tag=mystore-20"
                                                          ^^^^^^^^^^^^^^^^
                                                          Affiliate tag added
```

### Features by Platform

#### Amazon

* Link conversion with affiliate tag
* Optional auto-fetch: product name, price, rating
* Works with all Amazon domains (.com, .co.uk, .de, etc.)

#### Awin

* Universal link conversion for Awin partners
* Supports multiple merchants (ShareASale, Rakuten, etc.)

#### eBay

* Campaign ID tracking
* Works with eBay global marketplace

#### AliExpress

* Tracking ID injection
* Deep link generation

#### Shopee

* Affiliate ID tracking
* Regional marketplace support (SG, MY, TH, VN, PH)

### Use Cases

#### Use Case 1: Product Review Channel

```
Enable: Amazon + eBay
→ All product links automatically converted to affiliate links
→ Earn commission on purchases
```

#### Use Case 2: Deal Hunter Bot

```
Enable: AliExpress + Shopee
→ Forward deals from deal channels
→ Add affiliate tracking to all links
```

#### Use Case 3: Multi-Platform Store

```
Enable: All platforms
→ Forward from supplier channels
→ Auto-convert all product links
```

#### Header

* Icon: Monetization (dollar sign)
* Title: "MMO Feature"
* Description: Feature overview

#### Platform Cards

Each platform has:

* **Brand Color**: Platform-specific color scheme
* **Toggle Switch**: Enable/disable platform
* **Input Fields**: Platform-specific IDs/tags
* **Helper Text**: Setup instructions

### Benefits

* **Passive Income**: Earn commission automatically
* **Multi-Platform**: Support 5 major e-commerce networks
* **Zero Manual Work**: Auto-convert all links
* **Transparent**: Original message preserved
* **Flexible**: Enable/disable per platform

### Setup Guide

1. **Register Affiliate**: Sign up for affiliate program
2. **Get ID/Tag**: Copy your affiliate identifier
3. **Enable Platform**: Toggle switch ON
4. **Enter ID**: Paste affiliate ID/tag
5. **Save**: Tap "Save" button
6. **Done**: All product links auto-converted

