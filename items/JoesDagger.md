# Joe's Dagger

> Accumulates 1% of all damage dealt into stacks

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 49 |
| **Internal Name** | JoesDagger |
| **Class Name** | ItemJoesDagger |
| **Rarity** | Legendary |
| **Max Stacks** | 10 |
| **Price** | 14 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnDamage - DamageAccumulation

Accumulates 1% of all damage dealt into stacks

### PreAttack - ExecuteChance

Chance to instantly kill enemies based on stacks

**Chanceperstack:**
- base: `0.01`
- formula: `amount * 0.01`

## Internal Fields

| Field | Value |
|-------|-------|
| attackDamagePerProc | 0.01 |
| executionChancePerAmount | 0.01 |
| executionChance | 0.01 |
| maxStacks | 999999 |
| rollCooldown | 0.3 |

## Implementation Details

- **Constructor RVA:** `0x44B7B0`
- **Init RVA:** `0x44B390`
- **Cleanup RVA:** `0x44B030`
- **Oninitoramountchanged RVA:** `0x44B5C0`
- **Tick RVA:** `0x44B6B0`
- **Preattack RVA:** `0x44B5E0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** Yes
