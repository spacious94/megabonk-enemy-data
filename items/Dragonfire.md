# Dragonfire

> Chance to ignite enemies on hit

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 22 |
| **Internal Name** | Dragonfire |
| **Class Name** | ItemDragonfire |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **Price** | 10 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - BurnProc

Chance to ignite enemies on hit

**Procchance:**
- baseValue: `0.15`
- scaling: `linear`
- formula: `amount * 0.15`

**Burnchance:**
- baseValue: `0.15`
- scaling: `linear`
- formula: `amount * 0.15`

## Internal Fields

| Field | Value |
|-------|-------|
| procChancePerAmount | 0.15 |
| burnChancePerAmount | 0.15 |

## Implementation Details

- **Constructor RVA:** `0x45BD00`
- **Oninitoramountchanged RVA:** `0x45B9F0`
- **Proconhiteffects RVA:** `0x45BA20`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
