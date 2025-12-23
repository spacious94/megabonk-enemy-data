# Ice Crystal

> Chance to freeze enemies on hit

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 70 |
| **Internal Name** | IceCrystal |
| **Class Name** | ItemIceCrystal |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **Price** | 4 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - FreezeChance

Chance to freeze enemies on hit

**Freezechance:**
- base: `procChancePerAmount`
- formula: `amount * procChancePerAmount`

## Internal Fields

| Field | Value |
|-------|-------|
| freezeTime | extracted from constructor |
| procChancePerAmount | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x44A1F0`
- **Oninitoramountchanged RVA:** `0x44A100`
- **Proconhiteffects RVA:** `0x44A180`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
