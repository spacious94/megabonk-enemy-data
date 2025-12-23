# Backpack

> Increases your weapon's projectile count.

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 34 |
| **Internal Name** | Backpack |
| **Class Name** | ItemBackpack |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

| Stat | Type | Value | Scaling |
|------|------|-------|---------|
| Projectiles | Flat | +1 per stack | Linear |

## Formula

```
Total Projectiles Bonus = stacks × 1
```

**Example:**
- 1 stack: +1 projectile
- 3 stacks: +3 projectiles
- 5 stacks: +5 projectiles

## Implementation Details

- **Constructor RVA:** `0x438E60`
- **OnInitOrAmountChanged RVA:** `0x438DE0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No

### Internal Fields

| Field | Type | Default Value |
|-------|------|---------------|
| projectilesPerAmount | int | 1 |

## Technical Notes

- Projectiles stat is added as a **Flat** modifier, meaning it adds directly to the base projectile count
- Each weapon fires (base projectiles + bonus) projectiles per attack
- Stacks linearly with no diminishing returns

## Related Items

- **Echo Shard** - Also adds projectiles with different mechanics
