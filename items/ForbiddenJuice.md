# Forbidden Juice

> +5% crit chance per stack (estimated)

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 9 |
| **Internal Name** | ForbiddenJuice |
| **Class Name** | ItemForbiddenJuice |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **Price** | 3 |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| CritChance | Flat | +5.0% per stack | Linear |

## Internal Fields

| Field | Value |
|-------|-------|
| critPerStack | 0.05 |

## Implementation Details

- **Getdescription RVA:** `0x4596C0`
- **Oninitoramountchanged RVA:** `0x459850`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
