# Cowards Cloak

> When hit, gain temporary speed stacks

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 5 |
| **Internal Name** | CowardsCloak |
| **Class Name** | ItemCowardsCloak |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| MoveSpeedMultiplier | Flat | +5.0% per stack | Linear |

## Special Effects

### OnDamageTaken - TemporarySpeedBuff

When hit, gain temporary speed stacks

**Stacksgained:**
- perItem: `2`
- formula: `amount * 2`

## Internal Fields

| Field | Value |
|-------|-------|
| speedPerAmount | 0.05 |
| speedPerStack | 0.3 |
| maxStacks | 2 |
| stacksPerAmount | 2 |

## Implementation Details

- **Constructor RVA:** `0x455B00`
- **Init RVA:** `0x4558E0`
- **Cleanup RVA:** `0x4558A0`
- **Ondamage RVA:** `0x455A70`
- **Oninitoramountchanged RVA:** `0x455AB0`
- **Tick RVA:** `0x455BA0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
