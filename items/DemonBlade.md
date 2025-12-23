# Demon Blade

> A cursed blade that heals you on critical strikes.

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 10 |
| **Internal Name** | DemonBlade |
| **Class Name** | ItemDemonBlade |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| Crit Chance | Flat | +1% | Fixed (does not scale) |

## Special Effects

### On Critical Hit - Heal

When you land a critical hit, you have a chance to heal 1 HP.

| Property | Value |
|----------|-------|
| **Trigger** | On Critical Hit |
| **Base Chance** | 25% per stack |
| **Heal Amount** | 1 HP |
| **Proc Coefficient** | Yes (affected) |
| **Requires** | Can Lifesteal |

## Formulas

### Crit Chance Bonus
```
Crit Chance Bonus = 0.01 (1%)
```
Note: This is a fixed value and does NOT scale with stacks.

### Heal Chance
```
Total Heal Chance = stacks × 0.25 × procCoefficient
Heal Rolls = floor(Total Heal Chance) + (random < remainder ? 1 : 0)
```

**Example with 100% proc coefficient:**
- 1 stack: 25% chance to heal 1 HP
- 2 stacks: 50% chance to heal 1 HP
- 4 stacks: 100% chance to heal 1 HP (guaranteed)
- 8 stacks: 200% → guaranteed 2 HP heals per crit

## Implementation Details

- **Constructor RVA:** `0x45A0F0`
- **Init RVA:** `0x459B10`
- **Cleanup RVA:** `0x459A70`
- **OnInitOrAmountChanged RVA:** `0x45A020`
- **OnEnemyDamaged RVA:** `0x459C80`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No

### Internal Fields

| Field | Type | Default Value |
|-------|------|---------------|
| critChance | float | 0.01 |
| healChancePerStack | float | 0.25 |
| totalHealChance | float | calculated at runtime |

## Event Subscriptions

- Subscribes to enemy damaged events in `Init()`
- Unsubscribes in `Cleanup()`

## Technical Notes

- The crit chance bonus is **fixed at 1%** regardless of stack count
- The heal chance scales linearly with stacks (25% per stack)
- Healing is affected by `procCoefficient` of the attack
- Must pass `CanLifesteal()` check (blocked by certain debuffs)
- Uses hypergeometric distribution for multiple heal rolls when chance exceeds 100%

## Related Items

- **Leeching Crystal** - Alternative lifesteal mechanic
- **Demonic Blood** - Other demonic-themed item
- **Demonic Soul** - Other demonic-themed item
