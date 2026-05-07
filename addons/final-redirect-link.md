---
icon: puzzle
---

# Final Redirect Link

### Overview

Final Redirect Link is an advanced link processing addon designed to automatically resolve shortened or redirected URLs inside forwarded Telegram messages.

When a forwarded message contains shortened links such as Bitly, TinyURL, tracking links, or redirect-based URLs, the system will detect and resolve them to their actual final destination before forwarding the message.

This helps users:

* View the real destination URL
* Remove tracking or redirect layers
* Increase transparency and trust
* Improve link readability
* Avoid hidden or unsafe redirects

***

## Core Features

### 1. Resolve Final Destination URLs

The addon automatically follows redirect chains and retrieves the final destination URL from:

* Shortened links
* Tracking links
* Redirect-based URLs

#### Example

Original forwarded message:

```
https://bit.ly/example-link
```

Resolved result:

```
https://example.com/product-page
```

***

### 2. Replace or Append Final URLs

Users can choose how resolved links are handled.

#### Replace Mode

Replace the original shortened link completely.

Example:

```
Before:
https://bit.ly/example

After:
https://example.com/page
```

#### Append Mode

Keep the original link and append the final destination.

Example:

```
https://bit.ly/example
→ https://example.com/page
```

***

## Telegram Message Support

The addon supports processing links inside:

* Forwarded message text
* Message captions
* Media captions
* Auto-forwarded Telegram content

This allows seamless integration with Telegram forwarding and automation systems.

***

## Domain Filtering System

Users can configure:

* Include domains
* Exclude domains

per forwarding task.

### Include Domains

Only resolve links from specified domains.

Example:

```
bit.ly
t.co
tinyurl.com
```

### Exclude Domains

Skip resolving links from selected domains.

Example:

```
youtube.com
google.com
```

This helps optimize performance and avoid unnecessary processing.

***

## Link Processing Limits

To improve performance and reduce API load, users can configure:

* Maximum number of links to resolve per message

Example:

* Resolve only first 3 links
* Skip remaining links automatically

***

## Smart Redirect Resolver

The system uses:

* HTTP HEAD requests for fast redirect detection
* Automatic GET fallback for websites that block HEAD requests

This improves compatibility with:

* Cloudflare-protected sites
* Anti-bot systems
* Websites with strict HTTP rules

***

## Security Protection

The addon automatically blocks unsafe redirect targets including:

* Localhost addresses
* Private IP addresses
* Reserved network ranges
* Potentially unsafe redirect destinations

This helps prevent:

* Internal network abuse
* SSRF-related attacks
* Unsafe redirect chains

***

## Fail-Safe Processing

If:

* Timeout occurs
* Resolver fails
* Target website is unavailable

the forwarding process will continue normally.

This ensures:

* Forwarding tasks are never blocked
* Better system stability
* Reliable automation performance

***

## Use Cases

### Affiliate Marketing

Convert shortened affiliate links into visible destination URLs.

### Content Transparency

Allow users to see the real destination before clicking.

### Anti-Tracking

Remove unnecessary redirect and tracking layers.

### Telegram Automation

Automatically clean and normalize links during auto-forwarding workflows.

### Security Review

Inspect hidden redirect destinations before sharing content.

***

## Summary

Final Redirect Link provides a secure and intelligent way to resolve redirected URLs inside Telegram forwarded content.

Key advantages:

* Automatic redirect resolution
* Flexible link replacement modes
* Advanced filtering system
* Safe redirect validation
* Non-blocking forwarding workflow
* Optimized for Telegram automation systems
