# Blood Glove

> On hit, deal blood damage in an area and heal (cooldown-based)

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 74 |
| **Internal Name** | GloveBlood |
| **Class Name** | ItemGlovesBlood |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - BloodAOEWithHeal

On hit, deal blood damage in an area and heal (cooldown-based)

**Damage:**
- base: `baseDamageMultiplier`
- formula: `Uses base damage multiplier`

## Internal Fields

| Field | Value |
|-------|-------|
| cooldown | extracted from constructor |
| baseDamageMultiplier | extracted from constructor |
| baseRadius | extracted from constructor |
| healPercentage | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x445600`
- **Proconhiteffects RVA:** `0x444F70`
- **Getdamage RVA:** `0x444DA0`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
