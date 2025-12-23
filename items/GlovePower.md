# Power Glove

> Chance on hit to deal damage in an area with knockback

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 76 |
| **Internal Name** | GlovePower |
| **Class Name** | ItemGlovesPower |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - PowerAOEWithKnockback

Chance on hit to deal damage in an area with knockback

**Procchance:**
- base: `procChancePerAmount`
- formula: `Hyperbolic scaling with 50% cap`

**Damage:**
- base: `baseDamageMultiplier`
- formula: `Uses base damage multiplier`

**Radius:**
- base: `10.0`
- perStack: `radiusPerAmount`
- formula: `10.0 + amount * radiusPerAmount`

**Cooldown:**
- base: `3.2`
- min: `0.2`
- max: `2.0`
- formula: `3.2 - amount * 0.2, clamped between 0.2 and 2.0`

## Internal Fields

| Field | Value |
|-------|-------|
| knockbackForce | extracted from constructor |
| procChancePerAmount | extracted from constructor |
| baseDamageMultiplier | extracted from constructor |
| radiusPerAmount | extracted from constructor |
| cooldown | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x447960`
- **Oninitoramountchanged RVA:** `0x4471E0`
- **Proconhiteffects RVA:** `0x447270`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
