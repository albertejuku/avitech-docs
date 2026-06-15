# Plan Lifecycle

Plans move through a defined set of statuses. Understanding the lifecycle helps you retire old plans cleanly without breaking existing subscribers.

## Status Overview

```
         ┌─────────────┐
         │   INACTIVE  │ ◄──────────────┐
         └──────┬──────┘                │
                │ Activate              │ Deactivate
                ▼                       │
         ┌─────────────┐                │
         │   ACTIVE    │ ───────────────┘
         └──────┬──────┘
                │ Archive
                ▼
         ┌─────────────┐
         │   ARCHIVED  │
         └──────┬──────┘
                │ Delete (permanent)
                ▼
              (gone)
```

## Status Descriptions

| Status | New Subscribers | Existing Subscriptions | Visible in list |
|---|---|---|---|
| Active | Yes | Continue normally | Yes |
| Inactive | No | Continue until expiry | Yes |
| Archived | No | Continue until expiry | Only with filter |

## Actions by Current Status

### Active Plans

| Action | Result |
|---|---|
| Deactivate | Moves to Inactive. Existing subscribers keep their plan until renewal |
| Archive | Moves to Archived. No new subscriptions possible |
| Delete | Only if zero subscribers. Permanently removes the plan |

### Inactive Plans

| Action | Result |
|---|---|
| Activate | Moves back to Active. New subscriptions can be added again |
| Archive | Moves to Archived |
| Delete | Only if zero subscribers |

### Archived Plans

| Action | Result |
|---|---|
| Restore | Moves back to Inactive |
| Delete | Permanently deletes. Only allowed if no subscribers |

---

## Best Practices

**Retiring an old plan:**
1. Deactivate the plan — stops new signups but existing subscribers are unaffected
2. Migrate existing subscribers to the new plan via **Renew / Change Plan** on each subscriber
3. Once subscriber count reaches zero, Archive the plan
4. After archiving, you can delete if you want to clean up the list

**Replacing a plan with a new price:**
- Do not edit the price on the existing plan if it has many active subscribers
- Create a new plan with the new price
- Deactivate the old plan
- New subscribers go on the new plan; existing subscribers roll over at renewal

!!! tip
    Use the **Status: Archived** filter to view retired plans if you need to reference historical plan configurations.
