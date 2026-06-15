# Fair Usage Policy (FUP)

Fair Usage Policy (FUP) allows you to automatically throttle a subscriber's speed once they have consumed a defined amount of data within their billing cycle. This lets you offer "unlimited" plans while still protecting network quality for all users.

## How FUP Works

1. Subscriber uses data normally at their plan's full speed
2. When they reach the **FUP Threshold**, the RADIUS server automatically applies reduced speeds
3. The throttled speeds remain in effect until the next billing cycle resets their usage

```
Day 1                      FUP Threshold                    End of Cycle
|--------------------------|-------------------------------|
  Full speed (e.g. 20Mbps)   Throttled speed (e.g. 2Mbps)
```

## Configuring FUP on a Plan

FUP is configured in the **Fair Usage Policy** section of the plan creation or edit dialog.

| Field | Description |
|---|---|
| Enable FUP | Toggle to activate FUP for this plan |
| FUP Threshold (MB) | The data amount (in megabytes) before throttling starts |
| Throttled Download Speed (Mbps) | The reduced download speed applied after the threshold |
| Throttled Upload Speed (Mbps) | The reduced upload speed applied after the threshold |

### Example Configuration

| Setting | Value |
|---|---|
| Plan speed | 20 Mbps download / 5 Mbps upload |
| FUP Threshold | 51,200 MB (50 GB) |
| Throttled Download | 2 Mbps |
| Throttled Upload | 1 Mbps |

In this example, the subscriber gets full 20Mbps until they consume 50GB. After that, they are throttled to 2Mbps for the rest of the billing cycle.

## FUP vs Data Limit

| Feature | FUP | Data Limit |
|---|---|---|
| What happens at threshold | Speed is reduced | Internet access is cut off |
| Subscriber still online? | Yes, at reduced speed | No |
| Suitable for | "Unlimited" but fair use plans | Strict data cap plans |

You can use both on the same plan: set a data limit for hard cutoff and FUP for a soft throttle before that limit.

!!! note
    FUP enforcement requires a compatible RADIUS server configuration. Confirm with your network administrator that CoA (Change of Authorization) is enabled on your NAS devices for FUP to take effect dynamically.
