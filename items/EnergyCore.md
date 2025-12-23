# Energy Core

> Spawns orbiting energy orbs that fire at enemies

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 44 |
| **Internal Name** | EnergyCore |
| **Class Name** | ItemEnergyCore |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **Price** | 11 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### Passive - OrbitingOrbs

Spawns orbiting energy orbs that fire at enemies

**Orbs:**
- base: `4`
- perStack: `2`
- formula: `4 + (amount - 1) * 2`

**Cooldown:**
- base: `4.0`
- perOrb: `0.2`
- formula: `4.0 - numOrbs * 0.2`

## Internal Fields

| Field | Value |
|-------|-------|
| orbsPerAmount | 2 |
| numOrbs | 4 |
| range | 70.0 |
| cooldown | 4.0 |
| cooldownPerOrb | 0.2 |

## Implementation Details

- **Constructor RVA:** `0x45FBE0`
- **Fireorb RVA:** `0x45F690`
- **Getdamage RVA:** `0x45FA00`
- **Tick RVA:** `0x45FA50`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
