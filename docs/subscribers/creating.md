# Adding a Subscriber

Click **Add Subscriber** on the subscriber list to open the creation form.

*Screenshot: Add Subscriber form — add image here*

## The Form

Fill in the subscriber's details across four sections:

1. **Personal Information** — name, phone number, email
2. **Account Configuration** — subscriber type (Residential, Business, Corporate), zone, and service type (PPPoE, Static IP, or Hotspot)
3. **Plan & Subscription** — choose the service plan and billing cycle
4. **Activation Mode** — decide what happens after creation

## Activation Options

| Option | What happens |
|---|---|
| Activate Immediately | Subscriber gets internet access right away |
| Create as Suspended | Account exists but has no internet access until reactivated |
| Save as Draft | Account saved but not provisioned yet |

!!! note
    For PPPoE subscribers, RADIUS credentials are only pushed to the server when the account is activated — not on Draft. Activating immediately or reactivating later will provision the credentials.

## After Creation

You are taken to the subscriber's detail page where you can confirm the account number, verify credentials, and record a payment if needed.
