# Snek

> Chance to poison enemies and chance for poisoned enemies to explode

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 83 |
| **Internal Name** | Snek |
| **Class Name** | ItemSnek |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **Price** | 20 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - PoisonWithExplosion

Chance to poison enemies and chance for poisoned enemies to explode

**Poisonchance:**
- base: `poisonChancePerAmount`
- formula: `amount * poisonChancePerAmount`

**Explosionchance:**
- base: `poisonBurstChancePerAmount`
- formula: `amount * poisonBurstChancePerAmount`

**Damageratio:**
- base: `damageRatio`
- perStack: `damageRatioPerAmount`

## Internal Fields

| Field | Value |
|-------|-------|
| poisonChancePerAmount | extracted from constructor |
| poisonBurstChancePerAmount | extracted from constructor |
| damageRatio | extracted from constructor |
| damageRatioPerAmount | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x459F80`
- **Oninitoramountchanged RVA:** `0x459610`
- **Proconhiteffects RVA:** `0x459650`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
