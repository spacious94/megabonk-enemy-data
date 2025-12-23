# Boss Buster

> Increases damage dealt to bosses

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 65 |
| **Internal Name** | BossBuster |
| **Class Name** | ItemBossBuster |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **Price** | 3 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### PreAttack - BossDamageBonus

Increases damage dealt to bosses

**Damagebonus:**
- base: `damagePerAmount`
- perStack: `damagePerAmount`
- formula: `amount * damagePerAmount`

## Internal Fields

| Field | Value |
|-------|-------|
| damagePerAmount | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x43C300`
- **Oninitoramountchanged RVA:** `0x43C210`
- **Preattack RVA:** `0x43C230`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** Yes
