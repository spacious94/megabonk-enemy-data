# Steel Pot

> Increases the maximum level cap for weapons and tomes

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 84 |
| **Internal Name** | Pot |
| **Class Name** | ItemPotSteel |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **Price** | 21 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### Passive - IncreaseLevelCaps

Increases the maximum level cap for weapons and tomes

**Weaponlevels:**
- base: `weaponMaxLevelsPerAmount`
- formula: `amount * weaponMaxLevelsPerAmount`

**Tomelevels:**
- base: `tomeMaxLevelsPerAmount`
- formula: `amount * tomeMaxLevelsPerAmount`

## Internal Fields

| Field | Value |
|-------|-------|
| weaponMaxLevelsPerAmount | extracted from constructor |
| tomeMaxLevelsPerAmount | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x44F160`
- **Oninitoramountchanged RVA:** `0x44F140`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
