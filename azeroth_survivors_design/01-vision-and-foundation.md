# Vision and Existing Foundation

## Vision — confirmed

**Azeroth Survivors** is a Rust/Bevy 3D Warcraft-themed Vampire Survivors-style game. The player moves, dodges, positions, gathers physical XP pickups, and selects random spells/passives while combat attacks auto-fire. Ordinary mobs should eventually become slaughter fodder; bosses and rares stay dangerous. Classes differ primarily in starting spells, available abilities, and visual identity rather than mandatory tank/healer/DPS roles.

**Races are 100% cosmetic — a hard rule.** No racial statistics, abilities, progression, map restrictions, or advantages. All races can enter any unlocked map. Equipment and progression are account-wide as specified in the other documents.

## Current implementation baseline — previously reported, not freshly verified

- Repository: `C:\Azeroth\azeroth-survivors-re`; branch `phase2/content-system`; fork `https://github.com/neily2nd/azeroth-survivors-re.git`.
- Previously reported synced commit: `0c0ea1d`; build/tests/Clippy passed at that point.
- 9 classes, 8 races, 16 maps, 73 abilities with 16 runtime kinds.
- Six active ability slots, six passive slots; ordinary ability maximum rank 8.
- Current 15-minute timer victory is **to be replaced** with final boss at 30:00 and victory only upon its death.
- Current bosses chase and deal contact damage, without bespoke attacks or stacked individual health bars yet.
- Current maxed-build reward is a full-heal Healthstone; design replaces it with repeatable three-choice rewards, where a full heal may be one option.
- No permanent equipment, spell evolution, or talent progression implemented at that snapshot.

## Team and workflow

- User: creative director, design decisions and playtesting.
- ChatGPT: design collaborator, documentation and future implementation briefings.
- Luna (Codex GPT-6): implementation engineer when explicitly requested.
- **Do not convert these notes into coding tasks without user approval.**

## Product scope

- Normal zones and their associated dungeon boss rosters first.
- Heroic mode later, starting with numerical difficulty/loot changes.
- Raids and large allied NPC raid fantasies are explicitly long-term, not near-term milestones.
