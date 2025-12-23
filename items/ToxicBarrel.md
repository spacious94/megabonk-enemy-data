# Toxic Barrel

> Creates a poison cloud when taking damage

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 53 |
| **Internal Name** | ToxicBarrel |
| **Class Name** | ItemToxicBarrel |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **Price** | 7 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnDamageTaken - PoisonAOE

Creates a poison cloud when taking damage

**Radius:**
- base: `0`
- perStack: `1.0`
- formula: `amount * 1.0`

**Poisonstacks:**
- base: `5`
- perStack: `5`
- formula: `amount * 5 stacks`

## Internal Fields

| Field | Value |
|-------|-------|
| radiusPerAmount | 1.0 |
| poisonStacksPerAmount | 5 |
| cooldown | 0.25 |
| poisonDuration | 5.0 |

## Implementation Details

- **Constructor RVA:** `0x45CF80`
- **Init RVA:** `0x45CD60`
- **Cleanup RVA:** `0x45CC10`
- **Oninitoramountchanged RVA:** `0x45CEB0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
