# Old Mask

> Increases chance for elite enemies to spawn

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 82 |
| **Internal Name** | OldMask |
| **Class Name** | ItemOldMask |
| **Rarity** | Common |
| **Max Stacks** | Unlimited |
| **Price** | 4 |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| EliteSpawnChance | Addition | eliteSpawnChancePerAmount per stack | Linear |

## Internal Fields

| Field | Value |
|-------|-------|
| eliteSpawnChancePerAmount | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x43C300`
- **Oninitoramountchanged RVA:** `0x44E670`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
