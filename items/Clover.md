# Clover

> Increases your luck, improving various random outcomes.

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 35 |
| **Internal Name** | Clover |
| **Class Name** | ItemClover |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| Luck | Flat | +7.5% per stack | Linear |

## Formula

```
Total Luck Bonus = stacks × 0.075
```

**Example:**
- 1 stack: +7.5% luck
- 4 stacks: +30% luck
- 10 stacks: +75% luck

## What Luck Affects

Luck increases the probability of favorable random events:
- Critical hit chance (additive bonus)
- Item drop quality
- Chest contents
- Various proc chances

## Implementation Details

- **Constructor RVA:** `0x454010`
- **OnInitOrAmountChanged RVA:** `0x453F60`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No

### Internal Fields

| Field | Type | Default Value |
|-------|------|---------------|
| luckPerAmount | float | 0.075 |

## Technical Notes

- Luck is applied as a **Flat** modifier
- The Luck stat affects many probability-based systems in the game
- Stacks linearly with no cap

