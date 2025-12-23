# Unstable Transfusion

> Chance to apply bloodmark stacks on hit

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 61 |
| **Internal Name** | UnstableTransfusion |
| **Class Name** | ItemUnstableTransfusion |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - StackBloodmark

Chance to apply bloodmark stacks on hit

**Chance:**
- base: `0.27`
- perStack: `0.27`
- formula: `amount * 0.27 (27% per stack)`

## Internal Fields

| Field | Value |
|-------|-------|
| chanceToStackPerAmount | 0.27 |

## Implementation Details

- **Constructor RVA:** `0x45D5C0`
- **Oninitoramountchanged RVA:** `0x43C210`
- **Proconhiteffects RVA:** `0x45D4C0`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
