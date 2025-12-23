# Pumpkin

> Spawns extra pots and increases pot rewards

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 86 |
| **Internal Name** | Pumpkin |
| **Class Name** | ItemPumpkin |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **Price** | 9 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### Passive - ExtraPotsAndRewards

Spawns extra pots and increases pot rewards

**Extrapots:**
- base: `extraPotsPerAmount`
- formula: `amount * extraPotsPerAmount`

**Rewardmultiplier:**
- base: `rewardMultiplierPerAmount`
- formula: `amount * rewardMultiplierPerAmount`

## Internal Fields

| Field | Value |
|-------|-------|
| extraPotsPerAmount | extracted from constructor |
| rewardMultiplierPerAmount | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x44FF70`
- **Getrewardmultiplier RVA:** `0x44FF50`
- **Getextrapotssmall RVA:** `0x439270`
- **Getextrapotsbig RVA:** `0x44FF30`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
