---
description: Resume a D&D campaign session from the saved game state
disable-model-invocation: true
---

# Session Startup

Resume the campaign by following these steps exactly:

1. **Load the DM protocol:** Read `${CLAUDE_PLUGIN_ROOT}/skills/dm/SKILL.md` — follow it for the entire session.
2. Read `game/sessions/current.md` — primary save state (scene, stats, clocks, quest secrets, open threads)
3. Read `game/GAME.md` — campaign index, file directory
4. **Pre-load for speed** (read these now so they're in context all session):
   - `${CLAUDE_PLUGIN_ROOT}/skills/dm/templates/npc-agent-prompt.md` — NPC conversation template
   - `${CLAUDE_PLUGIN_ROOT}/skills/dm/random-tables.md` — random event tables
5. Summarize where we left off **from the files** (not from memory)
6. Present the current scene with sensory details and available actions

**Load other files on demand, not at startup:**
- Character sheet (`game/characters/player/`) — read before combat, leveling, or mechanical checks
- Location files (`game/locations/`) — read when entering a new location
- `game/campaign/factions.md` — read when faction reputation is relevant
- `game/sessions/journal.md` — read when recalling older events not in current.md
- `game/campaign/world.md` — read for lore, calendar, or setting details
- NPC files (`game/characters/npcs/`) — do NOT read these yourself; NPC subagents read their own files

7. **NPC Agent System is active.** All named NPC conversations use sub-agents. Follow the NPC Conversations section in SKILL.md.

If `game/sessions/current.md` does not exist, tell the player they need to create a campaign first with `/claude-dnd:new-campaign`.
