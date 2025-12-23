# Chonkplate

> +75% overheal capacity per stack

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 16 |
| **Internal Name** | Chonkplate |
| **Class Name** | ItemChonkplate |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **Price** | 10 |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| Overheal | Flat | +75.0% per stack | Linear |
| Lifesteal | Flat | +20.0% per stack | Linear |

## Internal Fields

| Field | Value |
|-------|-------|
| overhealPerAmount | 0.75 |
| lifestealPerAmount | 0.2 |

## Implementation Details

- **Constructor RVA:** `0x454CF0`
- **Oninitoramountchanged RVA:** `0x454B90`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
