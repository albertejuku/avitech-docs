# Renewing & Changing Plans

## How to Renew a Subscription

Renewals can be initiated from two places:

1. **Subscriptions page** → click the actions menu ( ⋮ ) → **Renew / Change Plan**
2. **Subscriber Detail page** → Subscription tab → **Renew / Change Plan** button

Both open the same dialog.

*Screenshot: Renew / Change Plan dialog — add image here*

## Renewal Dialog Fields

### Subscriber & Plan

| Field | Description |
|---|---|
| Subscriber | Pre-filled. Shows the subscriber's name |
| Plan | The plan to renew on. Change this dropdown to switch to a different plan |

### Dates

| Field | Description |
|---|---|
| Start Date | When the new period begins. Defaults to today or the current expiry date, whichever is later |
| End Date | Auto-calculated from the plan's billing cycle. Can be manually overridden if needed |

!!! tip "Early Renewal"
    If a subscriber pays before their current subscription expires, set **Start Date** to their current **Expiry Date** so their new period picks up where the old one left off — not from today.

### Payment

| Field | Description |
|---|---|
| Payment Method | Choose how the subscriber paid (see options below) |
| Amount (KES) | The amount received. Defaults to the plan price |
| Reference / Receipt # | Transaction ID or receipt number |

#### Payment Method Options

| Method | When to Use |
|---|---|
| No Payment (extend only) | Courtesy extensions, corrections, or when payment was already recorded separately |
| Cash | Customer paid in cash at your office or to a field agent |
| Bank Transfer | Customer paid via bank transfer — enter the bank reference |
| M-Pesa (manual ref) | Customer paid via M-Pesa — enter the Mpesa transaction ID (e.g. QDJ3LK8PXN) |
| M-Pesa STK Push | Trigger a real-time payment request to the customer's phone — see [STK Push](../payments/stk-push.md) |

---

## Changing a Subscriber's Plan

To move a subscriber to a different plan, open the Renew / Change Plan dialog and select a different plan from the **Plan** dropdown.

The **End Date** will automatically recalculate based on the new plan's billing cycle. You can still record a payment in the same step.

!!! note
    Plan changes take effect immediately. The subscriber's RADIUS session will be updated with the new plan's speed profile and data limits on their next connection (or immediately if CoA is triggered).

---

## Bulk Renewals / Extensions

To extend subscriptions for a group of subscribers at once, use **Bulk Extend** from the Subscriber List. See [Bulk Operations](../subscribers/bulk-operations.md) for details.

---

## What Happens After Renewal

1. The subscription end date is updated in the database
2. The RADIUS server expiry attribute is updated for the subscriber
3. If the subscriber was Suspended, their account is **automatically reactivated** and internet access restored
4. A payment record is created (unless "No Payment" was selected)
5. The subscription status changes to **Active**
