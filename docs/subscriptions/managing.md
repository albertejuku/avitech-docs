# Suspending & Cancelling Subscriptions

## Suspending a Subscription

Suspending removes internet access from a subscriber without closing their account. The subscriber can be reactivated at any time, typically after a payment is made.

### How to Suspend

**From the Subscriptions page:**

1. Find the subscriber in the list
2. Click the actions menu ( ⋮ )
3. Click **Suspend**
4. Confirm the action

**From the Subscriber Detail page:**

Click the **Suspend** button in the header or in the Subscription tab Quick Actions.

### What Happens on Suspension

- Subscriber status changes to **SUSPENDED**
- RADIUS session is terminated (subscriber is disconnected)
- No further internet access until reactivated
- Subscription record remains — expiry date is preserved
- The subscriber still appears in your subscriber list and all their history is intact

!!! note
    Suspension is reversible. Use **Reactivate** at any time to restore access without losing the subscription record or payment history.

---

## Reactivating a Subscription

1. Find the suspended subscriber
2. Click the actions menu ( ⋮ ) → **Reactivate** (Subscriptions page)  
   or click **Reactivate** in the Subscriber Detail page header
3. Confirm

The subscriber's RADIUS credentials are re-provisioned and internet access is restored immediately.

!!! tip
    If the subscriber's subscription has already expired (past end date), reactivating alone will not restore access long-term — use **Renew / Change Plan** to extend their subscription and reactivate in one step.

---

## Cancelling a Subscription

Cancellation ends the subscription permanently. The subscriber account remains but has no active plan.

### How to Cancel

1. From the Subscriptions page, click actions ( ⋮ ) → **Cancel Subscription**
2. Optionally enter a **reason** for the cancellation (for your records)
3. Click **Cancel Subscription** to confirm

*Screenshot: Cancel Subscription dialog — add image here*

!!! warning "Internet Access is Removed Immediately"
    Cancelling a subscription removes RADIUS access immediately, even if the subscriber has paid-up time remaining. Only cancel if the subscriber has explicitly requested to leave or if the account is being closed.

### Cancel vs Suspend vs Terminate

| Action | Access Removed | Account Remains | Can Be Reversed |
|---|---|---|---|
| Suspend | Yes | Yes | Yes — Reactivate |
| Cancel Subscription | Yes | Yes (no plan) | Yes — add new subscription |
| Terminate Account | Yes | No | No |

**Use Suspend** for non-payment or temporary holds.  
**Use Cancel Subscription** when a subscriber is leaving but may return.  
**Use Terminate** only for permanently closing an account.

---

## Automatic Suspension (Grace Period)

Subscriptions that expire without renewal automatically enter a **grace period** (default: 7 days). During the grace period:

- The subscriber retains internet access
- A countdown is shown on their Subscription tab
- At the end of the grace period, the subscriber is **automatically suspended**

The grace period length is configured per plan. Operators can manually renew at any time during or after the grace period to restore access without disruption.
