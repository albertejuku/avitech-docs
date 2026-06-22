# IP Pools

IP pools define the IP address ranges available for Static IP subscribers. Each pool is linked to a network device, and the system assigns IPs from these pools when creating subscribers.

## Viewing IP Pools

Go to **Network → IP Pools** in the sidebar.

*Screenshot: IP Pools list — add image here*

The list shows each pool with its range, gateway, assigned device, and usage (how many IPs are taken vs available).

## Creating an IP Pool

1. Click **Add IP Pool**
2. Fill in the fields:

| Field | Description |
|---|---|
| Pool Name | A descriptive name (e.g. "Static IPs — Kileleshwa") |
| Network Device | The router or NAS that manages this pool |
| Subnet | The subnet in CIDR notation (e.g. `192.168.100.0/24`) |
| Gateway | The gateway IP for this subnet |
| Start IP | First assignable IP in the range |
| End IP | Last assignable IP in the range |
| DNS Servers | Primary and secondary DNS (optional) |

3. Click **Save**

## How IP Assignment Works

When you create a Static IP subscriber and select a device, the system:

1. Looks up the IP pool linked to that device
2. Assigns the next available IP from the pool
3. Marks the IP as **in use** in the pool
4. Pushes the IP assignment to the router

When a subscriber is terminated or moved to a different service type, the IP is released back to the pool.

## Editing and Deleting

- **Edit** — you can expand or shrink a pool's range if there are unused IPs at either end. You cannot change the subnet of a pool with active assignments.
- **Delete** — only possible if no IPs in the pool are currently assigned to subscribers.

!!! warning
    The subnet, gateway, and IP range must all be consistent. Entering an incorrect gateway will prevent Static IP subscribers from reaching the internet.
