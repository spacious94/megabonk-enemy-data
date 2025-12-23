# Megabonk Enemy Data

Extracted enemy statistics from the game **Megabonk**.

## Files

- `all_enemies.json` - All enemies in a single file, sorted by HP
- `enemies/` - Individual JSON files for each enemy

## Data Structure

Each enemy has the following structure:

```json
{
  "name": "Skeleton",
  "enemyId": 0,
  "stats": {
    "hp": 20,
    "damage": 20,
    "shield": 0,
    "isPoison": false,
    "knockbackResistance": 0.0,
    "nukeProtection": false
  },
  "movement": {
    "mass": 40.0,
    "speed": 5.5,
    "isFlying": false,
    "teleportCooldown": 10.0,
    "isRunningFromPlayer": false,
    "minStayAtDistance": 0.0,
    "maxStayAtDistance": 0.0
  },
  "other": {
    "xp": 1,
    "despawnTime": 0.0,
    "canBeElite": true,
    "canBeExecuted": true,
    "maxSuckTime": 15.0
  },
  "spawning": {
    "maps": 9,
    "minStage": 0,
    "creditCost": 1.0,
    "canSpawnAfterTime": 0.0
  },
  "rendering": {
    "scale": 1.25,
    "colliderRadius": 1.25
  }
}
```

## Field Descriptions

### Stats
| Field | Type | Description |
|-------|------|-------------|
| `hp` | int | Base health points |
| `damage` | int | Base damage dealt on contact |
| `shield` | int | Damage reduction/armor |
| `isPoison` | bool | Deals poison damage |
| `knockbackResistance` | float | Resistance to knockback effects |
| `nukeProtection` | bool | Immune to nuke/instakill effects |

### Movement
| Field | Type | Description |
|-------|------|-------------|
| `mass` | float | Physics mass |
| `speed` | float | Movement speed |
| `isFlying` | bool | Can fly/hover |
| `teleportCooldown` | float | Seconds between teleports |
| `isRunningFromPlayer` | bool | Flees from player |
| `minStayAtDistance` | float | Minimum distance to maintain from player |
| `maxStayAtDistance` | float | Maximum distance to maintain from player |

### Other
| Field | Type | Description |
|-------|------|-------------|
| `xp` | int | Experience reward on kill |
| `despawnTime` | float | Time before despawn (0 = never) |
| `canBeElite` | bool | Can spawn as elite variant |
| `canBeExecuted` | bool | Can be executed/finished |
| `maxSuckTime` | float | Max time for vacuum/suction abilities |

### Spawning
| Field | Type | Description |
|-------|------|-------------|
| `maps` | int | Bitmask of maps where enemy can spawn |
| `minStage` | int | Minimum stage/wave to spawn |
| `creditCost` | float | Spawn cost in wave budget |
| `canSpawnAfterTime` | float | Seconds into run before can spawn |

## Enemy Summary

| Enemy | HP | Damage | Speed | Flying | Elite |
|-------|-----|--------|-------|--------|-------|
| Slime | 6 | 8 | 5.0 | No | Yes |
| GoblinWeak | 7 | 15 | 5.5 | No | Yes |
| Tumblebone | 7 | 9 | 8.0 | No | Yes |
| Mummy | 8 | 13 | 5.0 | No | Yes |
| Wisp | 8 | 13 | 6.0 | No | Yes |
| Ghoul | 9 | 12 | 7.5 | No | Yes |
| Bee | 10 | 15 | 10.0 | Yes | Yes |
| Ghost | 10 | 10 | 7.0 | Yes | Yes |
| Bush | 10000 | 45 | 0.0 | No | No |
| Head | 12 | 8 | 8.0 | No | Yes |
| Zombie | 12 | 20 | 4.5 | No | Yes |
| CactusShooter | 15 | 30 | 0.0 | No | Yes |
| GoblinStrong | 15 | 25 | 5.5 | No | Yes |
| Scorpion | 16 | 20 | 6.5 | No | Yes |
| SkeletonDusty | 16 | 22 | 5.0 | No | Yes |
| BoomerSpider | 18 | 30 | 8.0 | No | Yes |
| Golem | 20 | 20 | 4.0 | No | Yes |
| GhostGreater | 20 | 13 | 7.0 | Yes | Yes |
| Skeleton | 20 | 20 | 5.5 | No | Yes |
| SkeletonArmoredDusty | 25 | 16 | 4.5 | No | Yes |
| ScorpionBig | 30 | 30 | 5.5 | No | Yes |
| SkeletonArmored | 30 | 25 | 5.0 | No | Yes |
| GhostPurple | 40 | 20 | 8.0 | Yes | Yes |
| GoblinTank | 40 | 30 | 4.0 | No | Yes |
| MummyTank | 45 | 30 | 4.0 | No | Yes |
| SkeletonGold | 50 | 25 | 7.0 | No | Yes |
| SkeletonXp | 50 | 25 | 7.0 | No | Yes |
| MummyAncient | 70 | 40 | 5.0 | No | Yes |
| GhostRed | 100 | 30 | 10.0 | Yes | Yes |
| Miniboss_Desert_Golem | 250 | 40 | 5.0 | No | No |
| Miniboss_Golem | 250 | 40 | 4.0 | No | No |
| Miniboss_Pig | 250 | 40 | 6.0 | No | No |
| Miniboss_Scorpion | 250 | 35 | 5.5 | No | No |
| Miniboss_Ghostham | 320 | 45 | 6.5 | Yes | No |
| Miniboss_SkeletonKing | 320 | 40 | 5.5 | No | No |
| GhostGrave1 | 1100 | 20 | 7.0 | Yes | No |
| GhostGrave2 | 2250 | 25 | 7.0 | Yes | No |
| GhostGrave3 | 5500 | 30 | 7.0 | Yes | No |
| EntStage2 | 8000 | 40 | 0.0 | No | No |
| Pharaoh1 | 8000 | 40 | 5.0 | No | No |
| Pharaoh2 | 8000 | 40 | 5.0 | No | No |
| Pharaoh3 | 8000 | 40 | 5.0 | No | No |
| EntStage1 | 9000 | 40 | 0.0 | No | No |
| GhostGrave4 | 9000 | 35 | 7.0 | Yes | No |
| EntStage3 | 10000 | 22 | 0.0 | No | No |
| Bandit | 11000 | 50 | 7.0 | No | No |
| GhostKingData | 500000 | 40 | 4.0 | Yes | No |
| GhostInvincible | 2147483647 | 2147483647 | 0.0 | Yes | No |

## License

This data is for educational/research purposes. Megabonk is property of its respective developers.
