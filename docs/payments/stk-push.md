# M-Pesa STK Push

STK Push (Sim Toolkit Push) lets you trigger a real-time M-Pesa payment prompt directly on a subscriber's phone. The subscriber sees a PIN prompt on their screen and completes the payment without needing to initiate it themselves.

## When to Use STK Push

- When a subscriber is at your office or on the phone and wants to pay immediately
- During renewal calls — the agent triggers the push while the subscriber is on the line
- Faster than asking the subscriber to send money manually and then entering a reference

## How to Initiate an STK Push

1. On the **Payments** page, click **STK Push**
2. Search for and select the subscriber (auto-fills their phone number)
3. Verify or override the phone number if needed
4. Enter the amount in KES
5. Click **Send Payment Request**

*Screenshot: STK Push dialog — add image here*

### Phone Number Format

The phone number must be in one of these formats:

| Format | Example |
|---|---|
| Starting with 0 | `0712345678` |
| Starting with 254 | `254712345678` |

The system will auto-fill the subscriber's registered phone. You can override it if, for example, the subscriber wants to pay from a different number.

## What Happens Next

After sending the request:

1. The subscriber's phone displays an M-Pesa PIN prompt
2. The dialog shows a **spinner** with the message: *"Waiting for customer to complete payment on their phone"*
3. The system polls for confirmation **every 8 seconds** for up to **96 seconds** (12 attempts)
4. The system also listens on a WebSocket for instant payment events

*Screenshot: STK Push waiting state — add image here*

### Possible Outcomes

| Outcome | What You See |
|---|---|
| Payment confirmed | Green checkmark, success message, payment recorded automatically |
| Subscriber cancels | Error message — customer cancelled on their phone |
| Timeout (96 seconds) | Warning message — no response received |
| Payment failed | Error message with reason |

### Stop Waiting

If the subscriber needs more time or you want to cancel the polling, click **Stop Waiting**. This does not cancel the M-Pesa transaction — it only stops the portal from waiting. If the subscriber completes the payment after you stop waiting, it will appear as an **Unredeemed Payment** that you can manually link. See [Unmatched Payments](unmatched.md).

## After a Successful STK Push

A payment record is created automatically and linked to the subscriber. 

!!! note
    Like manual payment recording, a successful STK push records the payment but does **not** automatically extend the subscription. To renew the subscription at the same time, use the **Renew / Change Plan** dialog on the Subscription Tab and select **M-Pesa STK Push** as the payment method — this combines the push and the renewal in one flow.

## Troubleshooting STK Push

| Issue | Likely Cause | Action |
|---|---|---|
| Subscriber did not receive prompt | Phone may be off or out of network | Ask subscriber to check connectivity, retry |
| "Number not registered for M-Pesa" | Wrong phone number | Verify and correct the number |
| Timeout with no response | Subscriber did not act in time | Ask subscriber if they received the prompt, retry |
| Payment completed but not showing | WebSocket delay | Click Refresh on the Payments page — it should appear |
