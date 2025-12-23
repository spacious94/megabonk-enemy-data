# Gas Mask

> Gain armor and overheal based on poisoned enemies

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 52 |
| **Internal Name** | Gasmask |
| **Class Name** | ItemGasmask |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **Price** | 7 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### Passive - PoisonStacking

Gain armor and overheal based on poisoned enemies

**Armorperstack:**
- base: `0.005`
- formula: `0.5% armor per poisoned enemy`

**Overhealperstack:**
- base: `0.005`
- formula: `0.5% overheal per poisoned enemy`

**Maxarmor:**
- base: `0.4`
- perStack: `0.4`
- formula: `amount * 0.4`

**Maxoverheal:**
- base: `0.25`
- perStack: `0.25`
- formula: `amount * 0.25`

## Internal Fields

| Field | Value |
|-------|-------|
| armorPerStack | 0.005 |
| overhealPerStack | 0.005 |
| maxArmorPerAmount | 0.4 |
| maxOverhealPerAmount | 0.25 |
| updateInverval | 1.0 |

## Implementation Details

- **Constructor RVA:** `0x444620`
- **Init RVA:** `0x444100`
- **Cleanup RVA:** `0x443E80`
- **Oninitoramountchanged RVA:** `0x444230`
- **Tick RVA:** `0x444320`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
