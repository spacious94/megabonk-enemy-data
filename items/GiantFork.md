# Giant Fork

> Chance for attacks to deal massive 'Mega Crit' damage

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 12 |
| **Internal Name** | GiantFork |
| **Class Name** | ItemGiantFork |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| CritChance | Flat | +15.0% per stack | Linear |

## Special Effects

### PreAttack - MegaCrit

Chance for attacks to deal massive 'Mega Crit' damage

**Chance:**
- baseValue: `0.14`
- scaling: `linear`
- formula: `amount * 0.14`

## Internal Fields

| Field | Value |
|-------|-------|
| critChancePerAmount | 0.15 |
| megaCritChancePerAmount | 0.14 |
| megaCritDamageMultiplier | 4.0 |

## Implementation Details

- **Constructor RVA:** `0x45F0C0`
- **Oninitoramountchanged RVA:** `0x45EFA0`
- **Preattack RVA:** `0x45EFC0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** Yes
