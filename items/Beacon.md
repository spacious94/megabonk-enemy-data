# Beacon

> Spawns extra shrines and provides healing aura

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 78 |
| **Internal Name** | Beacon |
| **Class Name** | ItemBeacon |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### Passive - ShrineSpawnAndHealing

Spawns extra shrines and provides healing aura

**Extrashrines:**
- base: `extraShrinesPerAmount`
- formula: `amount * extraShrinesPerAmount`

**Healingradius:**
- base: `healingRadiusPerAmount`
- formula: `amount * healingRadiusPerAmount`

## Internal Fields

| Field | Value |
|-------|-------|
| extraShrinesPerAmount | extracted from constructor |
| healingRadiusPerAmount | extracted from constructor |
| healingFractionPerInterval | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x439350`
- **Gethealingperinterval RVA:** `0x439280`
- **Getradius RVA:** `0x439330`
- **Getextrashrines RVA:** `0x439270`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
