# Idle Juice

> Gain damage bonus while standing still

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 56 |
| **Internal Name** | IdleJuice |
| **Class Name** | ItemIdleJuice |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **Price** | 6 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### Passive - IdleDamageBonus

Gain damage bonus while standing still

**Damagebonus:**
- base: `1.0`
- perStack: `1.0`
- formula: `amount * 1.0 (100% per stack)`

**Chargerate:**
- base: `0.04`
- formula: `4% damage per second while idle`

## Internal Fields

| Field | Value |
|-------|-------|
| damagePerAmount | 1.0 |
| damagePerSecond | 0.04 |
| setupTime | 0.6 |
| distThreshold | 1.75 |
| updateDamageInterval | 1.0 |

## Implementation Details

- **Constructor RVA:** `0x44B000`
- **Oninitoramountchanged RVA:** `0x43C210`
- **Tick RVA:** `0x44AB80`
- **Createcamp RVA:** `0x44A8B0`
- **Removecamp RVA:** `0x44AB00`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
