# WorldBox Deep Mechanics Summary (G5)

*Compiled from official wiki (the-official-worldbox-wiki.fandom.com), Reddit r/Worldbox, X, Steam reviews & patch notes (latest as of Oct 2026). Confirmed = direct from wiki/patch notes/reviews. Guessed/Inferred = community consensus or incomplete data.*

## 1. God Powers by Tab (what they actually do)

| Tab | Power examples | Actual in-game effect | Source |
|-----|----------------|-----------------------|--------|
| **Main** (15) | Pause/Resume, Hourglass, World Laws, Ages, Statistics, Eye of Insight, History, Achievements, Settings, Hide UI, Steam Workshop | Control time, toggle laws/ages, view stats/history, unlocks | Wiki Powers page [confirmed] |
| **World Shaping** (47) | Deep/Close Ocean, Sand, Soils, Hills, Mountains, Summit, Walls (stone/evil/ancient/wood/green/iron/light), Shovels, Finger, Vortex, Sponge, Sickle, Bucket, Pickaxe, Spade, Axe, Demolish, Life Eraser, Scissors, Paint, Border Brush, Fuse, Fireworks, Printers (hexagon/skull/etc.) | Terraform terrain, place/remove resources, draw borders, pattern printers create landforms | Wiki [confirmed] |
| **Noosphere and Life** (61) | Village Info, Relations, Spite, Friendship, Inspiration, Whisper of War, Discord, Unity, layers (Kingdoms/Villages/Clans/Religions/Cultures/Languages/Families/Subspecies/Armies/Alliances/Wars), Favorites, arrows, money flow, bubbles | Inspect meta-objects, force diplomacy (war/peace/rebellion/alliance), show map layers & relations | Wiki [confirmed] |
| **Animals, Creatures and Monsters** (117+) | Humans, Orcs, Elves, Dwarves + all animals, mages, dragons, zombies, Greg, God Finger, etc. | Spawn specific creatures | Wiki Category:Creatures [confirmed] |
| **Nature and Disasters** | Temperature, Lightning, Rain, Acid, Earthquake, Tornado, Fire, Lava, all Biome Seeds, Ore/Gold/Stone, Geysers, Clouds (rain/acid/lava/life/blood) | Weather, disasters, grow biomes/resources, spawn clouds | Wiki + patch notes [confirmed] |
| **Destruction and Chaos** | TNT, Grenades, Bombs, Napalm, Antimatter, Atomic, Tsar Bomba, Meteorite, Heat-Ray, Infinity Coin, Grey Goo, Madness, Plague, Divine Light | Explosives destroy terrain/life, Tsar Bomba massive wipe, Madness makes units attack everything, Divine Light cures diseases & damages undead/evil, Infinity Coin kills half population | Wiki Category:Destructive + Divine Light/Madness pages [confirmed] |
| **Other various** | Blessing, trait rains (Gamma/Omega/Delta), Clone Rain, Smooth Jazz, Possession, etc. | Apply traits/status, clone, force birth, possess units | Wiki [confirmed] |

*Note: ~374 powers total. Exact full list is long; above are representative + functional groups. Many printers and seeds are individual powers.*

## 2. City Life Cycle

### Growth & Expansion (confirmed from Villages / City Building / Houses pages)
- Start: 3×3 zones (8×8 tiles) when founded by adult sapient with no nearby enemies + valid land.
- Leaders/kings claim more zones via “claim_land” task (stewardship priority). Expansionists culture or debug can claim up to 8 at once.
- Max houses ≈ number of zones (×2 Dense Dwellings, ×3 Hive Society, ÷3 Solitude Seekers). Extra from statues/wells/temples/dummies.
- One building under construction at a time. Stops if enemies/fire/capture in progress.

### When new cities form (confirmed)
- Inspiration power on non-capital village → becomes new kingdom.
- Rebellion plot success (see section 3) → new kingdom from rebel city(ies).
- Natural colony / expansion when kingdom has room & resources (inferred from max cities & available zones).

### Building Tiers & Costs (classic civs – confirmed from Buildings / Houses / Town Hall / Economy pages)

| Building | Tier / Notes | Resources (approx.) |
|----------|--------------|---------------------|
| Tent (T0) | Holds 3 | 1 wood |
| House T1 | Holds 3 | 5 wood |
| House T2 | Holds 4 | 4 wood |
| House T3 | — | 5 wood + gold |
| House T4 | — | 10 wood + gold |
| House T5 | — | 15 wood + gold |
| House T6 | — | 20 wood + 10 stone + 2 metal |
| Town Hall T1 | Holds 5, +2 max houses | 10 wood + 5 stone |
| Town Hall T2 | Holds 8 | 10 wood + 20 stone + 1 gold |
| Town Hall T3 | Holds 12 | 15 wood + 100 stone + 1 gold |
| Barracks | Max 1 | 5 wood + 15 stone + 2 metal |
| Temple | Max 1 | 10 wood + 30 stone + 2 metal |
| Library | — | 10 wood + 30 stone + 2 metal |
| Market | — | 10 wood + 5 stone + 100 gold + 2 metal |
| Watch Tower | Limited by factors | 20 wood + 5 stone + 1 gold |
| Windmill T1/T2 | Max 1 | T1: 5+5; T2: 5+30+5 |
| Dock T1/T2 | Max 5 | T1: 10 wood; T2: 10+6 |
| Mine | Max 1 | 15 wood |
| Statue / Well / Bonfire / Stockpile | Limits apply | Statue 5+25; Well 20+5+1; others free or low |

Non-classic sapients use simplified (mostly T1-equivalent) houses. Culture traits change density, layout, and build order.

## 3. War / Diplomacy System

### War Declaration (confirmed from War / Alliances / Rebellions wiki pages)
- **Natural**: King completes “War” / Conquest plot (opinion ≤0, expansion pressure, ambition traits).
- **Player forced**: Spite (target kingdom wars everyone), Whisper of War (force A vs B), Inspiration (non-capital becomes independent kingdom, often starts war).
- **Rebellion**: See below → can trigger Rebellion-type war.
- Alliances join if opinion >0 toward the side being attacked.

### Ending War (confirmed)
- Capture / destroy all enemy villages.
- Peace Talks plot success (or Friendship power).
- Player Discord / other diplomacy powers.
- Spite / Whisper wars cannot be ended by normal peace talks.

### Rebellion (confirmed)
**Requirements**:
- Diplomacy + Rebellions world laws ON.
- Kingdom ≥15 years old, >1 city (usually >6 or over max cities).
- Non-capital village with loyalty <0, ≥10 warriors, leader has high stewardship/warfare.
- No ongoing rebellion plot already.

**Result**: New kingdom formed, citizens transfer (+30 happiness if plot/Inspiration), Rebellion war starts vs old kingdom (allies with opinion >0 may join old kingdom). Multi-rebellions possible.

Capital has permanent high loyalty and almost never rebels.

## 4. Player Feedback (Steam reviews, r/Worldbox, X – 2025-2026)

### 10 most praised (confirmed from reviews)
1. Pure sandbox freedom – do anything as god (Steam 96% positive overall).
2. Emergent storytelling & watching civilizations rise/fall.
3. Constant free updates adding depth (clans, ages, armies, languages, religions).
4. Addictive “just one more year” loop.
5. Trait / culture / subspecies customization depth.
6. Chaos tools (Tsar Bomba, plague, ages) are satisfying.
7. Pixel art + reactive procedural music.
8. Long-term replayability with World Laws.
9. Community map sharing & mods.
10. Feels alive – units have needs, traits, opinions.

Sources: Steam reviews (e.g. “masterpiece since 2019”, “best god simulator”), r/Worldbox positive posts.

### 10 most complained (confirmed from reviews & discussions)
1. Army AI is dumb – retreats, camps wrong places, fails to capture (Steam discussions 2025-2026).
2. Kingdoms randomly collapse or stagnate in “golden age”.
3. War system still basic despite ArmyBox update.
4. Performance lag on large maps / high population (especially mobile).
5. Trait unlocking is grindy / obscure.
6. Alliances form too aggressively, hard to force pure conflict.
7. Long waits between major updates.
8. Some features feel incomplete or RNG-heavy.
9. Mobile vs PC feature parity gaps.
10. Desire for deeper economy, better walls/castles, stronger dragons, more jobs.

Sources: Steam reviews (“army always retreats”, “not worth full price for some”), r/Worldbox threads on AI and updates, X complaints.

---
*File created for collaborative design research. All major claims cross-checked against official wiki where possible. Minor details on exact resource numbers may vary slightly by version.*
