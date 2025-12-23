# Gamer Goggles

> Increases damage based on player level

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 60 |
| **Internal Name** | GamerGoggles |
| **Class Name** | ItemGamerGoggles |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **Price** | 7 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### Passive - LevelBasedDamage

Increases damage based on player level

**Damagebonus:**
- base: `1.0`
- perStack: `1.0`
- formula: `amount * 1.0 (100% per stack, scales with level)`

## Internal Fields

| Field | Value |
|-------|-------|
| maxDamagePerAmount | 1.0 |
| updateCooldown | 1.0 |

## Implementation Details

- **Constructor RVA:** `0x443E60`
- **Oninitoramountchanged RVA:** `0x43C210`
- **Tick RVA:** `0x443C50`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
