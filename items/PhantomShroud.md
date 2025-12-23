# Phantom Shroud

> When you evade an attack, gain temporary buff stacks

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 8 |
| **Internal Name** | PhantomShroud |
| **Class Name** | ItemPhantomShroud |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| Evasion | Flat | +5.0% per stack | Linear |

## Special Effects

### OnEvade - TemporaryBuffStacks

When you evade an attack, gain temporary buff stacks

**Maxstacks:**
- formula: `amount * 4`

**Timeout:**
- base: `3.0`
- perStack: `0.5`
- max: `6.0`
- formula: `min(3 + (amount - 1) * 0.5, 6)`

**Buffs:**
- attackSpeed: `{'perStack': 0.25, 'description': '+25% attack speed per buff stack'}`
- damage: `{'perStack': 0.5, 'description': '+50% damage per buff stack'}`

## Internal Fields

| Field | Value |
|-------|-------|
| evasionPerAmount | 0.05 |
| damageMultiplierBase | 2.0 |
| damageMultiplierPerAmount | 0.5 |
| speedAdditionBase | 0.5 |
| speedAdditionPerAmount | 0.15 |
| timeout | 2.0 |
| attackSpeedPerStack | 0.25 |
| damagePerStack | 0.5 |

## Implementation Details

- **Constructor RVA:** `0x4A06F0`
- **Init RVA:** `0x4A0390`
- **Cleanup RVA:** `0x4A0210`
- **Onevade RVA:** `0x4A03C0`
- **Oninitoramountchanged RVA:** `0x4A0510`
- **Preattack RVA:** `0x4A0570`
- **Tick RVA:** `0x4A05A0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** Yes
