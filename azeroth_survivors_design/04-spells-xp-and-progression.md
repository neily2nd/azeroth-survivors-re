# Spells, XP, Evolution and Talents

## Abilities and level-up choices — confirmed

- Six active spell slots and six passive/buff slots; ordinary spells max at **rank 8**.
- On each in-run level-up, **pause all gameplay** and present **three random valid choices**. No rerolls, skipping or guaranteed desired builds.
- Don't offer a new spell if its slot category is full. Choices must be attainable.
- One XP pickup can grant multiple levels: present **one full three-choice screen per level**, consecutively while paused. Each selection affects subsequent offers.
- After all spells/passives are maxed, continue indefinitely with three random repeatable rewards (e.g. +1% damage, +1% speed, +5% max HP, +100 gold, full heal Healthstone). Values illustrative, not balanced. Replaces existing automatic max-build full heal.

## XP gems — confirmed (Questions 81–86)

- XP must be physically collected; **never despawns**, including after long runs.
- Instant pickup on entering pickup radius; no channel, enemy obstruction or collection delay.
- The existing pickup-radius **passive spell** remains the means of extending pickup radius; do not add a separate permanent pickup-range stat.
- Ordinary enemy types award fixed XP per kill regardless of run time; tougher enemies/elites/minibosses give more. Dungeon bosses also drop large XP gems.
- **Nearby gems merge** into fewer larger gems, preserving exactly 100% of XP. Merge only at very short distances; no gem attraction, wandering, regional consolidation or teleporting XP to player.
- Combined gems remain at the local cluster, visually distinguishable by size/colour if feasible.
- XP needed per level **continues increasing indefinitely**, including repeatable-reward levels. No hard run-level cap; balance curve later.
- Permanent account XP is a separate system from collectible in-run XP.

## Spell evolution — confirmed

- Two spells at **rank 4 or above** can qualify for a recipe.
- Bosses guarantee evolution objects; rares may drop them; chests may contain them.
- Evolution objects **persist on the ground**. Must physically collect to trigger; combat fully pauses for reveal.
- If multiple recipes are eligible, **randomly select one**. If none eligible, award an alternative reward; don't store evolution objects for later.
- Evolution consumes both ingredient spells, creates **one evolved spell at rank 1**, and frees the other slot. Evolved spell can rank up.
- Branching, overlapping recipes and multi-stage chains allowed; **no universal evolution depth cap**. Examples: Rend + Thunder Clap → Thunderous Rend; Thunderous Rend + Blizzard → Bleeding Thunderstorm.
- Recipes hidden until first discovery, then permanently recorded in a catalogue; discovered recipes may appear as optional hints when inspecting spells in-run.
- Visuals use recognisable hybrid effects from both ingredients, reusing/layering existing assets, scaling, colours and procedural effects; rare recipes may eventually get custom particles/shaders. Actual rendering feasibility requires asset audit.

## Cross-class borrowed spells — confirmed

- Certain evolved spells conditionally add spells from other classes to the random level-up pool (e.g. owning Thunderous Rend permits Blizzard).
- Permission exists only **while the required evolved spell is currently owned in that run**.
- If prerequisite is consumed in an evolution **other than the intended dependent recipe**, borrowed spell disappears immediately, without refund; freed slot; show a clear paused explanation.
- Evolved spells inherit relevant talent effects through their **full ingredient ancestry**, potentially across classes. Adapt or define handling for mechanically incompatible effects.

## Permanent account level and class talents — confirmed

- Dungeon boss kills immediately grant account XP, retained after run death. Later bosses and higher maps provide gently larger rewards.
- Account level grants talent points to **each class independently**, not a single shared point budget. Illustrative: account level 21 → 20 talent points available to each class.
- Talents can be respecced **freely and without limit between runs**.
- Talents from multiple classes can affect an evolved spell when its ancestry includes those classes' abilities.
- Talents alone do **not** unlock cross-class spells.
