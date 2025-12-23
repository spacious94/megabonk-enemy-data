# Speed Boi

> Slows time when taking damage below HP threshold

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 51 |
| **Internal Name** | SpeedBoi |
| **Class Name** | ItemSpeedBoi |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **Price** | 10 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnDamageTaken - TimeSlowdown

Slows time when taking damage below HP threshold

**Hpthreshold:**
- base: `0.5`
- formula: `Triggers at 50% HP`

**Damagemultiplier:**
- base: `2.0`
- formula: `+100% damage during slowdown`

**Duration:**
- base: `2.0`
- perStack: `2.0`
- formula: `amount * 2.0 seconds`

## Internal Fields

| Field | Value |
|-------|-------|
| damageMultiplierDuringFreeze | 2.0 |
| durationPerAmount | 2.0 |
| normalCooldown | 10.0 |
| slowdownHpRatio | 0.5 |

## Implementation Details

- **Constructor RVA:** `0x45B8F0`
- **Init RVA:** `0x45B100`
- **Cleanup RVA:** `0x45AC30`
- **Oninitoramountchanged RVA:** `0x45B440`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
