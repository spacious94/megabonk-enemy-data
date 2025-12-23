# Skuleg

> +7% difficulty per stack (increases enemy spawn rate/strength)

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 38 |
| **Internal Name** | Skuleg |
| **Class Name** | ItemSkuleg |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **Price** | 4 |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| Difficulty | Flat | +7.0% per stack | Linear |

## Internal Fields

| Field | Value |
|-------|-------|
| difficultyPerAmount | 0.07 |

## Implementation Details

- **Constructor RVA:** `0x4BA990`
- **Oninitoramountchanged RVA:** `0x4BA8A0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
