# Soul Harvester

> When enemies die, spawn homing soul projectiles

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 47 |
| **Internal Name** | SoulHarvester |
| **Class Name** | ItemSoulHarvester |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **Price** | 13 |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnEnemyDeath - SpawnSoulProjectile

When enemies die, spawn homing soul projectiles

## Internal Fields

| Field | Value |
|-------|-------|
| numProjectiles | 2 |
| range | 50.0 |

## Implementation Details

- **Constructor RVA:** `0x4B7080`
- **Init RVA:** `0x4B6520`
- **Cleanup RVA:** `0x4B6430`
- **Onenemydied RVA:** `0x4B6590`
- **Spawnprojectile RVA:** `0x4B6830`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
