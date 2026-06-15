# Subscriptions

The Subscriptions page gives you a high-level view of all active, expired, suspended, and expiring subscriptions across your entire subscriber base — along with live revenue metrics.

*Screenshot: Subscriptions page overview — add image here*

## Navigation

- [Revenue Metrics](metrics.md) — MRR, ARR, MTD, YTD revenue cards
- [Renewing & Changing Plans](renewing.md) — renew, extend, and switch plans
- [Suspending & Cancelling](managing.md) — suspend access or cancel a subscription

## Quick Concept Recap

A **subscription** links a subscriber to a plan for a defined period. Every subscriber has one active subscription at a time. When a subscription expires, the subscriber enters a grace period before being automatically suspended.

## Subscription Statuses

| Status | Description |
|---|---|
| Active | Within the paid period, internet access is live |
| Expiring | Active but expires within 7 days — renewal action recommended |
| Expired | Period ended, subscriber is in grace period |
| Suspended | Access removed due to non-payment or manual suspension |
| Cancelled | Subscription was explicitly cancelled by an admin |

## Filters

| Filter | Options |
|---|---|
| Status buttons | All, Active, Expired, Suspended, Expiring (within 7 days) |
| Search | Name, username, phone number, or plan name |

## Table Columns

| Column | Description |
|---|---|
| Subscriber | Full name and RADIUS username |
| Plan | Name of the service plan |
| Price | Subscription price |
| Start Date | When the current period began |
| Expires | When the current period ends |
| Days Left | Color-coded: green (>5 days), amber (≤5 days), red (expired / negative) |
| Status | Subscription status chip |
| Actions | Per-row action menu |

## Per-Row Actions

| Action | When Available |
|---|---|
| View Subscriber | Always — opens the subscriber detail page |
| Renew / Change Plan | Always — opens the renewal dialog |
| Suspend | Status = Active or Expiring |
| Reactivate | Status = Suspended |
| Cancel Subscription | Status = Active or Suspended |
