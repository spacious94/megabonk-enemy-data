# Scarf

> Increases damage while airborne

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 40 |
| **Internal Name** | Scarf |
| **Class Name** | ItemScarf |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### Passive - AirborneDamageBonus

Increases damage while airborne

**Damagebonus:**
- base: `0.5`
- perStack: `0.5`
- formula: `amount * 0.5`

## Internal Fields

| Field | Value |
|-------|-------|
| damageAddPerAmount | 0.5 |

## Implementation Details

- **Constructor RVA:** `0x458910`
- **Init RVA:** `0x458630`
- **Cleanup RVA:** `0x4583D0`
- **Oninitoramountchanged RVA:** `0x458770`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
