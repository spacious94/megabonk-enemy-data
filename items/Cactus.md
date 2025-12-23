# Cactus

> Fire spine projectiles when taking damage

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 68 |
| **Internal Name** | Cactus |
| **Class Name** | ItemCactus |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **Price** | 4 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnDamageTaken - SpineRetaliation

Fire spine projectiles when taking damage

**Damage:**
- base: `damagePerAmount`
- formula: `amount * damagePerAmount`

**Projectiles:**
- base: `numProjectilesPerAmount`
- formula: `amount * numProjectilesPerAmount`

## Internal Fields

| Field | Value |
|-------|-------|
| damagePerAmount | extracted from constructor |
| numProjectilesPerAmount | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x43D410`
- **Init RVA:** `0x43C720`
- **Cleanup RVA:** `0x43C490`
- **Oninitoramountchanged RVA:** `0x43C870`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
