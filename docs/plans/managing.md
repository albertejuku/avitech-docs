# Managing Plans

## The Plans List

Navigate to **Subscribers → Plans** in the sidebar to see all service plans.

*Screenshot: Plans list — add image here*

### Filtering the List

| Filter | Options |
|---|---|
| Search | Filter by plan name, plan code, or description |
| Type | All, Fixed, Hotspot |
| Status | All, Active, Inactive, Archived |

### Table Columns

| Column | Description |
|---|---|
| Plan Name | Display name of the plan |
| Code | Short plan code in monospace (e.g. `HOME-20M`) |
| Type | Fixed (blue chip) or Hotspot (amber chip). Trial badge shown if applicable |
| Speed Profile | The linked speed profile and its download / upload speeds |
| Validity | How long the plan lasts per billing cycle (e.g. "30 days") |
| Price | Plan price in configured currency |
| Subscribers | Number of subscribers currently on this plan (Fixed plans only) |
| Status | Active, Inactive, or Archived |
| Actions | Edit, status changes, delete |

---

## Creating a Plan

Click **Add Plan** (or the + button) to open the plan creation dialog.

*Screenshot: Create Plan dialog — add image here*

### Section 1: Basic Information

| Field | Required | Description |
|---|---|---|
| Plan Name | Yes | The display name shown to staff and on invoices (e.g. "Home 20Mbps Monthly") |
| Plan Code | Yes | Short internal code, auto-uppercased (e.g. `HOME-20M`). Must be unique |
| Description | No | Free-text description of the plan |

### Section 2: Plan Configuration

| Field | Required | Notes |
|---|---|---|
| Plan Type | Yes | **Fixed** or **Hotspot** |
| Speed Profile | No | Links a pre-configured speed profile that sets RADIUS rate limits |

**For Fixed plans:**

| Field | Required | Description |
|---|---|---|
| Billing Cycle | Yes | Daily, Weekly, Monthly, Quarterly, or Yearly |
| Data Limit (MB) | No | Cap total data per cycle. Leave blank for unlimited |

**For Hotspot plans:**

| Field | Required | Description |
|---|---|---|
| Validity Duration | Yes | Number of time units |
| Validity Unit | Yes | Minutes, Hours, Days, Weeks, or Months |
| Data Limit (MB) | No | Cap total data for the validity period |
| Max Devices | No | Maximum simultaneous device connections |
| Trial | No | Check this to make the plan a one-time free trial (one use per device) |

### Section 3: Pricing

| Field | Required | Description |
|---|---|---|
| Price | Yes | The amount charged per billing cycle |
| Currency | Yes | KES, USD, or EUR |

### Section 4: Fair Usage Policy (FUP)

See [Fair Usage Policy](fup.md) for full FUP configuration details.

| Field | Description |
|---|---|
| Enable FUP | Toggle to activate data throttling |
| FUP Threshold (MB) | Data consumed before throttling kicks in |
| Throttled Download (Mbps) | Reduced download speed after threshold |
| Throttled Upload (Mbps) | Reduced upload speed after threshold |

### Section 5: Visibility

| Field | Description |
|---|---|
| Visible in public pricing | Whether this plan appears on your public pricing page |

---

## Editing a Plan

Click the **Edit** action on any plan to open the same dialog pre-filled with existing values.

!!! note
    Editing a plan's price, speed, or duration does **not** retroactively change existing subscriber subscriptions. Only new renewals and new subscriptions will use the updated values. Existing subscriptions continue until their current period ends.

!!! warning
    Changing a plan's **billing cycle** on an active plan with subscribers can cause subscription end dates to be inconsistent on next renewal. Consider creating a new plan and migrating subscribers instead of changing an existing plan's cycle.

---

## Deleting a Plan

Plans can only be permanently deleted if they have **no active subscribers**.

To delete a plan with subscribers, you must first:
1. Move subscribers to a different plan, or
2. Archive the plan instead (see [Plan Lifecycle](lifecycle.md))

The delete confirmation dialog shows the current subscriber count for Fixed plans so you can verify before proceeding.

!!! danger
    Permanent deletion cannot be undone. Archive the plan instead if you want to keep historical records.
