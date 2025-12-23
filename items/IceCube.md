# Ice Cube

> Chance to deal ice damage and freeze enemies

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 18 |
| **Internal Name** | IceCube |
| **Class Name** | ItemIceCube |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - FreezeProc

Chance to deal ice damage and freeze enemies

**Procchance:**
- baseValue: `0.2`
- scaling: `linear`
- formula: `amount * 0.2`

**Freezechance:**
- baseValue: `0.4`
- scaling: `linear`
- formula: `amount * 0.4`

**Damage:**
- baseRatio: `0.8`
- perStack: `0.4`
- formula: `baseDamage * (0.8 + (amount - 1) * 0.4)`

## Internal Fields

| Field | Value |
|-------|-------|
| procChancePerAmount | 0.2 |
| freezeChancePerAmount | 0.4 |
| damageRatio | 0.8 |
| damageRatioPerAmount | 0.4 |

## Implementation Details

- **Constructor RVA:** `0x4971D0`
- **Oninitoramountchanged RVA:** `0x496F20`
- **Proconhiteffects RVA:** `0x496F60`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
