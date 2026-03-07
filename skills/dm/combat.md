# Combat Flow

## Initiating Combat
1. Determine surprise (if applicable)
2. Roll initiative for all combatants: `d20(<roll>) + <DEX mod> = <total>`
3. Create/update `game/combat/tracker.md` with initiative order, HP, AC, conditions
4. Announce initiative order to the player

## Each Round
1. Process combatants in initiative order (highest to lowest)
2. For the player: present the situation, **then ask for their action and wait**. Never choose the player's action, spell, or target — even if the choice seems obvious. Each turn is a decision point.
3. For NPCs/monsters: determine their action based on personality/tactics from their `.md` file
4. Resolve all attacks/spells/abilities with transparent dice rolls
5. **Narrate first, then show mechanics.** Describe what happens in the fiction (the flame, the impact, the dodge), then present the mechanical results (damage, HP changes, conditions). The player should experience the story before the spreadsheet.
6. Update `game/combat/tracker.md` after each round

## Ending Combat
1. Narrate the outcome
2. Calculate and award XP (or note milestone progress)
3. Archive the combat to the session log
4. Clear `game/combat/tracker.md` (reset to "No active combat")
5. Update character sheet (HP, spell slots, abilities used)
6. Update `game/inventory/party.md` with any loot
7. Run a full state checkpoint

## Combat Rules (5e RAW)
- Actions: Attack, Cast a Spell, Dash, Disengage, Dodge, Help, Hide, Ready, Search, Use an Object
- Bonus actions: only if a feature/spell grants one
- Reactions: one per round (resets at start of your turn)
- Movement: can split before/after actions
- Opportunity attacks: when leaving a hostile creature's reach without Disengaging
- Concentration: CON save (DC 10 or half damage, whichever is higher) when taking damage
- Death saves: d20 at start of each turn when at 0 HP; 10+ = success, 9- = failure; nat 20 = regain 1 HP; nat 1 = 2 failures
