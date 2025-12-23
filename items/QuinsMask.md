# Quin's Mask

> Reflects damage and deals spread damage to nearby enemies

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 80 |
| **Internal Name** | QuinsMask |
| **Class Name** | ItemQuinsMask |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **Price** | 7 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - ThornsWithSpread

Reflects damage and deals spread damage to nearby enemies

**Thorns:**
- base: `thornsPerAmount`
- formula: `amount * thornsPerAmount`

**Radius:**
- base: `baseRadius`
- perStack: `radiusPerAmount`
- max: `maxRadius`

## Internal Fields

| Field | Value |
|-------|-------|
| thornsPerAmount | extracted from constructor |
| baseRadius | extracted from constructor |
| radiusPerAmount | extracted from constructor |
| maxRadius | extracted from constructor |
| damageSpreadMultiplier | extracted from constructor |
| procChance | extracted from constructor |
| maxProcsPerTick | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x450750`
- **Init RVA:** `0x450070`
- **Oninitoramountchanged RVA:** `0x450230`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
