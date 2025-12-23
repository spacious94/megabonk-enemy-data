# Mirror

> Blocks and reflects incoming damage back to enemies

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 48 |
| **Internal Name** | Mirror |
| **Class Name** | ItemMirror |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnDamageTaken - ReflectDamage

Blocks and reflects incoming damage back to enemies

**Damagemultiplier:**
- base: `1.0`
- perStack: `0.25`
- formula: `1.0 + (amount - 1) * 0.25`

**Cooldown:**
- base: `8.0`
- min: `4.0`

## Internal Fields

| Field | Value |
|-------|-------|
| cooldown | 8.0 |
| minCooldown | 4.0 |
| damageMultiplier | 1.0 |
| damagePerAmount | 0.25 |

## Implementation Details

- **Constructor RVA:** `0x4A2450`
- **Init RVA:** `0x4A1FA0`
- **Cleanup RVA:** `0x4A1EE0`
- **Oncheckstopdamage RVA:** `0x4A2020`
- **Reflectdamage RVA:** `0x4A20B0`
- **Tick RVA:** `0x4A23C0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
