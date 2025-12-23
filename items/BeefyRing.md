# Beefy Ring

> +10 max HP per stack

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 21 |
| **Internal Name** | BeefyRing |
| **Class Name** | ItemBeefyRing |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| MaxHealth | Flat | +10 per stack | Linear |
| DamageMultiplier | Flat | +dynamic per stack | Based on max hp |

## Internal Fields

| Field | Value |
|-------|-------|
| maxHpPerStack | 10 |
| powerPerHpPerAmount | 0.002 |

## Implementation Details

- **Constructor RVA:** `0x43B470`
- **Oninitoramountchanged RVA:** `0x43B340`
- **Refreshpower RVA:** `0x43B3D0`
- **Tick RVA:** `0x43B4A0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
