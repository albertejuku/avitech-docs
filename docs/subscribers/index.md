# Subscribers

Every internet customer is a subscriber. This is where you create accounts, assign plans, monitor connectivity, process payments, and manage their lifecycle.

## Subscriber Statuses

A subscriber has two independent states — their billing status and their live connection status.

| Billing Status | Meaning |
|---|---|
| Active | Account is in good standing, can access the internet |
| Suspended | Access removed, usually for non-payment |
| Terminated | Account permanently closed |
| Draft | Account created but not yet activated |

| Connection Status | Meaning |
|---|---|
| Online | Connected and passing traffic |
| Offline | Not currently connected |
| No Internet | Connected to the network but blocked from internet access |

## Service Types

| Type | How it works |
|---|---|
| PPPoE | Subscriber logs in with a username and password via RADIUS |
| Static IP | Subscriber has a fixed IP address assigned |
| Hotspot | Captive portal / WiFi access |

## Pages in This Section

- [Subscriber List](list.md) — browse, search, filter, and act on all subscribers
- [Adding a Subscriber](creating.md) — create a new subscriber account
- [Subscriber Details](details.md) — the full detail page and its tabs
- [Subscription Tab](subscription-tab.md) — plans, renewals, grace period
- [Payments Tab](payments-tab.md) — per-subscriber payment history
- [Sending Messages](messaging.md) — SMS and email to subscribers
- [Bulk Operations](bulk-operations.md) — extend subscriptions, import, export
