# Speed Profiles

Speed profiles define the bandwidth tiers you offer. Each profile sets a download and upload speed (in Mbps). Service plans reference a speed profile to enforce rate limits on subscriber connections.

## Viewing Speed Profiles

Go to **Services → Speed Profiles** in the sidebar.

*Screenshot: Speed profiles list — add image here*

The list shows all configured profiles with their download and upload speeds.

## Creating a Speed Profile

1. Click **Add Speed Profile**
2. Fill in the fields:

| Field | Description |
|---|---|
| Profile Name | Display name (e.g. "10 Mbps Basic", "50 Mbps Premium") |
| Download Speed (Mbps) | Maximum download bandwidth |
| Upload Speed (Mbps) | Maximum upload bandwidth |

3. Click **Save**

!!! tip
    Create all your speed tiers before creating plans — plans require a speed profile to be selected.

## Editing a Speed Profile

Click the **Edit** action on any profile. Changing a speed profile's values affects all plans that reference it, which in turn affects all subscribers on those plans at their next RADIUS session update.

## Deleting a Speed Profile

A speed profile can only be deleted if no plans are currently using it. If plans reference the profile, reassign those plans to a different profile first.
