# Megabonk Game Data

Extracted game statistics from **Megabonk**.

## Files

### Enemies
- `all_enemies.json` - All 48 enemies in a single file, sorted by HP
- `enemies/` - Individual JSON files for each enemy

### Weapons
- `all_weapons.json` - All 30 weapons in a single file, sorted by damage
- `weapons/` - Individual JSON files for each weapon

### Items
- `all_items.json` - All 86 items in a single file, sorted by item ID
- `items/` - Individual JSON files for each item

---

## Enemy Data Structure

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

### Enemy Field Descriptions

| Field | Type | Description |
|-------|------|-------------|
| `hp` | int | Base health points |
| `damage` | int | Base damage dealt on contact |
| `shield` | int | Damage reduction/armor |
| `isPoison` | bool | Deals poison damage |
| `knockbackResistance` | float | Resistance to knockback effects |
| `nukeProtection` | bool | Immune to nuke/instakill effects |
| `speed` | float | Movement speed |
| `isFlying` | bool | Can fly/hover |
| `xp` | int | Experience reward on kill |
| `canBeElite` | bool | Can spawn as elite variant |
| `creditCost` | float | Spawn cost in wave budget |
| `isBoss` | bool | (Boss enemies only) Marked as boss at spawn time |

### Boss Flag Note

Some enemies are flagged as **bosses at spawn time** using the game's `EEnemyFlag` system (Boss, StageBoss, FinalBoss, etc.). This runtime flag **prevents execution** regardless of what the `canBeExecuted` field says in the data.

Boss enemies have `"isBoss": true` in their data files. These include:
- **Minibosses**: Miniboss_Pig, Miniboss_Golem, Miniboss_Desert_Golem, Miniboss_Scorpion, Miniboss_Ghostham, Miniboss_SkeletonKing
- **Stage Bosses**: Pharaoh1, Pharaoh2, Pharaoh3, EntStage1, EntStage2, EntStage3
- **Special Bosses**: GhostKing, Bandit, Bush

---

## Weapon Data Structure

```json
{
  "name": "Sword",
  "weaponId": 2,
  "combat": {
    "damage": 11.0,
    "knockback": 2.0,
    "critChance": 0.0,
    "element": "Physical",
    "elementId": 0,
    "procCoefficient": 0.8
  },
  "projectile": {
    "count": 1,
    "bounces": 0,
    "speed": 1.0,
    "canBounce": false
  },
  "timing": {
    "attackDuration": 0.5,
    "maxDuration": 0.5,
    "effectDuration": 1.5,
    "cooldown": 0.75,
    "burstTime": 0.5,
    "minBurstInterval": 0.1
  },
  "behavior": {
    "amplificationMode": "Normal",
    "useVision": true,
    "canMultiHit": true,
    "hasCrosshair": false,
    "isAura": false,
    "onlySpawnWhenCloseEnemies": false,
    "maxSizeMultiplier": -1.0
  }
}
```

### Weapon Field Descriptions

| Field | Type | Description |
|-------|------|-------------|
| `damage` | float | Base damage per hit |
| `knockback` | float | Knockback force |
| `critChance` | float | Base critical hit chance (0.0-1.0) |
| `element` | string | Damage type (Neutral, Lightning, Ice, Fire, Bleed) |
| `procCoefficient` | float | Multiplier for on-hit effects |
| `projectile.count` | int | Number of projectiles per attack |
| `projectile.bounces` | int | Times projectiles can bounce |
| `cooldown` | float | Time between attacks |
| `isAura` | bool | Constant damage aura weapon |
| `canMultiHit` | bool | Can hit same enemy multiple times |

---

## Weapon Summary

| Weapon | Damage | Knockback | Element | Cooldown | Projectiles |
|--------|--------|-----------|---------|----------|-------------|
| Sniper | 22 | 4.0 | Neutral | 1.0 | 1 |
| DragonsBreath | 16 | 0.5 | Fire | 0.6 | 1 |
| Shotgun | 14 | 2.0 | Neutral | 0.9 | 6 |
| Chunkers | 12 | 2.5 | Neutral | 1.0 | 1 |
| CorruptedSword | 12 | 2.0 | Neutral | 0.7 | 1 |
| HeroSword | 11 | 2.0 | Neutral | 0.7 | 1 |
| Bone | 11 | 1.25 | Neutral | 0.75 | 1 |
| Sword | 11 | 2.0 | Neutral | 0.75 | 1 |
| Aegis | 10 | 3.0 | Neutral | 1.2 | 1 |
| FireStaff | 10 | 1.0 | Fire | 0.6 | 1 |
| Katana | 10 | 1.5 | Neutral | 0.65 | 1 |
| Bananarang | 9 | 1.0 | Neutral | 0.65 | 1 |
| BloodMagic | 9 | 1.0 | Neutral | 0.8 | 1 |
| Bow | 9 | 0.5 | Neutral | 0.45 | 1 |
| Dexecutioner | 9 | 1.0 | Neutral | 0.6 | 1 |
| FrostWalker | 9 | 0.5 | Ice | 0.6 | 1 |
| Scythe | 9 | 1.0 | Neutral | 0.5 | 1 |
| Revolver | 8 | 0.75 | Neutral | 0.5 | 1 |
| SpaceNoodle | 7 | 1.5 | Neutral | 0.7 | 1 |
| Axe | 6 | 1.0 | Neutral | 0.75 | 3 |
| Aura | 6 | 0.5 | Neutral | 1.0 | 1 |
| LightningBolt | 6 | 0.5 | Lightning | 0.6 | 1 |
| SluttyRocket | 6 | 3.0 | Neutral | 0.9 | 1 |
| Tornado | 6 | 0.5 | Neutral | 0.8 | 1 |
| FlameWalker | 5 | 0.0 | Fire | 0.6 | 1 |
| WirelessDagger | 5 | 0.5 | Lightning | 0.4 | 1 |
| BlackHole | 4.5 | 6.0 | Neutral | 1.0 | 1 |
| Mines | 3 | 5.0 | Neutral | 0.65 | 1 |
| PoisonFlask | 3 | 0.5 | Neutral | 0.6 | 1 |
| Dice | 0 | 2.5 | Neutral | 0.5 | 1 |

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
| Pharaoh1-3 | 8000 | 40 | 5.0 | No | No |
| EntStage1-3 | 8000-10000 | 22-40 | 0.0 | No | No |
| GhostGrave4 | 9000 | 35 | 7.0 | Yes | No |
| Bush | 10000 | 45 | 0.0 | No | No |
| Bandit | 11000 | 50 | 7.0 | No | No |
| GhostKing | 500000 | 40 | 4.0 | Yes | No |
| GhostInvincible | MAX_INT | MAX_INT | 0.0 | Yes | No |

---

## Item Data Structure

```json
{
  "name": "Clover",
  "itemId": 35,
  "internalName": "Clover",
  "rarity": "Common",
  "rarityId": 0,
  "maxAmount": 0,
  "price": 0,
  "inItemPool": true,
  "isEnabled": true,
  "showInUnlocks": true
}
```

### Item Field Descriptions

| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Display name |
| `itemId` | int | Internal item ID (EItem enum) |
| `internalName` | string | Code reference name |
| `rarity` | string | Common, Rare, Epic, Legendary, Corrupted, or Quest |
| `rarityId` | int | Rarity ID (0-5) |
| `maxAmount` | int | Stack limit (0 = unlimited) |
| `price` | int | Shop price |
| `inItemPool` | bool | Can appear in normal item pools |
| `isEnabled` | bool | Item is active in game |
| `showInUnlocks` | bool | Visible in unlocks menu |

## Item Summary

| Item | Rarity | Max Stack | Price | In Pool |
|------|--------|-----------|-------|---------|
| Battery | Common | Unlimited | 3 | Yes |
| Borgar | Common | Unlimited | 0 | Yes |
| Boss Buster | Common | Unlimited | 3 | Yes |
| Cactus | Common | Unlimited | 4 | Yes |
| Clover | Common | Unlimited | 0 | Yes |
| Cursed Doll | Common | Unlimited | 3 | Yes |
| ForbiddenJuice | Common | Unlimited | 3 | Yes |
| Ghost | Common | Unlimited | 4 | Yes |
| Golden Glove | Common | Unlimited | 0 | Yes |
| GymSauce | Common | Unlimited | 0 | Yes |
| IceCrystal | Common | Unlimited | 4 | Yes |
| Key | Common | Unlimited | 3 | Yes |
| Medkit | Common | Unlimited | 0 | Yes |
| Moldy Cheese | Common | Unlimited | 0 | Yes |
| Oats | Common | Unlimited | 0 | Yes |
| OldMask | Common | Unlimited | 4 | Yes |
| Skuleg | Common | Unlimited | 4 | Yes |
| Slippery Ring | Common | Unlimited | 0 | Yes |
| Tactical Glasses | Common | Unlimited | 3 | Yes |
| TimeBracelet | Common | Unlimited | 0 | Yes |
| Turbo Socks | Common | Unlimited | 3 | Yes |
| Wrench | Common | Unlimited | 0 | Yes |
| Backpack | Rare | Unlimited | 0 | Yes |
| Beacon | Rare | Unlimited | 0 | Yes |
| Beer | Rare | Unlimited | 0 | Yes |
| BrassKnuckles | Rare | Unlimited | 5 | Yes |
| Campfire | Rare | Unlimited | 0 | Yes |
| Cowards Cloak | Rare | Unlimited | 0 | Yes |
| CreditCardRed | Rare | Unlimited | 0 | Yes |
| Demon Blade | Rare | Unlimited | 5 | Yes |
| Demonic Blood | Rare | Unlimited | 5 | Yes |
| Echo Shard | Rare | Unlimited | 5 | Yes |
| Electric Plug | Rare | Unlimited | 0 | Yes |
| Flappy Feathers | Rare | Unlimited | 0 | Yes |
| Glove Lightning | Rare | Unlimited | 0 | Yes |
| Glove Poison | Rare | Unlimited | 5 | Yes |
| Golden Shield | Rare | Unlimited | 0 | Yes |
| Golden Sneakers | Rare | Unlimited | 5 | Yes |
| IdleJuice | Rare | Unlimited | 6 | Yes |
| Kevin | Rare | Unlimited | 8 | Yes |
| Leeching Crystal | Rare | Unlimited | 7 | Yes |
| PhantomShroud | Rare | Unlimited | 0 | Yes |
| Pumpkin | Rare | Unlimited | 9 | Yes |
| UnstableTransfusion | Rare | Unlimited | 0 | Yes |
| Beefy Ring | Epic | Unlimited | 0 | Yes |
| Bob Dead | Epic | Unlimited | 7 | Yes |
| Bobs Lantern | Epic | Unlimited | 9 | Yes |
| CreditCardGreen | Epic | Unlimited | 0 | Yes |
| Demonic Soul | Epic | Unlimited | 7 | Yes |
| Eagle Claw | Epic | Unlimited | 7 | Yes |
| Gamer Goggles | Epic | Unlimited | 7 | Yes |
| Gas Mask | Epic | Unlimited | 7 | Yes |
| Gloves Bloody | Epic | Unlimited | 0 | Yes |
| Gloves Cursed | Epic | Unlimited | 8 | Yes |
| Grandma's Secret Tonic | Epic | Unlimited | 7 | Yes |
| Mirror | Epic | Unlimited | 0 | Yes |
| Quins Mask | Epic | Unlimited | 7 | Yes |
| Scarf | Epic | Unlimited | 0 | Yes |
| Shattered Knowledge | Epic | Unlimited | 7 | Yes |
| Slutty Cannon | Epic | Unlimited | 7 | Yes |
| Spiky Shield | Epic | Unlimited | 0 | Yes |
| ToxicBarrel | Epic | Unlimited | 7 | Yes |
| Turbo Skates | Epic | Unlimited | 7 | Yes |
| Anvil | Legendary | 1 | 12 | Yes |
| Bloody Cleaver | Legendary | Unlimited | 15 | Yes |
| Bonker | Legendary | Unlimited | 0 | Yes |
| Chonkplate | Legendary | Unlimited | 10 | Yes |
| Dragonfire | Legendary | Unlimited | 10 | Yes |
| Energy Core | Legendary | Unlimited | 11 | Yes |
| Giant Fork | Legendary | Unlimited | 0 | Yes |
| Gloves Power | Legendary | Unlimited | 0 | Yes |
| Golden Ring | Legendary | Unlimited | 0 | No |
| Holy Book | Legendary | Unlimited | 10 | Yes |
| Ice Cube | Legendary | Unlimited | 0 | Yes |
| Joe's Dagger | Legendary | 10 | 14 | Yes |
| Lightning Orb | Legendary | Unlimited | 10 | Yes |
| Overpowered Lamp | Legendary | 2 | 0 | Yes |
| PotSteel | Legendary | Unlimited | 21 | Yes |
| Snek | Legendary | Unlimited | 20 | Yes |
| SoulHarvester | Legendary | Unlimited | 13 | Yes |
| Speed Boi | Legendary | Unlimited | 10 | Yes |
| Spicy Meatball | Legendary | Unlimited | 0 | Yes |
| Sucky Magnet | Legendary | Unlimited | 10 | Yes |
| Za Warudo | Legendary | Unlimited | 0 | Yes |
| CageKeyMonke | Quest | Unlimited | 0 | Yes |
| CryptKey | Quest | Unlimited | 0 | Yes |

## License

This data is for educational/research purposes. Megabonk is property of its respective developers.
