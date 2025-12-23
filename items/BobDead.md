# Bob Dead

> Spawns ghost projectiles as you move

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 46 |
| **Internal Name** | BobDead |
| **Class Name** | ItemBobDead |
| **Rarity** | Epic |
| **Max Stacks** | Unlimited |
| **Price** | 7 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnMove - SpawnGhostProjectiles

Spawns ghost projectiles as you move

## Internal Fields

| Field | Value |
|-------|-------|
| unitsPerProjectile | 14.0 |
| minSpawnTime | 0.05 |
| maxGhosts | 80 |

## Implementation Details

- **Constructor RVA:** `0x43AA40`
- **Oninitoramountchanged RVA:** `0x43A5C0`
- **Tick RVA:** `0x43A750`
- **Spawnghost RVA:** `0x43A650`
- **Getdamage RVA:** `0x43A450`
- **Getduration RVA:** `0x43A4C0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
