# Lightning Orb

> Chance to zap a nearby enemy with chain lightning

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 17 |
| **Internal Name** | LightningOrb |
| **Class Name** | ItemLightningOrb |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **Price** | 10 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - ChainLightning

Chance to zap a nearby enemy with chain lightning

**Procchance:**
- baseValue: `0.25`
- scaling: `linear`
- formula: `amount * 0.25`

**Stunchance:**
- baseValue: `0.25`
- scaling: `linear`
- formula: `amount * 0.25`

**Damage:**
- baseRatio: `0.4`
- perStack: `0.4`
- formula: `baseDamage * (0.4 + (amount - 1) * 0.4)`

## Internal Fields

| Field | Value |
|-------|-------|
| procChancePerAmount | 0.25 |
| stunChancePerAmount | 0.25 |
| baseRadius | 40.0 |
| damageRatio | 0.4 |
| damageRatioPerAmount | 0.4 |

## Implementation Details

- **Constructor RVA:** `0x4A1C50`
- **Oninitoramountchanged RVA:** `0x4A1320`
- **Proconhiteffects RVA:** `0x4A1380`
- **Tick RVA:** `0x4A1B00`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
