# Network Devices

Network devices are the physical hardware that authenticate subscribers and route their traffic — routers, OLTs, NAS devices, and switches.

## Viewing Devices

Go to **Network → Devices** in the sidebar.

*Screenshot: Devices list — add image here*

The list shows all registered devices with their type, IP address, zone, and online status.

## Adding a Device

1. Click **Add Device**
2. Fill in the fields:

| Field | Description |
|---|---|
| Device Name | A descriptive name (e.g. "MikroTik Kileleshwa", "ZTE C320 OLT") |
| Device Type | Router, OLT, NAS, or Switch |
| IP Address | Management IP address of the device |
| Zone | The zone this device serves |
| RADIUS Secret | Shared secret for RADIUS authentication (PPPoE devices) |
| API Port | Management API port (if applicable) |

3. Click **Save**

## Device Types

| Type | Used for |
|---|---|
| **Router** | MikroTik or similar — handles PPPoE, Static IP, Hotspot |
| **OLT** | Optical Line Terminal — serves fiber subscribers via ONUs |
| **NAS** | Network Access Server — RADIUS authentication and accounting |
| **Switch** | Layer 2/3 managed switches |

## Device Status

The device list shows live online/offline status. If a device shows offline:

1. Verify the device is powered on and reachable at its management IP
2. Check that API credentials are correct
3. Check the device logs for errors

!!! warning "RADIUS Secret"
    The RADIUS secret must match exactly what is configured on the device. If they don't match, PPPoE authentication will fail for all subscribers on that device.
