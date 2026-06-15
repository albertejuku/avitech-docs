# Subscribers

The Subscribers section is the core of the billing portal. Every internet customer is a subscriber — this is where you create accounts, monitor connectivity, manage subscriptions, process payments, and take action on individual accounts.

## What You Can Do

- View all subscribers with live online/offline status
- Filter by status, zone, router, or service type
- Add new subscribers
- Suspend, reactivate, or terminate accounts
- View per-subscriber subscription, payment history, and traffic
- Send SMS or email to individual subscribers
- Bulk-extend subscriptions for a group of subscribers
- Import subscribers from CSV / export the list

## Key Concepts

**Account Number** — A unique identifier automatically assigned to each subscriber. Used for support and billing references.

**Status** — The current billing/account state of the subscriber:

| Status | Meaning |
|---|---|
| Active | Account is in good standing, internet access is provisioned |
| Suspended | Access has been removed, usually due to non-payment |
| Terminated | Account permanently closed |
| Draft | Account created but not yet activated |

**Online Status** — The real-time network connection state (independent of billing status):

| Online Status | Meaning |
|---|---|
| Online | Subscriber is currently connected and passing traffic |
| Offline | Subscriber is not connected |
| No Internet | Connected to the network but traffic is blocked (e.g. suspended) |

**Service Type** — The type of network connection:

| Type | Description |
|---|---|
| PPPoE | Dial-up style authentication via RADIUS |
| Static | Fixed IP address assigned to the subscriber |
| Hotspot | Captive portal / WiFi access |

## Navigation

- [Subscriber List](list.md) — search, filter, and act on all subscribers
- [Adding a Subscriber](creating.md) — step-by-step account creation
- [Subscriber Details](details.md) — the full detail page and its tabs
- [Subscription Tab](subscription-tab.md) — manage plans, renewals, grace period
- [Payments Tab](payments-tab.md) — per-subscriber payment history
- [Sending Messages](messaging.md) — SMS and email
- [Bulk Operations](bulk-operations.md) — extend subscriptions, push static routes
