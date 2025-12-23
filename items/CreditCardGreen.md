# Credit Card (Green)

> Gain permanent luck bonus for each chest opened

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 64 |
| **Internal Name** | CreditCardGreen |
| **Class Name** | ItemCreditCardGreen |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnChestOpen - AccumulateLuck

Gain permanent luck bonus for each chest opened

**Luckperchest:**
- base: `luckPerChestPerAmount`
- formula: `amount * luckPerChestPerAmount per chest`

## Internal Fields

| Field | Value |
|-------|-------|
| luckPerChestPerAmount | extracted from constructor |
| accumulatedLuck | tracked at runtime |

## Implementation Details

- **Constructor RVA:** `0x43EFE0`
- **Init RVA:** `0x43EC80`
- **Cleanup RVA:** `0x43E8B0`
- **Oninitoramountchanged RVA:** `0x43C210`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
