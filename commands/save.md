---
description: Save current game progress without ending the session
disable-model-invocation: true
---

# Save Progress

Save all current game state by following these steps exactly:

1. Write the full session log to `game/sessions/log/session-NNN.md` using the template at `${CLAUDE_SKILL_DIR}/../skills/dm/templates/session-log.md`
2. Append 3-5 bullet points to `game/sessions/journal.md` covering key events, decisions, and consequences
3. Update `game/sessions/current.md` with full context for next session pickup — this is the primary save state
4. Update all canonical files for any data that changed during the session (character sheet, inventory, NPC files, clocks, factions, locations)
5. Update `game/GAME.md` if the campaign index needs new entries (new NPCs, locations, factions)
6. Confirm to the player that progress has been saved
