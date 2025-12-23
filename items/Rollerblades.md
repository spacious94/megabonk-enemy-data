# Turbo Skates

> Up to +40% attack speed per stack while moving

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 37 |
| **Internal Name** | Rollerblades |
| **Class Name** | ItemRollerblades |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **Price** | 7 |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| AttackSpeed | Flat | +dynamic per stack | Based on movement |

## Internal Fields

| Field | Value |
|-------|-------|
| maxAttackSpeedPerAmount | 0.4 |
| updateStatsInterval | 0.25 |

## Implementation Details

- **Constructor RVA:** `0x4A7B90`
- **Oninitoramountchanged RVA:** `0x4A7A70`
- **Tick RVA:** `0x4A7A90`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
