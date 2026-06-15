# Subscription Tab

Found on the [Subscriber Details](details.md) page, the Subscription tab shows the subscriber's current plan and gives you full control over renewals, plan changes, and account suspension.

*Screenshot: Subscription tab — add image here*

## Current Plan Card

The left side of the tab shows the subscriber's active subscription:

| Field | Description |
|---|---|
| Plan Name | The name of the service plan |
| Price | Monthly (or per-cycle) cost in KES |
| Speed | Download / Upload speeds from the plan's speed profile |
| Auto-Renew | Whether the subscription auto-renews at expiry |
| Start Date | When the current subscription period began |
| Expiry Date | When the current period ends. Shown in red if expired, amber if expiring within 7 days |

### Time Remaining Progress Bar

If the subscription is active, a green progress bar shows how much of the billing period remains:

```
[================          ] 12 days of 30
```

### Grace Period Progress Bar

If the subscription has expired but is still within the grace period (default 7 days), a red bar shows how much grace has been used:

```
[=====                     ] 3 / 7 days used  (auto-suspends in 4 days)
```

!!! warning "Grace Period"
    Once the grace period expires, the subscriber is automatically suspended and loses internet access. Reactivating requires a renewal payment.

---

## Quick Actions Card

The right side of the tab has shortcut buttons for common operations:

| Action | Description |
|---|---|
| Renew / Change Plan | Opens the renewal dialog (see below) |
| Quick Extend | Add a number of days to the current subscription without changing the plan or recording a payment |
| Reset MAC Binding | Clears the MAC address bound to this subscriber's RADIUS session — useful if a subscriber changes their router |
| Re-provision | For Static IP subscribers — re-pushes the IP assignment to the router |
| Force Redial (CoA) | For PPPoE subscribers — sends a Change of Authorization to disconnect and re-authenticate the subscriber |
| Suspend | Removes internet access (available when status is ACTIVE) |
| Reactivate | Restores internet access (available when status is SUSPENDED) |
| Terminate Subscription | Cancels the subscription — see [Suspending & Cancelling](../subscriptions/managing.md) |

---

## Renew / Change Plan Dialog

Click **Renew / Change Plan** to open the renewal dialog.

*Screenshot: Renew/Change Plan dialog — add image here*

### Fields

| Field | Description |
|---|---|
| Plan | Dropdown of all active plans. Change this to switch the subscriber to a different plan |
| Start Date | When the new subscription period begins (defaults to today or the current expiry date) |
| End Date | Auto-calculated based on the selected plan's duration, but can be overridden |
| Payment Method | How the subscriber paid for this renewal |
| Amount | The amount paid |
| Reference / Receipt # | Payment reference (M-Pesa transaction ID, bank ref, etc.) |

### Payment Methods

| Method | Notes |
|---|---|
| No Payment (extend only) | Records the renewal without a payment transaction — use for courtesy extensions |
| Manual / Cash | Records a cash payment with a reference number |
| Bank Transfer | Records a bank payment with a reference number |
| M-Pesa (manual ref) | Records an M-Pesa payment using a transaction ID you enter manually |
| M-Pesa STK Push | Triggers a real-time payment request on the subscriber's phone — see [STK Push](../payments/stk-push.md) |

!!! tip "Changing Plans"
    To change a subscriber to a different plan, simply select the new plan from the **Plan** dropdown in the renewal dialog. The end date auto-adjusts to match the new plan's duration. You can still record a payment in the same step.

---

## Quick Extend

Click **Quick Extend** to add days to the current subscription without going through the full renewal flow.

Enter the number of days and confirm. No payment is required — this is useful for:

- Courtesy extensions for service outages
- Correcting subscription end dates
- Giving a subscriber a trial extension

!!! note
    Quick Extend does not record a payment transaction. If a payment was made, use **Renew / Change Plan** instead so the payment is properly recorded in billing history.
