# Eagle Claw

> Chance to knock enemies up and deal bonus damage

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 39 |
| **Internal Name** | EagleClaw |
| **Class Name** | ItemEagleClaw |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **Price** | 7 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnHit - KnockupProc

Chance to knock enemies up and deal bonus damage

**Procchance:**
- baseValue: `0.08`
- scaling: `linear`
- formula: `amount * 0.08`

**Bonusdamage:**
- base: `0.66`
- perStack: `0.66`
- formula: `0.66 + (amount - 1) * 0.66`

## Internal Fields

| Field | Value |
|-------|-------|
| procChancePerAmount | 0.08 |
| damageAddition | 0.66 |
| damageAdditionPerAmount | 0.66 |
| knockupForce | 3.5 |

## Implementation Details

- **Constructor RVA:** `0x45C430`
- **Oninitoramountchanged RVA:** `0x45C2F0`
- **Preattack RVA:** `0x45C330`
- **Proconhiteffects RVA:** `0x45C3A0`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** Yes
