# Lightning Glove

> On hit, deal lightning damage in an area (cooldown-based)

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 72 |
| **Internal Name** | GloveLightning |
| **Class Name** | ItemGlovesLightning |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - LightningAOE

On hit, deal lightning damage in an area (cooldown-based)

**Damage:**
- base: `baseDamageMultiplier`
- formula: `Uses base damage multiplier`

## Internal Fields

| Field | Value |
|-------|-------|
| cooldown | extracted from constructor |
| baseDamageMultiplier | extracted from constructor |
| baseRadius | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x446880`
- **Proconhiteffects RVA:** `0x446280`
- **Getdamage RVA:** `0x446110`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
