# Spiky Shield

> Deals retaliation damage to nearby enemies based on armor

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 2 |
| **Internal Name** | SpikyShield |
| **Class Name** | ItemSpikyShield |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| Armor | Flat | +10.0% per stack | Linear |

## Special Effects

### Passive - Retaliation

Deals retaliation damage to nearby enemies based on armor

**Value:**
- baseValue: `200.0`
- formula: `totalArmor * 200 * stacks`

## Internal Fields

| Field | Value |
|-------|-------|
| armorPerAmount | 0.1 |
| retaliationPerArmorPerAmount | 200.0 |

## Implementation Details

- **Constructor RVA:** `0x4B9E10`
- **Oninitoramountchanged RVA:** `0x4B9C20`
- **Tick RVA:** `0x4B9C90`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
