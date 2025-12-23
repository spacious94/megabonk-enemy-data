# Brass Knuckles

> Increases damage in an AOE around the player

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 55 |
| **Internal Name** | BrassKnuckles |
| **Class Name** | ItemBrassKnuckles |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **Price** | 5 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### PreAttack - AOEDamageBonus

Increases damage in an AOE around the player

**Damagebonus:**
- base: `0.25`
- perStack: `0.25`
- formula: `amount * 0.25`

**Radius:**
- base: `7.0`
- perStack: `2.0`
- formula: `7.0 + (amount - 1) * 2.0`

## Internal Fields

| Field | Value |
|-------|-------|
| damagePerAmount | 0.25 |
| baseRadius | 7.0 |
| radiusAddPerAmount | 2.0 |

## Implementation Details

- **Constructor RVA:** `0x43C470`
- **Oninitoramountchanged RVA:** `0x43C3F0`
- **Preattack RVA:** `0x43C420`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** Yes
