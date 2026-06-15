# Payments

The Payments page is where all money coming into the system is recorded, tracked, and reconciled. Every transaction — whether from M-Pesa, cash, or bank transfer — appears here.

*Screenshot: Payments page overview — add image here*

## KPI Cards

Three summary cards appear at the top of the page:

| Card | Description |
|---|---|
| Today's Revenue | Total amount received today (KES) with a count of transactions |
| This Month | Total revenue collected in the current calendar month |
| Unredeemed Payments | Payments received that have not yet been linked to a subscriber — shown in red if count > 0 |

!!! warning "Unredeemed Payments"
    Unredeemed payments represent money received but not yet applied to a subscriber account. Always action these promptly so subscribers' subscriptions are updated correctly. See [Unmatched Payments](unmatched.md).

## Tabs

| Tab | Contents |
|---|---|
| All Payments | Every payment in the system |
| Unredeemed | Payments not yet linked to a subscriber (with count badge) |

## Filters

| Filter | Options |
|---|---|
| Search | Subscriber name, phone number, or payment reference |
| Provider | All, M-Pesa, Cash, Bank Transfer |
| Status | All, Completed, Pending, Failed |
| Date From | Start of date range |
| Date To | End of date range |
| Clear Filters | Resets all active filters |

## Table Columns

| Column | Description |
|---|---|
| Date | Date and time the payment was recorded |
| Provider | Payment channel with colored chip (M-Pesa = green, Cash = amber, Bank = blue) |
| Reference | Transaction ID or receipt number in monospace |
| Phone | Phone number associated with the payment |
| Account Ref | The subscriber account reference |
| Amount | Amount in KES in bold monospace |
| Method | Specific payment method |
| Status | Completed, Pending, Failed, or UNMATCHED (for unredeemed payments) |
| Actions | View subscriber (if matched) or Redeem button (if unmatched) |

## Top Bar Actions

| Button | Description |
|---|---|
| STK Push | Trigger an M-Pesa payment request to a subscriber's phone |
| Record Payment | Manually enter a payment received via cash, bank, or M-Pesa |
| Refresh | Reload the payment list |

## Navigation

- [Recording a Manual Payment](manual.md)
- [M-Pesa STK Push](stk-push.md)
- [Unmatched Payments](unmatched.md)
