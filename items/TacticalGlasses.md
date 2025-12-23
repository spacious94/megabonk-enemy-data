# Tactical Glasses

> Increases damage dealt to enemies

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 67 |
| **Internal Name** | TacticalGlasses |
| **Class Name** | ItemTacticalGlasses |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **Price** | 3 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### PreAttack - DamageBonus

Increases damage dealt to enemies

**Damagebonus:**
- base: `0.2`
- perStack: `0.2`
- formula: `amount * 0.2 (20% per stack)`

## Internal Fields

| Field | Value |
|-------|-------|
| damagePerAmount | 0.2 |

## Implementation Details

- **Constructor RVA:** `0x45C740`
- **Oninitoramountchanged RVA:** `0x43C210`
- **Preattack RVA:** `0x45C680`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** Yes
