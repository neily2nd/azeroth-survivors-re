# Worlds, Encounters and Bosses

## Maps and dungeon rosters — confirmed design direction

- **Zone = battlefield; associated dungeon = ordered boss/rare roster.** Use full appropriate dungeon roster rather than a fixed six-boss quota.
- Elwynn Forest → Deadmines → final boss **Edwin VanCleef**.
- The Barrens → Wailing Caverns → final boss **Mutanus the Devourer**.
- Tirisfal Glades (illustrative level requirement 40) → Scarlet Monastery wings (user cited eight bosses and three rares; roster needs verification).
- Western Plaguelands (illustrative level requirement 60) → Scholomance → final boss **Darkmaster Gandling**.
- Duskwood → Stockades bosses was suggested, **not finalised**.
- Bosses appear in sensible dungeon order; only the final boss is fixed to **30:00**. Do not show exact arrival times for earlier bosses.
- Bosses spawn at random valid locations away from player (rough design range 50–300 yards), announce arrival, and chase relentlessly. No minimap location icons.
- Individual boss health bars stack at screen top in spawn order.
- Collapsible on-screen dungeon boss tracker shows ordered roster, dead/spawned/future states, no arrival countdowns; rares tracked separately.
- Earlier bosses never despawn, reset, leash or get culled; can accumulate. Killing final boss ends run even if earlier bosses survive.

## Full Warcraft zones and world streaming — preferred, unverified

- Strong preference to use **entire Warcraft zones**, not tiny arenas, with correct terrain, caves and landmarks.
- The technical possibility is credible through chunk/region streaming and distance-based simulation, but **requires code/assets audit**: terrain loader, model availability, collision, cave transitions, camera and navigation. Do not claim it already works.
- Player should have **unrestricted access** to the playable map, with no timed area gates.
- Geographic danger zones use simple fixed enemy stat modifiers and themed encounters; no bespoke region AI required. Enemy stats can be assigned at spawn and remain stable after leaving region.
- Dynamic ordinary hordes spawn outside visible view around the player across the map, while thematic encounters exist at learnable fixed locations.
- If full zones are impractical, preserve fixed encounters within available maps and consider optional dynamic encounters later.

## Named world minibosses — confirmed (Questions 69–77)

- Fixed, learnable world locations, including Normal and Heroic; examples include **Goldtooth** at a kobold mine and a named spider in another mine. Exact encounter roster/location requires asset/world-data validation.
- Distinctive **2–3× scale** compared with ordinary models; no minimap markers or permanent discovery markers. **Knowledge is power.**
- Aggro automatically within a **small detection radius** or from **any damage**, including accidental automatic spell/AoE hits. No immunity to unintended targeting.
- Once pulled, miniboss chases until killed or player dies. **No leash, reset, despawn, return-home or teleport catch-up.** Damage remains.
- At long range, disable rendering/full animation and update pursuit cheaply; restore full simulation when near. Valid terrain/cave routing remains a technical dependency.
- Each named miniboss can be killed once per run and **guarantees one free treasure chest**; chest contains random rewards under existing chest rules and remains until collected. No additional guaranteed evolution drop just for being a miniboss.
- Player may intentionally or accidentally accumulate multiple minibosses and dungeon bosses.

## Dungeon boss rewards — confirmed (Questions 91–92)

- Boss death immediately awards **permanent account XP**, retained even if the run ends in death.
- Boss also drops a **large collectible in-run XP gem**, which persists and merges under normal XP rules.
- Major bosses **guarantee an evolution object** on the ground, subject to normal eligibility/alternative-reward rules.
- **Later bosses in a dungeon award more of both XP types**, with the final boss giving the most; higher-level maps gently improve permanent account XP without making old maps obsolete.
- Killing final boss immediately ends run; uncollected rewards on ground at that instant may be lost, while immediate permanent XP is retained. **Exact final-boss pickup/victory handling remains an open UX question.**

## Map unlocking — confirmed direction

- Unlock next map by **either** defeating preceding map's final boss **or** reaching its account-level threshold.
- Level-based unlocking does not mark earlier maps as completed.
- All races can play all unlocked maps; no race/class restrictions.
- Exact map order, thresholds and dungeon roster are still to be finalised.

## Heroic and raids — deferred

- Heroic mode (illustrative account-level requirement 60) initially scales enemy numbers/stats and offers stronger variants of normal loot plus exclusive drops. New mechanics come **after** the core game works.
- Raid maps **eventually** use normal 30-minute run structure with raid bosses, ending on final raid boss death. Raid development is not immediate scope.
- Far-future fantasy: 40-character allied party (player + 39 NPC tanks/healers/DPS), immense armies, longer 45–60-minute raids and 3–5-minute raid boss fights; Molten Core/Blackwing Lair using Searing Gorge/Burning Steppes as examples. **Explicitly parked, potentially years away, not an implementation commitment.**
