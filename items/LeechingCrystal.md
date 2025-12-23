# Leeching Crystal

> +HP based on maxHpPerAmount field

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 66 |
| **Internal Name** | LeechingCrystal |
| **Class Name** | ItemLeechingCrystal |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **Price** | 7 |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| MaxHealth | Flat | +amount * maxHpPerAmount per stack | Linear |
| HpRegen | Addition | amount * regenAdditivePerAmount per stack | Linear |

## Internal Fields

| Field | Value |
|-------|-------|
| regenAdditivePerAmount | extracted from constructor |
| maxHpPerAmount | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x44C5A0`
- **Oninitoramountchanged RVA:** `0x44C4D0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
