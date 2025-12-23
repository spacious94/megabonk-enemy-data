# Electric Plug

> When hit, zap nearby enemies with lightning

## Overview

| Property | Value |
|----------|-------|
| **Item ID** | 45 |
| **Internal Name** | ElectricPlug |
| **Class Name** | ItemElectricPlug |
| **Rarity** | Rare |
| **Max Stacks** | Unlimited |
| **In Item Pool** | Yes |

## Stat Modifiers

This item does not provide passive stat bonuses.

## Special Effects

### OnPlayerHit - LightningRetaliation

When hit, zap nearby enemies with lightning

**Radius:**
- base: `13.0`
- perStack: `4.0`
- formula: `13 + (amount - 1) * 4`

**Targets:**
- base: `15`
- perStack: `5`
- formula: `15 + (amount - 1) * 5`

## Internal Fields

| Field | Value |
|-------|-------|
| radius | 13.0 |
| radiusPerAmount | 4.0 |
| targets | 15 |
| targetsPerAmount | 5 |

## Implementation Details

- **Constructor RVA:** `0x460320`
- **Init RVA:** `0x460030`
- **Cleanup RVA:** `0x45FEE0`
- **Onplayerhit RVA:** `0x4600E0`
- **Has On-Hit Proc:** No
- **Has Pre-Attack Proc:** No
