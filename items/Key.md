# Key

> Chance to get an extra item from chests

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 0 |
| **Internal Name** | Key |
| **Class Name** | ItemKey |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **Price** | 3 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnChestOpen - ExtraItem

Chance to get an extra item from chests

**Chance:**
- baseValue: `0.1`
- scaling: `linear`
- formula: `stacks * 0.1`

## Internal Fields

| Field | Value |
|-------|-------|
| chancePerStack | 0.1 |
| currentChance | 0.1 |

## Implementation Details

- **Constructor RVA:** `0x495D80`
- **Oninitoramountchanged RVA:** `0x495D20`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
