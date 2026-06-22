# Troubleshooting

Common billing issues and how to resolve them from the admin portal.

## Payments

### Payment not appearing

1. Click **Refresh** on the Payments page
2. Check the **Unredeemed** tab — the payment may have arrived but not been matched to a subscriber
3. Ask the subscriber for their M-Pesa confirmation message and verify the transaction ID
4. If the payment is still missing after 10 minutes, check with your payment provider

### STK Push not reaching subscriber

| Symptom | Likely cause | Fix |
|---|---|---|
| No prompt on phone | Wrong phone number | Verify the subscriber's phone number in their profile and retry |
| "Not registered for M-Pesa" | Number not on M-Pesa | Ask subscriber for their M-Pesa registered number |
| Timeout (96 seconds) | Subscriber did not act | Retry or ask subscriber to send manually and record as manual payment |

### Wrong amount recorded

Find the payment on the Payments page. You cannot edit a payment amount directly — void the incorrect payment (if your role allows) and record a new one with the correct amount.

### Duplicate payment

If a subscriber paid twice for the same period, the extra amount can be treated as account credit. Record the second payment and inform the subscriber — the credit will offset their next renewal.

---

## Subscriptions

### Subscription not extending after payment

Recording a payment on the Payments page does **not** extend the subscription. Use **Renew / Change Plan** on the subscriber's Subscription Tab to both record payment and extend the end date in one step.

### Subscriber still suspended after renewal

1. Go to the subscriber's detail page
2. On the Subscription Tab, click **Reactivate**
3. If reactivation fails, click **Force Redial (CoA)** to disconnect and re-authenticate

### Expiry date is wrong

Use **Quick Extend** on the Subscription Tab to adjust the end date. Enter the number of days to add or correct. No payment record is created for a quick extend.

### Grace period ended, subscriber auto-suspended

The subscriber can still be renewed. Use **Renew / Change Plan** — recording a payment and extending the subscription will automatically reactivate them.

---

## Subscriber Accounts

### Subscriber cannot connect (PPPoE)

1. Check the subscriber's **Online Status** on the list — is it Offline or No Internet?
2. Verify RADIUS credentials on the subscriber detail page
3. Click **Force Redial (CoA)** to kick the subscriber's session
4. Click **Refresh Status** to check live RADIUS state
5. If the subscriber changed their router, use **Reset MAC Binding**

### Subscriber cannot connect (Static IP)

1. Verify the static IP is assigned and shows as **(fixed)** on the detail page
2. Click **Re-provision** to push the IP assignment to the router
3. Check that the router/NAS device is online under Network → Devices

### Wrong zone or device assignment

Edit the subscriber and update the Zone or Router/NAS field. For PPPoE subscribers, the RADIUS credentials will be reprovisioned on the new device automatically.

### Account status stuck

Click **Refresh Status** on the subscriber detail page to force a live status check against the RADIUS server. If status is still incorrect, check the RADIUS server logs.

---

## Plans

### Cannot delete a plan

Plans with active subscribers cannot be deleted. Either:
- Move subscribers to a different plan via **Renew / Change Plan**, or
- **Archive** the plan instead (preserves historical records)

### Plan changes not affecting existing subscribers

Plan edits (price, speed, duration) only apply to NEW subscriptions and renewals. Existing active subscriptions keep their original terms until the current period ends.

---

## Invoices

### Invoice stuck as Issued

An invoice stays **Issued** until manually marked as paid. If payment was received, find the invoice and click **Mark as Paid**.

### Invoice marked as paid by mistake

You cannot undo a paid status. Create a new invoice if the charge still applies, or issue a credit note.

### Wrong amount on invoice

Void the incorrect invoice and create a new one with the correct amount. Voiding is permanent — double-check before confirming.

---

## Login & Access

### Cannot log in

1. Verify the username/email and password
2. Check if the account is active (not disabled)
3. Use **Forgot Password** to trigger a reset email
4. If the user is locked out, an admin can reset their password from Settings → Users

### Section missing from sidebar

Access to portal sections is controlled by user roles. If a section is not visible, contact your system administrator to adjust your role permissions.

### Session keeps expiring

Sessions expire after a period of inactivity for security. Log in again. If it happens frequently, check that your browser is not clearing cookies automatically.

