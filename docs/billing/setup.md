# Setup Guide

Follow this guide in order when setting up CoreSync for a new tenant. Each step links to the detailed page that explains how to do it.

---

## 1. Speed Profiles

Speed profiles define the bandwidth tiers you offer subscribers (e.g. 10Mbps, 20Mbps, 50Mbps). Plans reference speed profiles to set RADIUS rate limits.

Go to **Services → Speed Profiles** in the portal to create your speed tiers before creating plans.

---

## 2. Zones

Zones represent your coverage areas — neighborhoods, buildings, regions, or any grouping that makes sense for your network.

Go to **Network → Zones** to define your zones. Subscribers are assigned to a zone during creation, which determines which router or NAS device serves them.

---

## 3. Network Devices

Register your routers, OLTs, NAS devices, and switches. These are the physical devices that authenticate and route subscriber traffic.

Go to **Network → Devices** to add each device. For PPPoE subscribers, the device must be RADIUS-enabled. For Static IP subscribers, the device manages the IP pool assignments.

---

## 4. IP Pools

If you offer Static IP services, configure your IP address ranges. Each IP pool is linked to a network device.

Go to **Network → IP Pools** to define your ranges. The system will assign IPs from these pools when creating Static IP subscribers.

---

## 5. Service Plans

Plans define what subscribers get — speed, data limits, billing cycle, and price.

See [Managing Plans](../plans/managing.md) for the full guide on creating plans. Key decisions:

- **Fixed plans** — recurring billing (Daily, Weekly, Monthly, Quarterly, Yearly)
- **Hotspot plans** — time or data-limited, with optional trial mode
- Set pricing, speed profiles, data limits, and Fair Usage Policy (FUP) thresholds

!!! tip "Plan Codes"
    Use short, descriptive plan codes (e.g. `HOME-20M`, `BIZ-50M`). They must be unique and will appear throughout the portal.

---

## 6. Import Subscribers

Once your zones, devices, and plans are in place, add your subscribers.

See [Adding a Subscriber](../subscribers/creating.md) for individual creation, or [Bulk Operations](../subscribers/bulk-operations.md) for importing via CSV.

Imported subscribers are created in **Draft** status by default. Activate them individually, or use **Bulk Extend** to activate in batch.

---

## 7. Final Checks

After setup, verify:

- [ ] Each zone has at least one network device assigned
- [ ] Each plan has a speed profile linked
- [ ] IP pools are configured (if using Static IP)
- [ ] A few test subscribers can connect and pass traffic
- [ ] Payments and invoice flows work end-to-end

If any step fails, see the [Troubleshooting](troubleshooting.md) guide.
