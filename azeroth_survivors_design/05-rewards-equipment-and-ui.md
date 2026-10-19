# Rewards, Equipment and Interface

## Gold and chests — confirmed

- Ordinary kills award **automatically collected in-run gold**. Gold does not require walking over drops.
- Standard treasure chests spawn every **2–4 minutes**, indefinitely even after 30:00, at valid reachable points roughly **50–100 yards** from player.
- Chests appear on minimap only **when within minimap range**, like WoW Find Treasure; no global chest location marker.
- Chests **never despawn**. If unaffordable, they remain available for a later return.
- Chest price increases with run time but is **locked at spawn**, so earlier chests remain cheaper. Gold income increases with rising mob density. Aim for a successful ~30-minute run to afford most/all spawned chests, not early effortless purchases.
- Walk over affordable standard chest → **automatically pay/open**, full pause and receive **one random reward** (no selection/preview). Potential rewards: temporary common/uncommon gear, evolution object or other rewards.
- Named world minibosses guarantee **free** chests, using existing random reward logic.
- In-run gold expires when run ends. Selling permanent gear between runs provides a modest **starting-gold bonus for the next run only**, not a banked currency. Unused bonus gold expires after that run.

## Permanent equipment — confirmed

- At **victory**, dungeon-specific permanent rare/epic items have a **chance** to drop, inspired by original WoW loot (examples: Deadmines Cruel Barb, Wailing Caverns Armor of the Fang, Scarlet Monastery Herod's Shoulder, Scholomance Headmaster's Charge). No guaranteed permanent drop.
- Heroic eventually offers stronger variants and unique drops.
- Account-wide bags and equipment; any class can use items, no weapon proficiency or class restrictions, but slot placement still applies.
- Full original WoW slot layout: head, neck, shoulders, cloak, chest, shirt, tabard, wrists, hands, belt, legs, boots, two rings, two trinkets, main hand, offhand, ranged/relic.
- Duplicates are **separate item instances**; can equip identical items in compatible slots, sell them or merge them.
- Upgrades have **no hard cap**. Merge two identical items by **summing their existing upgrade levels**; one copy consumed, no bonus rank for merging. Example +5 and +3 → +8. Unupgraded duplicate merges may yield +0 under this rule; review whether intended if/when upgrade economy is implemented.
- Stats scale with item upgrades; numerical examples like Cruel Barb base +10% damage and +1 percentage point per upgrade are illustrative, not fixed.
- Gear selection, merging, selling, talents and appearance management happen **between runs only**. Permanent loadout locked during runs.

## Temporary equipment — confirmed

- Random common/uncommon gear from chests during a run.
- No equipment slots, replacement or in-run inventory management; temporary bonuses stack on top of permanent equipped gear.
- All temporary bonuses expire at run end. A Run Bonuses panel is an optional UI idea.

## Character appearance — confirmed direction

- Basic race/gender/face/skin/hair customisation on home screen between runs, as supported by assets; no barber shop required.
- Equipped permanent gear should visibly appear on character. Prioritise weapons, shields, helms and shoulders, then other armour, subject to asset pipeline audit. Rings and similar items need not be visible.
- Temporary gear does **not** change character appearance.
- Individual hide/show gear visibility toggles initially.
- Full transmog later. **Proposed, not explicitly confirmed:** collecting an item's appearance permanently unlocks its cosmetic even after selling/consuming the item.
- Race remains cosmetic only, without any gameplay impact.

## Run results and history — confirmed

- Both victory and death show a **detailed results screen**, not just Game Over.
- Persist run history: duration, level, enemies killed, bosses killed, gem XP, permanent boss XP, gold, ability damage breakdown, evolutions, equipment loadout, talents, final spells/ranks, boss roster and related run statistics.
- Permanent dungeon loot rolls at victory; permanent account XP from boss kills is already credited at kill time.

## Boss HUD — confirmed

- Boss health bars stacked across the top in spawn order.
- Collapsible ordered dungeon boss tracker: future/spawned/alive/dead states; separate rare tracking; no earlier boss spawn countdowns.
- Bosses have no minimap location markers; fixed named minibosses likewise have no markers.
