# Unmatched Payments

Unmatched (or "unredeemed") payments are transactions that arrived in the system — typically via M-Pesa — but could not be automatically linked to a subscriber account.

## Why Payments Go Unmatched

- The subscriber paid from a phone number not registered in the system
- The subscriber paid the wrong amount or used an unrecognized reference
- An STK push timed out but the subscriber completed payment anyway
- A new subscriber paid before their account was created

## Finding Unmatched Payments

Two ways to find them:

1. **KPI Card** — The **Unredeemed Payments** card at the top of the Payments page shows the count. It turns red when count > 0
2. **Unredeemed Tab** — Click the **Unredeemed** tab on the Payments page (also shows a count badge)

*Screenshot: Unredeemed tab — add image here*

## How to Redeem (Match) a Payment

1. Go to the **Unredeemed** tab on the Payments page
2. Find the payment — note the phone number and amount to identify the subscriber
3. Click the **Redeem** button on the payment row
4. In the dialog, search for and select the subscriber to link the payment to
5. Click **Confirm**

*Screenshot: Redeem payment dialog — add image here*

### The Redeem Dialog Shows

| Field | Description |
|---|---|
| Reference | The M-Pesa or payment reference |
| Amount | The amount received |
| Phone | The phone number the payment came from |
| Subscriber | Search and select the subscriber to link this payment to |

## After Redemption

- The payment is linked to the selected subscriber
- It moves from the Unredeemed tab to the All Payments tab
- It appears in the subscriber's Payments tab history
- Status changes from **UNMATCHED** to **Completed**

!!! note
    Redeeming a payment links it to the subscriber but does **not** automatically extend their subscription. After redeeming, go to the subscriber's Subscription Tab and use **Renew / Change Plan** to update their subscription end date.

## Preventing Unmatched Payments

- Ensure subscribers have their correct phone number registered in the system
- When using STK Push, always confirm the correct phone number before sending
- Train subscribers to use their account number as the M-Pesa reference when sending manually
- Act on unmatched payments daily — the longer they sit, the harder it is to identify who paid
