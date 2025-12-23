# Bloody Cleaver

> Chance to apply bloodmark stacks when lifesteal procs

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 62 |
| **Internal Name** | BloodyCleaver |
| **Class Name** | ItemBloodyCleaver |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **Price** | 15 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - BloodmarkOnLifesteal

Chance to apply bloodmark stacks when lifesteal procs

**Bloodmarkstacks:**
- base: `bloodmarkStacksPerLifestealPerAmount`
- formula: `amount * bloodmarkStacksPerLifestealPerAmount`

**Bloodmarkchance:**
- base: `bloodmarkChancePerAmount`
- formula: `amount * bloodmarkChancePerAmount`

## Internal Fields

| Field | Value |
|-------|-------|
| bloodmarkStacksPerLifestealPerAmount | extracted from constructor |
| bloodmarkChancePerAmount | extracted from constructor |

## Implementation Details

- **Constructor RVA:** `0x43A4A0`
- **Init RVA:** `0x439DD0`
- **Cleanup RVA:** `0x439AD0`
- **Oninitoramountchanged RVA:** `0x439F20`
- **Proconhiteffects RVA:** `0x43A000`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
