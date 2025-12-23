# Holy Book

> When healing, deal damage to nearby enemies

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 54 |
| **Internal Name** | HolyBook |
| **Class Name** | ItemHolyBook |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **Price** | 10 |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| MaxHealth | Flat | +100 per stack | Linear |
| HpRegen | Flat | +50 per stack | Linear |
| Overheal | Flat | +25.0% per stack | Linear |

## Special Effects

### OnHeal - DamageNearbyEnemies

When healing, deal damage to nearby enemies

**Radius:**
- base: `5.0`
- perStack: `1.0`
- formula: `5.0 + amount * 1.0`

## Internal Fields

| Field | Value |
|-------|-------|
| maxHpPerAmount | 100.0 |
| hpRegenPerAmount | 50.0 |
| overhealPerAmount | 0.25 |
| radiusPerAmount | 1.0 |
| cooldown | 1.5 |

## Implementation Details

- **Constructor RVA:** `0x449F10`
- **Init RVA:** `0x449730`
- **Cleanup RVA:** `0x449420`
- **Oninitoramountchanged RVA:** `0x449890`
- **Tick RVA:** `0x4499D0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
