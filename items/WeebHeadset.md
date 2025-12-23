# Weeb Headset

> Chance to charm enemies on hit

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 50 |
| **Internal Name** | WeebHeadset |
| **Class Name** | ItemWeebHeadset |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **Price** | 5 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - CharmEnemy

Chance to charm enemies on hit

**Charmchance:**
- base: `0.02`
- perStack: `0.02`
- formula: `amount * 0.02`

**Charmduration:**
- base: `1.5`
- perStack: `1.5`
- formula: `amount * 1.5`

## Internal Fields

| Field | Value |
|-------|-------|
| charmChancePerAmount | 0.02 |
| durationPerAmount | 1.5 |
| maxProcsPerTick | 100 |

## Implementation Details

- **Constructor RVA:** `0x45D6E0`
- **Oninitoramountchanged RVA:** `0x45D5D0`
- **Proconhiteffects RVA:** `0x45D640`
- **Tick RVA:** `0x45D6D0`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No
