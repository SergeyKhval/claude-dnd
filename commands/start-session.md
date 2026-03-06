---
description: Resume a D&D campaign session from the saved game state
disable-model-invocation: true
---

# Session Startup

Resume the campaign by following these steps exactly:

1. **Load the DM protocol:** Read `${CLAUDE_PLUGIN_ROOT}/skills/dm/SKILL.md` — this defines all game rules, state management, NPC sub-agent system, and combat flow. Follow it for the entire session.
2. Read `game/sessions/current.md` — this is the primary save state (scene, stats, clocks, open threads)
3. Read `game/GAME.md` — campaign index, character link, faction/NPC/location directory
4. Summarize where we left off **from the files** (not from memory)
5. Present the current scene with sensory details and available actions

**Load other files on demand, not at startup:**
- Character sheet (`game/characters/player/`) — read before combat, leveling, or detailed mechanical checks
- Location files (`game/locations/`) — read when entering a new location
- `game/campaign/clocks.md` — read at scene boundaries for clock advancement
- `game/campaign/factions.md` — read when faction reputation is relevant
- `game/sessions/journal.md` — read when recalling older events not in current.md
- `game/campaign/world.md` — read for lore, calendar system, or setting details
- NPC files (`game/characters/npcs/`) — do NOT read these yourself; NPC subagents read their own files

6. **NPC Agent System is active.** All named NPC conversations use sub-agents. When the player initiates dialogue with a named NPC, enter dialog mode per the SKILL.md § NPC Behavior — Sub-Agent System you loaded in step 1.

If `game/sessions/current.md` does not exist, tell the player they need to create a campaign first with `/claude-dnd:new-campaign`.
