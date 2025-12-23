# Curse Glove

> Chance on hit to deal curse damage in an area

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 75 |
| **Internal Name** | GloveCurse |
| **Class Name** | ItemGlovesCursed |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **Price** | 8 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - CurseAOE

Chance on hit to deal curse damage in an area

**Procchance:**
- base: `procChancePerAmount`
- formula: `amount * procChancePerAmount`

**Damage:**
- base: `baseDamageMultiplier`
- formula: `Uses base damage multiplier`

## Internal Fields

| Field | Value |
|-------|-------|
| procChancePerAmount | extracted from constructor |
| difficultyPerAmount | extracted from constructor |
| maxHpMultiplierPerAmount | extracted from constructor |
| baseDamageMultiplier | extracted from constructor |
| baseRadius | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x446040`
- **Oninitoramountchanged RVA:** `0x445990`
- **Proconhiteffects RVA:** `0x445AA0`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
