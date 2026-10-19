# Runs, Combat and Enemies

## Run structure — confirmed

- A run continues until the **final dungeon boss is killed** (victory) or the player reaches zero HP (death).
- The final boss appears at **exactly 30:00**. The clock alone never wins a run; players may intentionally survive for hours without killing the final boss.
- **One life, absolute rule:** no resurrection, extra lives via gear/spells/talents, or second chances.
- Victory triggers immediately on final boss death even if earlier bosses or summoned enemies remain alive.
- Level-up, evolution reveals and chest reward reveals pause the entire simulation: enemies, projectiles, cooldowns and timer.

## Enemy population and difficulty — confirmed (Questions 60, 67, 78–80, 87)

- Progress through **escalating enemy types and density**: weak enemies stay in the spawn pool; tougher elites and variants join later.
- Initial busiest-screen performance goal: **300–600 enemies**. Larger populations (1,000+, 2,000+) are future aspirations, contingent on profiling and optimisation.
- Spawn rate increases over run time and **continues increasing after 30:00**. No dynamic difficulty assistance for struggling builds.
- A technical active-enemy cap may prevent overload; it is **not** a gameplay mechanism to make bad runs easier.
- Ordinary enemy health/damage **stop time-based scaling at 30:00**. More enemies, not ever-inflating wolf health, provide endless pressure.
- Ordinary enemies far beyond a generous player-centred active range are culled/despawned. Merely leaving the camera view does not despawn them.
- Uncollected XP, healing items and treasure chests are **not** culled with enemies and never expire.

## Behaviours and collision — confirmed (Questions 61–66)

- Reusable ordinary enemy archetypes: melee, **short-range weaker ranged**, fast/fragile, tanky and eventually summoner. No bespoke AI for every Warcraft creature.
- Ranged enemies have limited attack distance, lower danger than comparable melee enemies, and readable projectiles; no off-screen sniping.
- Enemies **pass through one another**. No enemy-to-enemy physics separation or pushing.
- Enemies **do not block player movement**. The player can run through hordes but risks contact damage.
- Contact damage uses a short **player invulnerability window** after a hit (initial test value around 0.5 seconds; not final balance).
- **Initially:** boss and normal contact hits share that invulnerability window. **Deferred improvement:** stronger boss hit can replace the damage of a weaker hit in the window without double-charging damage (e.g. 5 then 100 → 100 total).
- Ordinary enemy melee attack animations are **visual decoration only**; damage is calculated through contact, not animation hit events.
- Ordinary attack sounds are disabled to avoid audio spam. Stagger animations where helpful; animation LOD/distance update rates are optimisation candidates.
- Audio removal alone does not guarantee performance; rendering and animation costs require profiling.

## Healing — confirmed (Questions 57–59)

- Healing comes from **spells/passives** and **occasional pickups** from enemies/chests.
- Ordinary mobs have a very small chance to drop healing; tougher elites/rares have better chances and some may guarantee a drop. Balance against high late-game kill rates.
- Walk over healing item → **immediate automatic consumption**, even at full health; excess healing is wasted.
- No consumable inventory or potion hotkeys.
- Uncollected healing pickups persist indefinitely.
- Healing pickup collection should require close proximity, not long-distance XP-style attraction.

## Crowd control — confirmed (Question 88)

- Ordinary enemies receive full crowd control.
- Elites and named minibosses have some resistance.
- Dungeon/raid bosses have **slight** resistance, not total immunity: weaker slows, shorter hard CC and protection against permanent stunlock; reduced knockback.
- Exact percentages, timings and implementation remain balancing details. Avoid elaborate diminishing-return systems initially.

## Boss summons — confirmed (Questions 89–90)

- **Some**, not all, bosses may summon thematic reinforcements using existing enemy behaviours. Boss-specific summons can be implemented after core boss rosters work.
- Summoned creatures are ordinary enemies once created. They remain when their summoning boss dies, and use normal XP, gold and culling rules.
