# Azeroth Survivors — Design Documentation

**Status:** Design interview paused after Question 92 (19 October 2026).  
**Purpose:** Preserve decisions for future discussion and eventual implementation by Luna (Codex GPT-6).  
**Important:** This is a design record, **not an implementation request**. Separate confirmed decisions from deferred ambitions and unresolved details.

## Documents

1. [Vision and existing foundation](01-vision-and-foundation.md)
2. [Runs, combat and enemies](02-runs-combat-and-enemies.md)
3. [Worlds, encounters and bosses](03-worlds-encounters-and-bosses.md)
4. [Spells, XP, evolution and talents](04-spells-xp-and-progression.md)
5. [Rewards, equipment and interface](05-rewards-equipment-and-ui.md)
6. [Future ideas, dependencies and open decisions](06-roadmap-and-open-questions.md)

## Design principles

- **Autobattler first, Warcraft second.** Player movement, positioning, pickups and choices; spells attack automatically.
- **One life per run.** No resurrection, extra-life effects or second chances.
- **Player knowledge matters.** Learn maps, miniboss locations, dangerous regions and boss patterns.
- **Build power is earned.** RNG, talents and choices matter; no hidden adaptive difficulty rescuing bad runs.
- **Performance-conscious spectacle.** Start with 300–600 visible enemies, then optimise upward; raids are a distant ambition.
- **Keep it implementable.** Reuse behaviours and assets, prioritise a functional core, and defer bespoke mechanics.

## Decision notation

- **Confirmed:** Explicitly agreed in interview.
- **Proposed:** Suggested but not explicitly agreed.
- **Deferred:** Long-term feature or later improvement, not immediate scope.
- **Unverified:** Needs audit of existing code/assets or technical proof.

This record reflects the design conversation and known project context, not a fresh codebase audit.
