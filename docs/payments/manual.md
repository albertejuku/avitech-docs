# Recording a Manual Payment

Use this when a subscriber pays via **cash**, **bank transfer**, or **M-Pesa** and you are entering the payment details manually (rather than triggering an STK push).

## How to Record a Payment

1. On the **Payments** page, click **Record Payment**
2. Fill in the dialog fields
3. Click **Save**

*Screenshot: Record Payment dialog — add image here*

## Fields

| Field | Required | Description |
|---|---|---|
| Subscriber | Yes | Search by name or phone number. Select from the autocomplete dropdown |
| Amount (KES) | Yes | The amount the subscriber paid |
| Provider | Yes | Cash, Bank Transfer, or M-Pesa |
| Reference / Receipt # | Yes | The transaction ID, bank reference, or receipt number |

!!! tip
    For M-Pesa manual payments, the reference is the M-Pesa transaction ID (e.g. `QDJ3LK8PXN`) found on the subscriber's M-Pesa confirmation message. Always ask the subscriber for this before recording the payment.

## What Happens After Saving

1. A payment record is created and linked to the subscriber
2. The payment appears in the subscriber's Payments tab
3. The payment appears on the main Payments page with status **Completed**
4. If the payment was made as part of a renewal, use **Renew / Change Plan** on the subscriber's Subscription tab so that the subscription end date is also extended

!!! note
    Recording a payment here does **not** automatically extend the subscription. To extend the subscription at the same time as recording a payment, use the **Renew / Change Plan** dialog on the [Subscription Tab](../subscribers/subscription-tab.md) — it handles both in one step.

## Difference: Record Payment vs Renew / Change Plan

| Feature | Record Payment | Renew / Change Plan |
|---|---|---|
| Creates a payment record | Yes | Yes |
| Extends subscription end date | No | Yes |
| Updates RADIUS expiry | No | Yes |
| Reactivates if suspended | No | Yes |

Use **Record Payment** when you only need to log a transaction (e.g. a partial payment, a deposit, or a payment that was already applied separately).

Use **Renew / Change Plan** when you want to both record payment and extend the subscription in one action.
