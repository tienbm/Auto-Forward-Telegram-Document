---
description: >-
  Send real-time webhook notifications to your external systems whenever Auto
  Forward Telegram successfully forwards, edits, or deletes messages.
icon: puzzle
---

# Outbound Webhooks

This addon allows you to integrate forwarding activities with your own applications, CRM systems, analytics platforms, automation workflows, monitoring tools, or custom business processes.

### How It Works

When a configured task successfully performs an action, Auto Forward Telegram sends an HTTPS POST request to your configured webhook endpoint.

Supported lifecycle events:

* New Message Forwarded
* Message Edited
* Message Deleted

Each webhook can be independently configured to receive only the events you need.

### Features

#### Real-Time Message Notifications

Receive webhook notifications immediately after messages are successfully forwarded.

Typical use cases:

* Store forwarded messages in your database
* Trigger automation workflows
* Update dashboards
* Send alerts to internal systems
* Synchronize content across platforms

***

#### Message Edit Events

Track when previously forwarded messages are updated.

When enabled, your webhook endpoint receives notifications whenever Auto Forward Telegram successfully edits a target message.

Examples:

* Maintain synchronized archives
* Update external content feeds
* Track message revision history
* Refresh cached content

***

#### Message Delete Events

Receive notifications when forwarded messages are deleted.

This is especially useful when combined with:

* Auto Delete Messages
* Manual deletion workflows
* Content expiration systems

Examples:

* Remove content from external databases
* Trigger cleanup workflows
* Update reporting systems
* Archive deleted message information

***

#### Multiple Webhook Endpoints

Each task can deliver events to multiple destinations.

Supported:

* Up to 3 webhook endpoints per task

Examples:

Endpoint 1:

* Internal CRM

Endpoint 2:

* Analytics Platform

Endpoint 3:

* Monitoring System

Each endpoint can have its own:

* Events
* Secret key
* Retry settings
* Timeout settings
* Payload configuration

***

#### Event Filtering

Choose which events each endpoint should receive.

Available events:

| Event           | Description                                   |
| --------------- | --------------------------------------------- |
| new\_message    | Triggered after a successful forward          |
| edit\_message   | Triggered after a successful message edit     |
| delete\_message | Triggered after a successful message deletion |

Example:

Webhook A:

* new\_message only

Webhook B:

* edit\_message + delete\_message

Webhook C:

* all events

***

#### Signed Webhook Requests

Protect your integrations using webhook signatures.

Each endpoint can define its own signing secret.

When configured:

* Every webhook request is cryptographically signed
* Your server can verify authenticity
* Prevents spoofed requests
* Improves security for production integrations

This is strongly recommended for all public-facing endpoints.

***

#### Selective Payload Data

Control which information is included in webhook payloads.

**Include Message Text**

Include forwarded message text or captions.

Useful for:

* Content synchronization
* Search indexing
* Analytics
* Archiving

**Include Source Information**

Include source chat information.

Useful for:

* Channel tracking
* Reporting
* Source attribution

**Include Target Information**

Include destination chat information.

Useful for:

* Delivery monitoring
* Multi-channel analytics
* Distribution reporting

***

#### Configurable Timeouts

Specify how long the system waits for your server to respond.

Supported range:

* Minimum: 1 second
* Maximum: 10 seconds

Recommended:

* 3–5 seconds

If your endpoint does not respond within the configured timeout, the request is considered failed.

***

#### Automatic Retry Handling

Failed webhook deliveries can be retried automatically.

Supported range:

* 0 to 3 retries

Example:

Max Retries:

* 2

Result:

* Initial attempt
* Retry #1
* Retry #2

This improves reliability during temporary outages or network issues.

### Typical Use Cases

#### CRM Integration

Send forwarding activity directly into your CRM system.

Examples:

* Lead tracking
* Customer communication logs
* Sales notifications

***

#### Analytics & Reporting

Track message delivery events inside your analytics platform.

Examples:

* Message volume reporting
* Source performance metrics
* Destination engagement tracking

***

#### Automation Platforms

Trigger workflows in:

* Zapier
* Make (Integromat)
* n8n
* Pipedream
* Custom automation systems

Examples:

* Create records automatically
* Send notifications
* Launch follow-up workflows

***

#### External Databases

Store forwarding activity in:

* MySQL
* PostgreSQL
* MongoDB
* Firebase
* Supabase

Examples:

* Message archiving
* Compliance logging
* Historical reporting

***

#### Monitoring & Alerting

Receive notifications whenever important forwarding activity occurs.

Examples:

* Slack alerts
* Discord notifications
* Internal monitoring systems
* Operations dashboards

### Security Recommendations

For production environments:

✓ Use HTTPS endpoints only

✓ Configure a signing secret

✓ Verify signatures before processing requests

✓ Keep timeout values reasonable

✓ Use retries for temporary failures

✓ Restrict endpoint access where possible

### Configuration Limits

| Setting                    | Limit        |
| -------------------------- | ------------ |
| Maximum Endpoints Per Task | 3            |
| Supported Events           | 3            |
| Timeout Range              | 1–10 Seconds |
| Maximum Retries            | 3            |
| Signing Secret             | Optional     |

### Example Configuration

Endpoint:

* https://api.example.com/webhooks/telegram

Events:

* new\_message
* edit\_message

Include Text:

* Enabled

Include Source:

* Enabled

Include Target:

* Enabled

Timeout:

* 5 seconds

Retries:

* 2

Signing Secret:

* configured

Result:

Whenever the task forwards or edits a message, a signed webhook request is sent to your endpoint with the selected event data.

### Benefits

* Integrate Auto Forward Telegram with any system
* Build real-time automations
* Receive message lifecycle notifications
* Synchronize external databases
* Improve monitoring and reporting
* Secure integrations with signed requests
* Configure independently for each forwarding task

Short Marketplace Description

Send signed HTTPS webhooks to your systems whenever messages are forwarded, edited, or deleted. Integrate Auto Forward Telegram with CRMs, databases, analytics platforms, and automation tools in real time.
