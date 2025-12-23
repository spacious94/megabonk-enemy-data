# Campfire

> Stand still to create a campfire that heals you

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 36 |
| **Internal Name** | Campfire |
| **Class Name** | ItemCampfire |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### Passive - CampfireHealing

Stand still to create a campfire that heals you

**Healing:**
- baseValue: `1100`
- scaling: `linear`
- formula: `amount * 1100 HP/minute`

## Internal Fields

| Field | Value |
|-------|-------|
| healthRegenPerMinutePerAmount | 1100.0 |
| setupTime | 0.6 |
| distThreshold | 1.75 |

## Implementation Details

- **Constructor RVA:** `0x454CB0`
- **Createcamp RVA:** `0x4547A0`
- **Removecamp RVA:** `0x454B30`
- **Tick RVA:** `0x454BC0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
