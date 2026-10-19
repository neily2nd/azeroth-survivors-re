# Roadmap, Dependencies and Open Questions

## Development philosophy

This is **not** an implementation plan or instruction to Luna. Preserve design, audit actual systems first, implement incrementally and profile before committing to scale. The user explicitly requested a pause after 92 design questions.

## Priority bands

### Core gameplay and correctness

- 30-minute final-boss win condition and ordered dungeon boss rosters.
- One-life run ending, detailed result/history, pause semantics.
- XP gems, local merging, multi-level queues and reward validity.
- Simple scalable enemy archetypes, contact damage/invulnerability, spawning/culling.
- Persistent bosses and fixed world minibosses with guaranteed rewards.
- Gold, standard chests, healing drops and repeatable max-build rewards.
- Spell evolutions, cross-class dependency rules, talents and account progression.

These are **design needs**, not claims that all are missing or ordered engineering tickets. Verify what already exists before changes.

### Larger foundational work requiring investigation

- Full-zone Warcraft terrain and asset pipeline, world streaming and caves.
- Navigation through caves/around obstacles for persistent long-distance boss pursuit.
- Efficient 3D animation and rendering at 300–600 simultaneous enemies, then beyond.
- Visually equipped permanent items, account-wide bags and upgrade/merge systems.
- Correct persistence and save migration for run history, discoveries, talents and gear.

### Explicitly deferred

- Bespoke Heroic boss mechanics; first Heroic implementation may use stat/loot scaling.
- Sophisticated boss summoning and unique attack behaviours beyond basic chase/contact.
- Stronger-hit override during contact invulnerability; initially shared window.
- Full transmog and elaborate cosmetic asset work.
- Raid maps (initial raid design: normal 30-minute structure).
- Player plus 39 allied NPCs, 45–60-minute raid endurance runs, thousands of enemies, multi-minute raid bosses — distant ambition, **not current scope**.

## Open questions / design gaps

1. **Final boss loot timing:** If final boss death immediately ends the run, how can the player collect its evolution object and large XP gem? Decide whether final boss differs from earlier bosses or victory resolves drops automatically.
2. **Full-zone feasibility:** Inspect terrain assets, cave access, collisions, camera, streaming and available world-data before promising complete Elwynn Forest.
3. **Miniboss distant navigation:** Specify pathing that avoids walls and caves without teleporting; consider what happens if player crosses inaccessible boundaries.
4. **Map and boss roster:** Verify complete dungeon boss/rare lists, timings, map order, unlock level thresholds and which zone hosts each dungeon.
5. **Spawn balancing:** Tune density ramps, technical caps, elite ratios and late-run performance after measuring actual gameplay.
6. **XP curve:** Tune rising level requirements and XP rewards, especially with huge kill rates and merged gems.
7. **Healing balance:** Tune healing drop chances against mob density and contact damage windows.
8. **Evolution recipes:** Define actual spell combinations, rank inheritance, compatibility and alternate rewards when no recipe eligible.
9. **Cross-class ancestry:** Formalise which talent modifiers carry into evolved spells and how incompatible mechanics adapt.
10. **Equipment economics:** Define item stats, victory drop rates, Heroic item differences, selling bonus, and consequences of merging two +0 items.
11. **Boss mechanics:** Determine exact roster of bosses allowed to summon and later which have unique attacks.
12. **UI details:** Define final boss tracker presentation, catalogue, results history, appearance options and equipment management after existing UI audit.
13. **World miniboss roster:** Ground fixed locations and named creatures in actual accessible Warcraft map assets rather than assuming all landmarks are available.

## Most recent confirmed decisions (Questions 57–92)

| Question | Decision |
|---|---|
| 57 | Healing spells/passives **and** occasional healing pickups |
| 58 | Healing pickups auto-consume on contact, even if wasted |
| 59 | Very rare ordinary healing drops; better elite/rare chances |
| 60 | Enemy types and density escalate; weak enemies remain |
| 61 | Reusable enemy archetypes; ranged mobs short-range and weaker |
| 62 | No enemy-to-enemy collision |
| 63 | Enemies do not block player movement |
| 64 | Brief player contact-damage invulnerability |
| 65 | Shared boss/normal invulnerability initially; stronger-hit override later |
| 66 | Decorative attack animations; silent ordinary attacks; contact damage |
| 67 | Start with 300–600 enemies; optimise higher later |
| 68 | Raid levels eventually use normal 30-minute structure; grand 40-NPC raids parked |
| 69 | Dynamic hordes plus fixed geographically meaningful encounters |
| 70 | Fixed named minibosses, once per run; full zone preferred if feasible |
| 71 | Unrestricted exploration with dangerous geographic regions |
| 72 | Pulled minibosses chase relentlessly, never leash/reset |
| 73 | No miniboss minimap markers; oversized 2–3× models |
| 74 | Small proximity aggro radius |
| 75 | Guaranteed free chest from named miniboss kill |
| 76 | Any damage, including accidental AoE, triggers miniboss aggro |
| 77 | Lightweight long-range miniboss pursuit, no teleporting |
| 78 | Cull distant ordinary enemies, not persistent bosses or pickups |
| 79 | Fixed escalating spawn rates; only technical population cap |
| 80 | Spawn rate continues increasing after 30:00 |
| 81 | Fixed per-type XP; larger rewards from tougher enemies |
| 82 | Nearby XP gems merge without losing value |
| 83 | Gems do not attract or move to merge over distance |
| 84 | XP pickup instant within radius |
| 85 | Multiple levels → consecutive three-choice screens, fully paused |
| 86 | XP requirements rise indefinitely |
| 87 | Ordinary enemy stats stop scaling at 30:00 |
| 88 | Bosses have slight crowd-control resistance |
| 89 | Some bosses summon thematic reinforcements |
| 90 | Summons remain after summoner boss dies |
| 91 | Bosses grant immediate account XP plus collectible large in-run XP gem |
| 92 | Later dungeon bosses award more of both XP types |

## Resuming the interview

Start with a brief recap, not another wall of questions. Ask **one question at a time**. Do not start implementation or write Luna prompts unless the user explicitly asks. The next unanswered question is **Question 93**.
