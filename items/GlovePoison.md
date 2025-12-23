# Poison Glove

> On hit, deal poison damage in an area and apply poison stacks (cooldown-based)

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 73 |
| **Internal Name** | GlovePoison |
| **Class Name** | ItemGlovesPoison |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **Price** | 5 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - PoisonAOE

On hit, deal poison damage in an area and apply poison stacks (cooldown-based)

**Damage:**
- base: `baseDamageMultiplier`
- formula: `Uses base damage multiplier`

## Internal Fields

| Field | Value |
|-------|-------|
| cooldown | extracted from constructor |
| baseDamageMultiplier | extracted from constructor |
| baseRadius | extracted from constructor |
| poisonStacksPerAmount | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x446FA0`
- **Proconhiteffects RVA:** `0x4469D0`
- **Getdamage RVA:** `0x446940`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
