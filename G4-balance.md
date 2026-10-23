# G4 Balance Numbers – Original God-Simulation Design

*Deterministic design inspired by WorldBox-style simulation but fully original numbers. 10 ticks/sec, 1 day = 600 ticks, 1 year = 2 days (1200 ticks). Map 192×192, zones 8×8. Caps: 3000 units / 1000 animals / 4000 buildings / 32 kingdoms.*

## 1. Life per Race

| Race | Adult Age (yr) | Elder Age (yr) | Lifespan Range (yr) | Birth Cooldown (days) | Max Children / Couple | Food/Day Adult | Food/Day Child | Days Starve to Death | Reason |
|------|----------------|----------------|---------------------|-----------------------|-----------------------|----------------|----------------|----------------------|--------|
| Human | 16 | 50 | 55–75 | 8 | 6 | 2 | 1 | 12 | Balanced baseline; steady growth without exploding |
| Elf | 25 | 90 | 120–180 | 20 | 3 | 1 | 1 | 18 | Long life + slow breeding keeps forests stable and populations low |
| Dwarf | 18 | 60 | 70–100 | 12 | 4 | 3 | 2 | 14 | Strong body needs more food; moderate breeding fits mining focus |
| Orc | 12 | 35 | 40–55 | 5 | 8 | 3 | 2 | 8 | Fast breeding + short life creates aggressive pressure and rapid turnover |

## 2. Economy

| Job / Resource | Yield | Work Time (ticks) | Regrowth (days) | Reason |
|----------------|-------|-------------------|-----------------|--------|
| Berries (wild) | 3 | 40 | 4 | Quick early food so new cities survive the first years |
| Farm field | 8 | 180 | 6 | Main mid-game food; requires work investment |
| Fishing | 5 | 90 | — | Reliable water food without land pressure |
| Hunting | 6 | 120 | — | Meat for orcs/dwarves; riskier but high yield |
| Wood | 4 | 70 | 12 (tree) | Core building material; trees regrow slowly enough to matter |
| Stone | 3 | 110 | — | Mid-tier construction; mining is slower than wood |
| Iron | 2 | 200 | — | Late material; scarce to keep top tiers rare |
| Gold | 1 | 280 | — | Luxury / top buildings only; forces trade or long mining |
| Granary storage | 400 | — | — | Enough for ~200 adults for several days |
| Town Hall T1 storage | 150 | — | — | Early shared stock |
| Town Hall T2 storage | 350 | — | — | Mid growth |
| Town Hall T3 storage | 700 | — | — | Late empire buffer |

## 3. Buildings

| Building | Wood | Stone | Iron | Gold | Build Work (ticks) | Housing / Effect | Reason |
|----------|------|-------|------|------|--------------------|------------------|--------|
| Tent | 2 | 0 | 0 | 0 | 80 | House 2 | Instant early shelter |
| House T1 | 6 | 0 | 0 | 0 | 200 | House 3 | First permanent home |
| House T2 | 8 | 4 | 0 | 0 | 350 | House 4 | Stone appears |
| House T3 | 10 | 8 | 2 | 0 | 550 | House 5 | Iron for top housing |
| Town Hall T1 | 12 | 6 | 0 | 0 | 400 | +2 max houses, storage 150 | Core of any city |
| Town Hall T2 | 18 | 15 | 2 | 0 | 700 | +3 max houses, storage 350 | Mid expansion |
| Town Hall T3 | 25 | 30 | 5 | 2 | 1100 | +4 max houses, storage 700 | Late prestige |
| Granary | 10 | 5 | 0 | 0 | 300 | Storage 400 | Food security |
| Farm field | 1 | 0 | 0 | 0 | 120 | +food production | Cheap food engine |
| Windmill | 8 | 4 | 1 | 0 | 450 | +30% farm yield | Multiplier for farms |
| Lumber mill | 6 | 3 | 0 | 0 | 280 | +wood yield | Speeds timber |
| Mine | 8 | 6 | 0 | 0 | 400 | Unlocks stone/iron/gold | Resource gate |
| Dock | 10 | 2 | 0 | 0 | 320 | Enables boats | Coastal growth |
| Blacksmith | 12 | 8 | 3 | 0 | 500 | Equipment tiers | Combat upgrade |
| Barracks | 15 | 10 | 2 | 0 | 600 | Warrior training | Army core |
| Watchtower | 8 | 6 | 1 | 0 | 350 | Vision + defense | Border security |
| Temple | 10 | 12 | 2 | 1 | 650 | Loyalty + happiness | Soft power |
| Wall segment | 3 | 5 | 0 | 0 | 150 | Defense | Cheap fortification |
| Boat | 12 | 0 | 1 | 0 | 400 | Transport / trade | Expansion tool |

*Tier rule followed: wood early → stone mid → iron/gold only top.*

## 4. City Growth

| Rule | Value | Reason |
|------|-------|--------|
| Max houses per zone | 4 | Keeps density reasonable on 8×8 |
| Claim new zone when | Pop ≥ 18 and stock ≥ 40 food + 20 wood | Prevents early sprawl; forces resource buffer |
| Town Hall T1 → T2 | Pop ≥ 35 and 1 granary | Natural mid-game upgrade |
| Town Hall T2 → T3 | Pop ≥ 70 and iron ≥ 5 | Late-game only |
| Settlers leave to found new city | Pop ≥ 45, distance ≥ 24 tiles, stock surplus | Creates natural colonies without instant spam |
| Max cities by kingdom age | Age 0–20: 3; 21–50: 6; 51+: 10 | Prevents early empire blobs; allows later growth |

## 5. Combat per Race

| Race | Health | Attack | Defense | Speed (tiles/s) | Attack CD (ticks) | Sight | Reason |
|------|--------|--------|---------|-----------------|-------------------|-------|--------|
| Human | 100 | 12 | 6 | 1.4 | 40 | 8 | Balanced baseline |
| Elf | 80 | 14 | 4 | 1.7 | 35 | 10 | Fast accurate skirmishers |
| Dwarf | 140 | 15 | 12 | 1.0 | 45 | 6 | Tanky slow melee |
| Orc | 110 | 16 | 5 | 1.5 | 30 | 7 | Aggressive high damage |

**Equipment bonuses (additive)**  
| Tier | Atk | Def | Reason |
|------|-----|-----|--------|
| None | 0 | 0 | Baseline |
| Wood | +3 | +2 | Early |
| Stone | +6 | +5 | Mid |
| Iron | +10 | +9 | Strong |
| Gold | +14 | +12 | Rare end-game |

**Trait modifiers (%)**  
| Trait | Effect | Reason |
|-------|--------|--------|
| strong | +25% Atk/Def | Clear power fantasy |
| weak | –25% Atk/Def | Opposite |
| fast | +20% Speed, –10% CD | Mobility |
| slow | –20% Speed, +15% CD | Opposite |
| brave | +15% Atk, ignore fear | Charge |
| coward | –20% Atk, flee earlier | Avoid |
| giant | +40% HP, –15% Speed | Size trade-off |
| tiny | –30% HP, +25% Speed | Opposite |
| bloodlust | +30% Atk, –20% Def | Glass cannon aggression |
| peaceful | –40% Atk, never initiate | Pure defense |

## 6. Armies

| Rule | Value | Reason |
|------|-------|--------|
| Warriors in peace | 12% of adults | Enough to police, not drain economy |
| Warriors in war | 35% of adults | Real mobilization without emptying cities |
| Gather time before march | 180 ticks (18 s) | Visible preparation, not instant |
| Siege capture | Defenders ≤ 15% of original garrison → capture | Clear, deterministic, no endless stalemate |
| Retreat rule | Retreat only if army HP < 25% **and** no progress for 40 s | Prevents the hated “army sits forever and never captures” |

## 7. Diplomacy

| Modifier | Value | Reason |
|----------|-------|--------|
| Shared border | –15 | Friction |
| Distance > 60 tiles | +10 | Isolation reduces hate |
| Same race | +20 | Kinship |
| Human–Elf | +5 | Mild positive |
| Human–Dwarf | +8 | Trade friendly |
| Human–Orc | –12 | Cultural clash |
| Elf–Dwarf | –8 | Forest vs mountain |
| Elf–Orc | –20 | Strong dislike |
| Dwarf–Orc | –15 | Aggressive conflict |
| King ambitious | –10 to all | Warmonger |
| King kind | +12 to all | Diplomat |
| Recent war | –40, decays 8 per year | Memory of conflict |
| Alliance | +30 | Strong bond |
| Active trade | +10 | Soft power |
| War threshold | Opinion ≤ –25 | Clear trigger |
| Peace after | 4 years **or** 35% total losses | Avoids endless wars |
| Max alliance size | 4 kingdoms | Stops snowball |

## 8. Loyalty & Rebellion

| Modifier | Value | Reason |
|----------|-------|--------|
| Distance to capital (per 20 tiles) | –6 | Distant cities feel neglected |
| Happiness high | +15 | Content people stay |
| Happiness low | –20 | Unhappy people leave |
| Leader ambitious | –10 | Wants own crown |
| Leader loyal | +18 | Holds the realm |
| Kingdom size > 6 cities | –8 | Overextension |
| Rebellion conditions | Kingdom age ≥ 15 yr, non-capital, loyalty < 0, ≥ 12 warriors | Matches design goal; capital never rebels |

## 9. Animals

| Rule | Value | Reason |
|------|-------|--------|
| Herbivore herd size | 4–12 | Visible groups |
| Predator pack size | 2–5 | Threat without wipeout |
| Breeding cooldown | 15–25 days | Slow natural recovery |
| Predator hunger | Must kill every 8 days or lose HP | Forces hunting pressure |
| Max animals on 192×192 | 1000 | Hard cap |

## 10. Disasters

| Disaster | Radius / Chance | Damage / Effect | Reason |
|----------|-----------------|-----------------|--------|
| Lightning | 1 tile | 40 HP + fire chance 30% | Precise god strike |
| Fire spread | 18% per tick to adjacent flammable | Controllable blaze |
| Earthquake | 12-tile radius | 25% building damage, 15 HP units | Area shake |
| Meteor | 8-tile radius | 80 HP + crater | Dramatic but rare |
| Volcano | 20-tile lava flow | Continuous burn | Long-term hazard |
| Plague | 12% infection chance / day | 8-day duration, 25% death | Population control without total wipe |

## Design Goals Check
- 1–3 starting races → 4–10 kingdoms in ~100 years: achieved by settler thresholds + max-cities-by-age.
- War every 10–20 years: opinion thresholds + ambitious kings + border friction.
- Population 800–3000: food yields + starve timers + race breeding rates keep it in band.
- No calm golden age > 30 years: rebellions, disasters, opinion decay, and overextension penalties force events.

## 5 Main Stabilizing Feedback Loops

1. **Food ↔ Population**  
   More people need more food → farms/hunting expand → surplus allows new houses/cities → more mouths → pressure returns. Starvation kills excess fast.

2. **Expansion ↔ Overextension**  
   Claiming zones and founding cities raises power but drops loyalty with distance and size → rebellion risk rises → kingdoms split → map stays fragmented.

3. **War ↔ Recovery**  
   Border friction + ambitious kings start wars every 10–20 years → losses and opinion decay force peace after 4 years or heavy casualties → recovery period → next tension builds.

4. **Resources ↔ Technology Tiers**  
   Early wood buildings are cheap; stone/iron/gold require mines and time → only successful mid/late cities reach top tiers → inequality creates targets for war or rebellion.

5. **Disasters + Traits ↔ Stability**  
   Occasional lightning/fire/plague/meteor prune populations and destroy buildings → happiness and loyalty swing → trait distribution (brave/coward, strong/weak) changes combat outcomes → no kingdom stays static forever.

These five loops keep the simulation dynamic within the hard caps while producing the desired 100-year story arc.
