# Credit Card (Red)

> Gain permanent damage bonus for each chest opened

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 63 |
| **Internal Name** | CreditCardRed |
| **Class Name** | ItemCreditCardRed |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnChestOpen - AccumulateDamage

Gain permanent damage bonus for each chest opened

**Damageperchest:**
- base: `damagePerChestAmount`
- formula: `amount * damagePerChestAmount per chest`

## Internal Fields

| Field | Value |
|-------|-------|
| damagePerChestAmount | extracted from constructor |
| accumulatedDamage | tracked at runtime |

## Implementation Details

- **Constructor RVA:** `0x43F710`
- **Init RVA:** `0x43F3C0`
- **Cleanup RVA:** `0x43EFF0`
- **Oninitoramountchanged RVA:** `0x43C210`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
