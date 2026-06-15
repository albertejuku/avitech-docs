# Plans

Service plans define what subscribers get — speed, data limits, validity, and price. Every subscriber must be on a plan, and plans drive your billing amounts and subscription durations.

## Plan Types

| Type | Description |
|---|---|
| Fixed | Long-term plans for home and business subscribers. Billed on a recurring cycle (monthly, quarterly, etc.) |
| Hotspot | Time or data-limited plans for WiFi / captive portal customers. Can be one-time or recurring |

## Plan Lifecycle

Plans move through a defined set of states:

```
INACTIVE → ACTIVE → (INACTIVE) → ARCHIVED → (deleted)
```

| Status | Meaning |
|---|---|
| Active | Available for new subscriptions |
| Inactive | Existing subscriptions continue but no new subscribers can be added |
| Archived | Hidden from normal views, fully retired |

## Navigation

- [Managing Plans](managing.md) — create, edit, and configure plans
- [Plan Lifecycle](lifecycle.md) — activate, deactivate, archive, and delete
- [Fair Usage Policy (FUP)](fup.md) — configure speed throttling after a data threshold
