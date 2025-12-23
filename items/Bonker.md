# Bonker

> A legendary hammer that unleashes devastating shockwaves on hit.

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 3 |
| **Internal Name** | Bonker |
| **Class Name** | ItemBonker |
| **Rarity** | Legendary |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### On Hit - Shockwave

When you hit an enemy, you have a chance to trigger a massive AOE shockwave.

| Property | Base Value | Per Stack | Formula |
|----------|------------|-----------|---------|
| **Proc Chance** | 2% | +1.5% | `0.02 + (stacks - 1) * 0.015` |
| **Damage Multiplier** | 2000% | +1000% | `baseDamage * (20 + (stacks - 1) * 10)` |
| **Radius** | 6.0 | +1.0 | `min(6 + stacks, 10)` |
| **Max Radius** | 10.0 | - | Hard cap |
| **Max Procs/Tick** | 5 | - | Prevents infinite chains |

## Formulas

### Proc Chance
```
Chance = 0.02 + (stacks - 1) × 0.015
```

| Stacks | Proc Chance |
|--------|-------------|
| 1 | 2% |
| 2 | 3.5% |
| 3 | 5% |
| 5 | 8% |
| 10 | 15.5% |

### Damage Multiplier
```
Multiplier = 20 + (stacks - 1) × 10
Final Damage = Base Damage × Multiplier
```

| Stacks | Multiplier | With 100 Base Damage |
|--------|------------|---------------------|
| 1 | 2000% | 2,000 |
| 2 | 3000% | 3,000 |
| 3 | 4000% | 4,000 |
| 5 | 6000% | 6,000 |

### AOE Radius
```
Radius = min(6 + stacks × 1, 10)
```

| Stacks | Radius |
|--------|--------|
| 1 | 7.0 |
| 2 | 8.0 |
| 3 | 9.0 |
| 4+ | 10.0 (capped) |

## Implementation Details

- **Constructor RVA:** `0x43D360`
- **OnInitOrAmountChanged RVA:** `0x43CE00`
- **ProcOnHitEffects RVA:** `0x43CE70`
- **Tick RVA:** `0x43D350`
- **Has On-Hit Proc:** Yes
- **Has Pre-Attack Proc:** No

### Internal Fields

| Field | Type | Default Value |
|-------|------|---------------|
| baseChance | float | 0.02 |
| baseDamageMultiplier | float | 20.0 |
| chancePerStack | float | 0.015 |
| damageMultiplierPerStack | float | 10.0 |
| radiusPerStack | float | 1.0 |
| radius | float | 3.5 |
| maxRadius | float | 10.0 |
| maxProcsPerTick | int | 5 |

## Technical Notes

- Uses `ItemUtility.TryProc()` with proc coefficient for chance calculation
- Shockwave can chain to nearby enemies within the radius
- Maximum 5 procs per tick prevents infinite loops with multiple Bonkers
- Damage applies `damageEffect = 1` (visual/audio feedback)
- Knockback is multiplied by 1.25× for shockwave hits
- Creates a reusable DamageContainer for efficiency

## Synergies

- **High proc coefficient weapons** - More chances to trigger shockwaves
- **Multi-hit weapons** - Each hit can proc independently
- **Damage items** - Base damage affects shockwave damage

## Related Items

- **Echo Shard** - Another on-hit proc item
- **Lightning Orb** - Chain damage mechanic
