# Subscriber Details

Click **View Details** on any subscriber to open their full detail page. This page is the single source of truth for everything about a subscriber's account.

*Screenshot: subscriber detail page header — add image here*

## Header / Profile Strip

The top of the page shows:

- **Avatar** — colored circle indicating account status (green = Active, amber = Suspended, gray = Terminated)
- **Full Name** — the subscriber's name
- **Status chip** — current billing status
- **Type chip** — Residential / Business / Corporate
- **Credit Balance** — any account credit available (used to offset future invoices or renewals)
- **Account Number** — unique account identifier in monospace format

### Header Action Buttons

| Button | Description |
|---|---|
| Edit | Opens the edit dialog to update subscriber information |
| Suspend | Removes internet access and sets status to SUSPENDED |
| Reactivate | Restores internet access and sets status to ACTIVE (appears when Suspended) |
| Terminate | Permanently closes the account — **cannot be undone** |
| Refresh Status | Forces a live status check against the RADIUS server |

!!! warning "Terminating an Account"
    Termination is permanent. The subscriber's RADIUS credentials are removed and the account cannot be reactivated. Use **Suspend** if you only want to temporarily remove access.

## Tabs

The detail page has six tabs:

| Tab | Contents |
|---|---|
| [Overview](#overview-tab) | Personal info, account details, connectivity |
| [Subscription](#subscription-tab-summary) | Current plan, expiry, renewal actions |
| [Payments](#payments-tab-summary) | Full payment history |
| Traffic | Real-time bandwidth graph |
| Usage | Historical data usage per period |
| Queue | Router simple queue / QoS info |

---

## Overview Tab

*Screenshot: Overview tab — add image here*

### Personal Information

| Field | Description |
|---|---|
| Username | RADIUS or hotspot login username |
| Phone | Contact phone number |
| Email | Contact email address |
| Address | Physical address (if entered) |

### Account

| Field | Description |
|---|---|
| Account Number | Unique billing reference number |
| Zone | The network zone this subscriber is assigned to |
| Type | Residential, Business, or Corporate |
| Credit Balance | Available account credit (shown in green if positive) |

### Connectivity

| Field | Description |
|---|---|
| Connection Type | Static IP, PPPoE, or PPPoE + Hotspot |
| NAS / Router | The network device managing this subscriber's connection |
| Assigned IP | The subscriber's IP address. Marked as **(fixed)** for Static subscribers. |

---

## Subscription Tab (Summary) {#subscription-tab-summary}

See the full [Subscription Tab](subscription-tab.md) documentation for details on renewing, changing plans, grace period tracking, and quick actions.

---

## Payments Tab (Summary) {#payments-tab-summary}

See the full [Payments Tab](payments-tab.md) documentation for the per-subscriber payment history.
