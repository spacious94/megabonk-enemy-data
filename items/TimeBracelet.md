# Time Bracelet

> Increases damage based on game time

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 71 |
| **Internal Name** | TimeBracelet |
| **Class Name** | ItemTimeBracelet |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### Passive - TimeDamageBonus

Increases damage based on game time

**Damagebonus:**
- base: `damagePerAmount`
- formula: `amount * damagePerAmount`

## Internal Fields

| Field | Value |
|-------|-------|
| damagePerAmount | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x4390B0`
- **Oninitoramountchanged RVA:** `0x45C960`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
