# Setup Guide

Follow these steps in order when setting up CoreSync for the first time. Each step links to the page that shows you exactly how to do it.

---

## 1. Speed Profiles

Speed profiles define your internet speed tiers — for example 10Mbps, 20Mbps, or 50Mbps. Every service plan references a speed profile to set the subscriber's bandwidth limits.

[How to create speed profiles →](../network/speed-profiles.md)

---

## 2. Zones

Zones are your coverage areas — neighborhoods, buildings, or regions. Every subscriber belongs to a zone, and zones determine which network device serves them.

[How to set up zones →](../network/zones.md)

---

## 3. Network Devices

Add your routers, OLTs, and NAS devices. These are the physical hardware that authenticate subscribers and route their traffic. PPPoE subscribers need a RADIUS-enabled device. Static IP subscribers need a device that manages IP pools.

[How to add network devices →](../network/devices.md)

---

## 4. IP Pools

If you offer Static IP services, define your IP address ranges here. Each pool is linked to a network device, and the system assigns IPs from these pools when creating Static IP subscribers.

[How to configure IP pools →](../network/ip-pools.md)

---

## 5. Service Plans

Plans define what subscribers get — speed, data limit, billing cycle, and price. Create your plans after speed profiles are in place so you can link them.

[How to create and manage plans →](../plans/managing.md)

- **Fixed plans** — recurring billing (Daily, Weekly, Monthly, Quarterly, Yearly)
- **Hotspot plans** — time or data-limited, with optional trial mode

!!! tip "Plan Codes"
    Use short, descriptive codes like `HOME-20M` or `BIZ-50M`. They must be unique.

---

## 6. Add Subscribers

Once zones, devices, and plans are ready, add your subscribers.

- [Adding subscribers one at a time →](../subscribers/creating.md)
- [Importing subscribers in bulk via CSV →](../subscribers/bulk-operations.md)

Imported subscribers start in **Draft** status. Activate them individually or use Bulk Extend to activate in batch.

---

## 7. Final Checks

- [ ] Every zone has at least one device assigned
- [ ] Every plan has a speed profile linked
- [ ] IP pools are configured (if using Static IP)
- [ ] Test a few subscribers — can they connect and pass traffic?
- [ ] Record a test payment — does the invoice flow work?

If anything fails, see [Troubleshooting](troubleshooting.md).
