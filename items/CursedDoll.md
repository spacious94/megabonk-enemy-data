# Cursed Doll

> Curses nearby enemies, dealing damage over time

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 43 |
| **Internal Name** | CursedDoll |
| **Class Name** | ItemCursedDoll |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **Price** | 3 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### Passive - CurseEnemies

Curses nearby enemies, dealing damage over time

**Damagepertick:**
- baseValue: `0.3`
- formula: `enemy max HP * 0.3 per tick`

## Internal Fields

| Field | Value |
|-------|-------|
| damageMaxHpPercentage | 0.3 |
| enemiesCursedPerDoll | 2 |
| maxNumCursesPerCheck | 5 |
| attackCooldown | 1.0 |

## Implementation Details

- **Constructor RVA:** `0x459340`
- **Init RVA:** `0x458F60`
- **Cleanup RVA:** `0x458EA0`
- **Onenemydied RVA:** `0x459050`
- **Tick RVA:** `0x459060`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
