# Kevin

> Chance to take damage when dealing damage to enemies

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 57 |
| **Internal Name** | Kevin |
| **Class Name** | ItemKevin |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **Price** | 8 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnEnemyDamage - SelfDamageChance

Chance to take damage when dealing damage to enemies

*Deals damage to player but provides some benefit (likely damage boost)*

**Damagechance:**
- base: `0.25`
- perStack: `0.25`
- formula: `amount * 0.25`

## Internal Fields

| Field | Value |
|-------|-------|
| damageChancePerAmount | 0.25 |

## Implementation Details

- **Constructor RVA:** `0x44C120`
- **Init RVA:** `0x44BEA0`
- **Cleanup RVA:** `0x44BBE0`
- **Oninitoramountchanged RVA:** `0x43C210`
- **Tick RVA:** `0x44C080`
- **Onenemydamaged RVA:** `0x44BFF0`
- **Checkselfdamage RVA:** `0x44B860`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
