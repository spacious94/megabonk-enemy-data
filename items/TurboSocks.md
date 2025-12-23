# Turbo Socks

> +15% move speed per stack

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 30 |
| **Internal Name** | TurboSocks |
| **Class Name** | ItemTurboSocks |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **Price** | 3 |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| MoveSpeedMultiplier | Flat | +15.0% per stack | Linear |

## Internal Fields

| Field | Value |
|-------|-------|
| moveSpeedPerAmount | 0.15 |

## Implementation Details

- **Constructor RVA:** `0x43D600`
- **Oninitoramountchanged RVA:** `0x4BB300`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
