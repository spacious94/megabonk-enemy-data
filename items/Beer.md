# Beer

> +20% damage per stack

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 1 |
| **Internal Name** | Beer |
| **Class Name** | ItemBeer |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| DamageMultiplier | Flat | +20.0% per stack | Linear |
| MaxHealth | Flat | +-5.0% per stack | Linear |

## Internal Fields

| Field | Value |
|-------|-------|
| damagePerStack | 0.2 |
| maxHealthPerStack | -0.05 |

## Implementation Details

- **Constructor RVA:** `0x439690`
- **Oninitoramountchanged RVA:** `0x439520`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
