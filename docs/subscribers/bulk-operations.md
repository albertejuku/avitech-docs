# Bulk Operations

The billing portal supports several bulk operations that let you take action on large groups of subscribers at once — without having to open each account individually.

## Bulk Extend Subscriptions

Extend the subscription end date for multiple subscribers in one operation. This is useful for:

- Giving an extension to an entire zone after a service outage
- Providing a courtesy extension to all subscribers on a specific router during maintenance
- Handling end-of-month renewals in bulk

### How to Bulk Extend

1. On the **Subscriber List**, click the **Actions** dropdown (top right)
2. Select **Extend Subscriptions**
3. Set your audience filters:

| Filter | Description |
|---|---|
| Status | Active, Suspended, or All |
| Zone | Limit to subscribers in a specific zone |
| Router / NAS | Limit to subscribers on a specific device |
| Service Type | PPPoE, Hotspot, Static, or All |

4. Click **Preview** — the dialog shows a sample of affected subscribers and the total count
5. Enter the number of **days to extend**
6. Click **Extend**

*Screenshot: Bulk Extend dialog — add image here*

!!! warning "Suspended Subscribers"
    If you include Suspended subscribers in the extension, they will be **automatically reactivated** and their RADIUS expiration will be updated. Only include Suspended subscribers in a bulk extend if you intend to restore their access.

!!! tip
    Always click **Preview** before confirming so you can verify the correct group is selected.

---

## Push Static to Router

For ISPs using Static IP service, this operation pushes all static IP assignments to the relevant network devices in bulk.

### When to Use This

- After a router is rebooted and loses its ARP/IP binding table
- After making changes to multiple static IP assignments
- During initial setup of a new router with existing static subscribers

### How to Run

1. On the **Subscriber List**, click the **Actions** dropdown
2. Select **Push Static to Router**
3. Confirm the operation

The system will push all active static IP bindings to their respective routers via the API.

---

## CSV Import

Import multiple subscribers at once from a spreadsheet.

### How to Import

1. Click the **Import** button on the Subscriber List
2. Download the CSV template (if provided) to ensure the correct column format
3. Fill in your subscriber data
4. Upload the CSV file
5. The portal validates each row and reports any errors before importing

### Required CSV Columns

| Column | Notes |
|---|---|
| First Name | Required |
| Last Name | Required |
| Phone | Required |
| Email | Optional |
| Zone | Must match an existing zone name |
| Service Type | PPPOE, HOTSPOT, or STATIC |
| Plan Code | Must match an existing plan code |

!!! note
    Imported subscribers are created in **Draft** status by default. Activate them individually or use Bulk Extend after import to activate in batch.

---

## CSV Export

Export the current subscriber list (with all active filters applied) as a CSV file for use in spreadsheets, reports, or external systems.

1. Apply any filters you need (zone, status, service type, etc.)
2. Click **Export CSV**
3. The file downloads automatically

The export includes all visible columns: name, phone, email, username, status, zone, service type, plan, expiry date, and MTD usage.
