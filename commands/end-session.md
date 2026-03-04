---
description: End the current D&D session and save all game state
disable-model-invocation: true
---

# Session End

End the current session by following these steps exactly:

1. Find a natural stopping point (safe location, narrative pause)
2. Save all game state:
   a. Write the full session log to `game/sessions/log/session-NNN.md` using the template at `${CLAUDE_SKILL_DIR}/../skills/dm/templates/session-log.md`
   b. Append 3-5 bullet points to `game/sessions/journal.md` covering key events, decisions, and consequences
   c. Update `game/sessions/current.md` with full context for next session pickup — this is the primary save state
   d. Update all canonical files for any data that changed during the session (character sheet, inventory, NPC files, clocks, factions, locations)
   e. Update `game/GAME.md` if the campaign index needs new entries (new NPCs, locations, factions)
3. Give the player a brief "next time on..." teaser
