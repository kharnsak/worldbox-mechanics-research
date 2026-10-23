# WorldBox – God Simulator Mechanics Research Report

*(Maxim Karpenko / SuperWorldBox; current Steam ~0.51.x / mobile equivalents as of late 2026. Sources: official wiki the-official-worldbox-wiki.fandom.com, Steam store/news/patch notes, Destructoid/GamerDigest guides, Reddit/Steam reviews, X posts. Mechanics only; no assets. Version notes where mechanics changed. Unverified items marked.)*

### 1. World
**Map sizes** (tiles; default generator, PC/Steam; mobile may differ slightly):  
| Size       | Tiles     | Notes                  | Source |
|------------|-----------|------------------------|--------|
| Tiny      | 128×128  | 2×2                    | https://the-official-worldbox-wiki.fandom.com/wiki/Map_Creation |
| Small     | 192×192  | 3×3                    | same |
| Standard  | 256×256  | 4×4                    | same |
| Large     | 320×320  | 5×5                    | same |
| Huge      | 384×384  | 6×6                    | same |
| Gigantic  | 448×448  | 7×7                    | same |
| Titanic   | 512×512  | 8×8                    | same |
| Iceberg   | 576×576  | 9×9 (PC only)          | same |

Modded sizes possible (min ~1×1, max much larger; rectangular supported via workshop/Discord). Generator supports many shapes (continent, box, checkerboard, etc.) + options (random biomes, mountain edges, vegetation, resources, center lake/land, round/square edges, tree ring, low/high ground).

**Terrain layers / biomes**: Tiles include basic (deep/close ocean, shallow water, sand, plain/forest soil, hills, mountains, summit) + walls (stone, evil, ancient, wooded, green, iron, light). Biomes (seeds or natural): Grass, Savanna, Birch, Maple, Swamp, Jungle, Corrupted, Infernal, Mushroom, Candy, Enchanted, Flower, Clover, Garlic, Lemon, Crystal, Arcane Desert, Permafrost/Snowy, Rocklands, Celestial, Paradox, Singularity, Wasteland, Sand/Beach (special), etc. (~20+; exact count varies by version). Each has high/low variants, burn chance/rate, walk speed, nutrition, resources (herbs, berries, metals, etc.), special effects (e.g., Paradox: 10% chance quick-aging +1 year per step).

**Biome spread**: Grow strength 5 or 6. Higher strength wins contested tiles via random roll. Ages strongly modify: no spread in Age of Ice / Despair; dominant biomes spread 2× in favored ages. Generator pot amount / max continuous size control natural appearance.

**Ages** (10 total; controllable via Age Clock; introduced/expanded 0.21.0 MegaBox, upgraded later):  
| Age          | Approx. Length (years) | Key Effects (Loyalty/Opinion bonuses, temp, biome boost, clouds, etc.) | Source |
|--------------|------------------------|-----------------------------------------------------------------------|--------|
| Hope        | 35–55                 | +15 L / +15 O; unfreeze; light age/damage; normal growth; slots 1/3/5/6 | https://the-official-worldbox-wiki.fandom.com/wiki/Ages ; Steam 0.21 notes |
| Sun         | 35–55                 | +5 L / +5 O; unfreeze mtns; drought (kills trees); fire ×2; Fire Elementals chance; disabled vegetation growth | same |
| Dark        | 35–55                 | –5 L / –5 O; 50% less weapon range; 50% crop destroy chance | same |
| Tears       | (varies)              | Negative loyalty/opinion; emotional effects (unverified details)     | Steam 0.21 |
| Moon        | (varies)              | Night/overlay effects                                                | same |
| Chaos       | (varies)              | High chaos / danger                                                  | same |
| Wonders     | (varies)              | Magic-focused; special events                                        | same |
| Ice         | 30–40                 | Freezes growth; snow; –10 L/O range; freezes world                   | wiki Ages |
| Ash         | (varies)              | Life fading                                                          | Steam 0.21 |
| Despair     | (varies)              | Cold/dark/danger; freezes growth; –20 biome boost (no growth)        | wiki Ages |

Average weighting favors Hope; random “unknown” slots. Biome boosts, cloud rates, temperature damage, particle overlays vary. Ages can be forced/drag-dropped (post-0.50).

### 2. Units
**Races (civilized / sapient core 4; many more via subspecies/monoliths post-0.50)**:  
Humans, Orcs, Elves, Dwarves (classic; each has unique building style + race traits). Later: many animal civs, Lemon/Garlic/Candy Man, Crystal Golem, etc. via evolution/monoliths/subspecies. Base stats (unaltered L1 approx.):  
- Dwarf: 22 dmg, 4% armor, 30 spd, 1% dodge, 91% acc, 4 dip, 220 HP (king +30 XP/yr).  
- Elf: 15 dmg, 0% armor, 50 spd, 16% dodge, 96% acc, 8 dip, 140 HP (king +20 XP/yr).  
- Others scale similarly; level-up bonuses shared (e.g., L10: +5 dmg, +3% armor, +9% dodge/acc, +18 dip, +180 HP).

Preferred biomes: Elves forests/trees; Dwarves mountains; Orcs aggressive/any; Humans adaptable. Lifespan: varies by traits/genes (Long Liver, etc.); adults at ~16 if max age >30. Breeding: sapient adults; fertility traits; subspecies inheritance; families post-0.50.

**Traits** (116 creature traits; categories Cognitive/Mind/Spirit/Body/Acquired/Fun/Misc/Special; birth/inheritance/grow-up rates; many from biomes/food/books/ages/achievements; editor unlockable by hovering or achievements):  
Examples (full list on wiki; effects modify stats/behavior/appearance; same/opposite trait opinion mods):  
- Cognitive: Eagle Eyed (+5 acc, +15% crit; Arcane Desert/Lemon), Genius (+10 int etc.; Lemon/Celestial), Short Sighted, Stupid, Thief, Wise (age 40+ 30%).  
- Mind: Ambitious (+5 cities, +4 warfare… –15 loyalty; books), Content, Deceitful, Evil, Gluttonous, Greedy, Honest, Hotheaded, Lustful, Paranoid, Peaceful, Psychopath, Pyromaniac, Strong Minded…  
- Body/Spirit/Acquired: Acid Blood/Proof, Agile, Blessed (power), Bloodlust, Fire Proof, Immortal, Miner (Dwarves), Regeneration/Savage (Orcs), Weightless (Elves), Zombie, etc. Many from specific biomes/foods (e.g., Candy → Gluttonous), combat (Kingslayer), or powers (Blessed, Madness). Special (Boat, Scar of Divinity, Clone, etc.) non-random.

**Professions/jobs**: Leaders/kings (claim land, stewardship prioritizes expansion), blacksmiths (armor/weapons; mastery traits), miners, farmers, traders, soldiers/captains (post-0.51 armies), writers/readers (books/languages post-0.50), etc. Skilled workers added in later updates. (Exact full job list partially verified via culture traits.)

**Items/equipment**: Tiers from wood/bone → iron → higher metals (Mythril, Adamantine for Dwarves). Weapons (swords, hammers, bows, flame variants via culture traits), armor, boats (fishing/trading/transport). Crafting chance 50% for specials; culture traits enable roads, advanced items.

**Life cycle**: Eat (food tiles/nutrition; Gluttonous eats 2×; hunters meat), sleep (status), age (years; quick-aging biomes; old age death chance reduced in recent patches), die (combat, old age, disasters, traits like Death Nuke). Hunger/old age toggleable via World Laws.

### 3. Cities
**Founding**: Sapient adult (Prefrontal Cortex trait), no nearby enemies (same island + 1 chunk/16×16), valid 8×8 zone (land, not lava/water/other city, adapted biome), island ≥300 connected land tiles (excl. mtns). Starts ~3×3 zones. With existing kingdom: similar but kingdom-linked.

**Zones/territory**: 8×8 tile zones. Leaders/kings claim via “claim_land” task (stewardship priority; Expansionists culture or debug = up to 8 at once). Avoids non-adapted/uninhabitable.

**Buildings** (race-specific styles for houses/town halls; shared campfires/mines): Houses (density via Dense Dwellings/Hive Society culture traits), town halls, mineshafts, statues (+4 max via trait), roads (culture trait), walls, docks/boats. Tiers upgrade with knowledge/resources (exact costs partially verified; wood/stone/metals/gold). Post-0.50 more variety.

**Resources**: Food (herbs, berries, fruits, meat, mushrooms, candy, lemons, garlic, evil beets…), wood, stone, common metals, Mythril, gold, leather, etc. From tiles, mining, killing, trading.

**Roads/boats**: Roads via culture; boats (fishing/trading/transport; size tiers). Loyalty (traits, taxes, ages, events); low → rebellion (World Law). Taxes/tribute (kingdom traits High/Low Tax/Tribute 20–70%; default 50%).

### 4. Kingdoms
**Kings/succession**: Kings gain XP; clans/bloodlines (0.21+; levels, mottos, traits). Succession via clan/family. Leaders claim land.

**Clans**: Bloodlines with traits (e.g., Blood of Eons from Paradox); affect loyalty/diplomacy.

**Cultures/knowledge**: Culture traits (Harmony/Architecture/Buildings/Warfare… e.g., Roads, Dense Dwellings, Armorsmith Mastery, Expansionists). Knowledge levels via books/languages (post-0.50; reading grants XP/stats). Languages (opinion, learning). Religions (traits, rites, plots; 39 traits). Families (post-0.50).

**Opinion modifiers**: Same/opposite traits, ages (L/O bonuses), cultures/languages/religions, plots, wars, tributes. Exact numeric values sparse (e.g., trait mods ±5–30); diplomacy World Law enables alliances/wars/rebellions/plots.

**War declaration**: Plots (Whisper of War, Spite), natural opinion, ambition. Alliances via Unity/Friendship; Discord severs. Plots include peace talks, rebellions, rites.

### 5. War
**Armies** (meta-object post-0.51 ArmyBox): Captains rally; viewable/favoritable; zones/targets. Combat stats from unit level/traits/equipment (dmg, armor, dodge, acc, crit, range). Sieges/capture: armies attack villages; capture via occupation (AI sometimes suboptimal—retreats, poor targeting common complaint). Peace: plots, Friendship power, opinion recovery, Age effects.

### 6. Creatures and Monsters
Full list extensive (117+ spawn powers). Categories: civilized (Humans/Orcs/Elves/Dwarves + evolved), animals (Cat, Dog, Chicken, Rabbit, Monkey, Fox, Sheep, Cow, Wolf, Bear, Rhino, Buffalo, Hyena, Rat, Alpaca, Capybara, Goat, Penguin, Ostrich, Crab, Scorpion, Turtle, Crocodile, Snake, Frog, Piranha, Seal…), specials (UFO lasers, Dragon, Crabzilla, God Finger, Greg, Ants (black/green/blue create terrain), Bandit, Mages (White/Evil/Necromancer), Demons, Fairies, Zombies/Skeletons/Fire Skull, Tumor/Bioblob/Mush, Crystal Sword/Golem, Lemon/Garlic/Candy Man, Acid Blob, Smore, Flower Bud, Living Plants/Houses, etc.). Behavior: peaceful/herbivore/carnivore, spawn in biomes, traits (Peaceful, Savage…), some terraform or spread infection.

### 7. God Powers
~374 total across 8 tabs (Main, Unit, World Shaping, Noosphere and Life, Animals/Creatures/Monsters, Nature and Disasters, Destruction and Chaos, Other). No mana cost.  

- **Main**: Pause/Resume, Hourglass (time speed), Statistics, Eye of Insight, World Laws, Ages, World History, Game Stats, New World, Saves, Settings, Achievements, Community, Hide UI, Steam Workshop.  
- **World Shaping**: Terrain (oceans, sand, soils, hills, mtns, summit), walls (various), tools (shovels, finger, vortex, sponge, sickle, bucket, pickaxe, spade, axe, demolish, life eraser, scissors, paint, border brush), fuse/fireworks, printer patterns (hexagon, skull, etc.).  
- **Noosphere and Life**: Village/Kingdom/Relations info, Spite/Friendship/Inspiration/Whisper of War/Discord/Unity, favorites, layers (wars, armies, alliances, kingdoms, villages, clans, religions, cultures, languages, families, subspecies), map options, arrows (destination/lover/house/etc., Steam), money flow, bubbles.  
- **Animals…**: Spawn all races/creatures listed above.  
- **Nature and Disasters**: Temp hot/cold, Lightning, Force, Rain, Acid, Earthquake, Tornado, Fire, Lava, Seeds (all biomes), Fruit Bush, Stone/Gold/Ore, Geysers (water/acid/lava), Clouds (rain/acid/lava/life/blood…).  
- **Destruction and Chaos**: Bombs/grenades, Nukes/Tsar Bomba, Plague, Gray Goo, Infinity Coin, Death Mark, etc.  
- **Other**: Blessing, Madness, rains (Gamma/Omega/Delta for traits), possession, clone, etc.

### 8. World Laws
Toggles for fundamental rules (reorderable post-0.50; some achievement-locked; Forbidden Knowledge unlocks all but disables unlocks/achievements). Examples (complete list long; defaults noted):  
- Harmony / 100 People: Cap settlement pop at 100 (off).  
- Gaia’s Covenant: No damage from explosions/fire/disasters to tiles (off).  
- Hunger, Old Age, Animal Spawn, Fast Spawn, Sonic Speed, Mutant Box (random birth traits), Glitched Noosphere (more random traits), Grin Reaper, Magic Rites, etc. Many more for weather, disasters, logs, specific creatures.

### 9. UI
Windows/lists: World stats/graphs (pop pyramids, renown, kill counts, joined/left…), Village/Kingdom/Clan/Religion/Culture/Language/Family/Subspecies/Army info, Relations, Wars, Plots, Achievements, History log, Saves, Settings, Trait/Gene/Culture/Religion editors, Favorites.  

Map modes/layers: Kingdoms, Villages, Clans, Religions, Cultures, Languages, Families, Subspecies, Armies, Alliances, Wars, Borders, Happiness, Tasks, Money flow, Battles, Important events, Meta pins, Species icons, Names. Tooltips (zones/units, Steam), arrows (path/lover/house/family/parents/kids/attack). Minimap, power bar (hideable), possession view.

### 10. Player Reception
**What makes it fun** (Steam ~96% positive overall; reviews/X/Reddit):  
- Pure sandbox freedom — create or destroy anything with zero resource cost.  
- Emergent storytelling from living sims (kingdoms rise/fall, unexpected wars, trait inheritance).  
- Watching civilizations grow, trade, invent, and collapse over centuries.  
- God-like chaos tools (nukes, plagues, ages, biomes) for instant spectacle.  
- Deep customization (traits, genes, cultures, religions, subspecies post-0.50).  
- Replayability via World Laws and ages creating unique scenarios.  
- Pixel aesthetic + procedural music that reacts to the scene.  
- Constant free updates adding systems (clans, armies, languages, families).  
- Sharing maps/worlds and community creativity.  
- “Just one more year” addictive simulation loop.

**Common complaints**:  
- AI pathing/decision-making weak (armies retreat, ignore objectives, suboptimal sieges).  
- Kingdoms collapse randomly or stagnate in “golden age.”  
- War system still basic despite ArmyBox; needs deeper strategy.  
- Performance lag on large maps/high pop (especially mobile).  
- Unlocking traits/achievements sometimes obscure or buggy.  
- Long gaps between major updates (though frequent smaller ones).  
- Some features feel incomplete or RNG-heavy.  
- Mobile vs PC feature parity gaps (map sizes, tooltips).  
- Alliances form too aggressively, hard to force pure conflict.  
- Desire for more jobs, deeper economy, better walls/castles, stronger dragons.

This covers core mechanics across versions. For design inspiration, focus on the layered simulation (tiles → units with traits → cities → meta-objects like clans/cultures/religions → player god powers + laws) and emergent age/biome interactions. Further deep dives available on specific wiki pages.

---
*Researched and saved by Grok for collaborative use. Original request from user kharnsak. Public repo for sharing with other AIs/collaborators.*