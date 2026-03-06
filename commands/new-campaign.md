---
description: Create a new D&D campaign with world generation and game directory scaffold
disable-model-invocation: true
---

# New Campaign Setup

Create a new campaign by following these steps:

## Step 1: Scaffold the game directory

Create the following directory structure. Use the templates from `${CLAUDE_PLUGIN_ROOT}/skills/dm/templates/` as starting points for each file:

```
game/
├── GAME.md                          # from game-index.md template
├── campaign/
│   ├── world.md                     # from world.md template
│   ├── factions.md                  # from factions.md template
│   ├── quests.md                    # from quests.md template
│   └── clocks.md                    # from clocks.md template
├── characters/
│   ├── player/                      # empty — filled during character creation
│   └── npcs/                        # empty — filled during world gen
├── locations/
│   ├── index.md                     # from location-index.md template
├── sessions/
│   ├── current.md                   # from current-session.md template
│   ├── journal.md                   # from journal.md template
│   └── log/                         # empty — filled per session
├── combat/
│   └── tracker.md                   # from combat-tracker.md template
├── inventory/
│   └── party.md                     # from party-inventory.md template
└── rules/
    └── houserules.md                # from houserules.md template
```

## Step 2: World Generation

Collaborate with the player on the type of setting they want, then:

1. Generate the world and write to `game/campaign/world.md`
2. Create the starting location and write to `game/locations/`
3. Create 2-3 starting NPCs and write to `game/characters/npcs/` (include `## Conversation Log` section — see NPC template)
4. Create initial factions and write to `game/campaign/factions.md`
5. Create **starting quests** using the Secrets-First Protocol (read `${CLAUDE_PLUGIN_ROOT}/skills/dm/quest-design.md`):
   - **1 Standard quest** — the main opening hook that draws the player into the world
   - **1-2 Minor quests** — smaller threads discoverable through NPCs or exploration
   - For each: define the Truth first, build evidence trail, seed NPC Knowledge tables and location Quest Clues
   - Write all quests to `game/campaign/quests.md`
   - Populate the Quest Secrets Summary in `game/sessions/current.md`
6. Update `game/locations/index.md` with starting locations
7. Update `game/GAME.md` with all cross-references
8. Write the opening scene to `game/sessions/current.md`

## Step 3: Character Creation

Guide the player through creating their character. Use the character sheet template at `${CLAUDE_PLUGIN_ROOT}/skills/dm/templates/character-sheet.md` for the final output format.

1. Ask the player for their character concept (or offer suggestions that fit the world)
2. Guide through race selection — explain racial traits
3. Guide through class selection — explain class features
4. Ability scores — offer Standard Array, Point Buy, or 4d6-drop-lowest
5. Background selection — explain feature and proficiencies
6. Equipment selection — by class/background or starting gold
7. Personality traits, ideals, bonds, flaws
8. Backstory — collaborate with the player, tie it into the world
9. Write the complete character sheet to `game/characters/player/<name>.md`
10. Update `game/GAME.md` and `game/inventory/party.md`

### Guidelines

- Roll all dice transparently (4d6 drop lowest, starting gold, etc.)
- Explain each choice clearly but don't overwhelm — let the player decide how deep they want to go
- If the player has a clear vision, don't force them through every sub-step
- Ensure all modifiers, proficiencies, and features are correctly calculated
