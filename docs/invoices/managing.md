# Managing Invoices

## Actions Available per Invoice

| Action | Available When | Description |
|---|---|---|
| View / Print | Always | Opens the printable invoice detail page |
| Mark as Paid | Status = Issued or Overdue | Records payment and closes the invoice |
| Void | Status = Issued or Overdue | Cancels the invoice permanently |

---

## Viewing and Printing an Invoice

Click the **View / Print** button on any invoice row. This opens a full invoice detail page formatted for printing, showing:

- Invoice number and dates
- Subscriber name, phone, and address
- Plan / service description
- Amount due
- Payment terms and due date
- Your company branding (if configured)

Use your browser's **Print** function (`Ctrl+P` / `Cmd+P`) to print or save as PDF.

*Screenshot: Invoice print view — add image here*

---

## Marking an Invoice as Paid

When a subscriber pays an outstanding invoice:

1. Find the invoice on the Invoices page
2. Click **Mark as Paid**
3. Optionally enter a **Payment Reference** (M-Pesa transaction ID, bank reference, etc.)
4. Click **Confirm Paid**

*Screenshot: Mark as Paid dialog — add image here*

The invoice status changes to **Paid** and the paid date and reference are recorded.

!!! note
    Marking an invoice as paid records the payment against the invoice. It does **not** automatically extend the subscriber's subscription. If a subscription renewal is involved, also use **Renew / Change Plan** on the subscriber's Subscription Tab.

---

## Voiding an Invoice

Voiding cancels an invoice that was created in error or is no longer applicable.

1. Click **Void** on the invoice row
2. Confirm the action in the dialog

!!! danger "Void is Permanent"
    A voided invoice cannot be reinstated. If you need to re-bill the subscriber, create a new invoice. Only void invoices that were created in error or where the charge is being waived.

---

## Invoice Aging & Overdue Status

Invoices automatically transition from **Issued** to **Overdue** once their due date passes (if a due date was set). Overdue invoices appear in red in the status column and will show in filtered overdue reports.

Use the **Status: Overdue** filter to quickly see all unpaid invoices that are past due for follow-up.

---

## Best Practices

- Always enter a payment reference when marking invoices as paid — it links the invoice to the actual transaction for audit purposes
- Use the date filters regularly to identify invoices that are aging without payment
- For business subscribers, set a due date (e.g. 7 or 14 days from issue) to give them a clear payment deadline
- Void invoices promptly when a charge is waived or an error is found — do not leave erroneous invoices in Issued status
