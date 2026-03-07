# Game Systems

## Encounter Balance

1. Reference the player's character level from their character sheet
2. Use the CR system for encounter difficulty (solo-adjusted — one step lower than standard):
   - **Easy:** CR = level - 3 (or multiple very weak enemies)
   - **Medium:** CR = level - 2
   - **Hard:** CR = level - 1
   - **Deadly:** CR = level to level + 1
3. For solo play, lean toward Medium encounters with occasional Hard
4. Adjust on the fly if the player is struggling or breezing through
5. Ensure encounters serve the narrative, not just combat quotas
6. For detailed CR benchmarks, see [encounter-guidelines.md](encounter-guidelines.md)

---

## Solo Play Rules

Since this is a solo campaign (one PC, no party), these rules keep things viable:

### Sidekick Option
- At campaign start or when narratively appropriate, offer the player a sidekick NPC
- Sidekick uses simplified Tasha's rules: **Warrior** (melee/tank), **Expert** (skills/utility), or **Spellcaster** (support/healing)
- The sidekick is DM-controlled but follows the player's lead in combat and exploration
- The sidekick has their own character file in `game/characters/npcs/`
- The sidekick levels up with the player and has their own personality, but defers to the PC for decisions

### Safety Net
- When the solo PC drops to 0 HP **outside of combat**, they automatically stabilize (no death saves) — they're alone, no one is finishing them off unless narratively forced (e.g., assassination, trap)
- In combat, standard death save rules apply

### Healing Access
- If no healer is in the party, healing potions are **common loot** and always available at shops
- Short rests are encouraged — remind the player when appropriate

---

## Tension Clocks

Clocks track off-screen threats, player progress, and faction agendas. Tracked in `game/campaign/clocks.md`.

### How Clocks Work
- Each clock has a name, type (Threat/Progress/Faction), segments (4/6/8), and current fill
- Clocks advance on defined triggers: time passing, player actions, faction moves, failed checks
- When a clock fills -> its consequence fires (narrative event, encounter, faction shift, quest change)

### When to Advance Clocks
- **At each scene boundary checkpoint:** Check all active clocks — did any triggers occur?
- **When significant time passes:** Travel, rests, downtime — advance time-based clocks
- **After major player actions:** Success or failure on quests, faction interactions
- **At each dawn** (in-world): Advance any daily clocks

### Creating Clocks
- Create clocks when introducing threats, faction agendas, or long-term goals
- Match segment count to urgency: 4 (imminent), 6 (standard), 8 (slow burn)
- Always define the consequence before starting the clock

---

## Random Events & Encounters

The world moves and surprises. Random tables in [random-tables.md](random-tables.md) keep things dynamic.

### When to Roll
- **Entering a new scene** (after a scene transition)
- **After a rest** (short or long)
- **During travel** (once per leg of the journey)

### How to Roll

**Do not announce random event rolls to the player.** Roll silently and weave the result into the narration. The player should never see "Let me roll a random event" — just the scene.

1. Roll d20
2. On **1-10:** Nothing notable — describe the atmosphere, move on
3. On **11-20:** Use the corresponding entry from the relevant table (Town, Road, Wilderness, Dungeon). **Do not show the raw table entry to the player** — it is DM-facing only.
4. **Narrate the scene first**, then prompt for any required rolls. Describe what happens in the fiction — the player should feel the danger before seeing the dice. Apply the table entry's full mechanical effect (saves, combat, skill checks, hazards). Do not skip mechanics for flavor-only narration.
5. **Quest-like encounter?** If the encounter has mystery, ongoing threat, or investigation potential that won't resolve in this scene, **pause narration and create a quest** following the quest-design protocol in `${CLAUDE_SKILL_DIR}/quest-design.md` (Minor difficulty fits most random encounters). Define the truth and write all quest files before the player interacts with it. Then narrate the hook.
6. **Check active quest secrets** — if the random event can plausibly connect to a quest's evidence trail, use it to surface a clue or reinforce the quest's truth. Aim for ~1 in 3 random events to tie back to an active quest.
7. Expand the seed narratively — tie it to active quests, clocks, or factions when possible
8. Not every random event needs to be combat — most are flavor, information, or choice

---

## Reputation System

Track how factions and organizations view the player. Managed in `game/campaign/factions.md`.

### Reputation Scale

| Score | Tier | Description |
|-------|------|-------------|
| -5 | Nemesis | Active war — faction will spend resources to destroy the player |
| -4/-3 | Hostile | Kill on sight, bounties, sabotage |
| -2/-1 | Unfriendly | Refuses service, may report player, increased prices |
| 0 | Unknown | No relationship — neutral default |
| +1/+2 | Friendly | Willing to trade, share public info, offer minor aid |
| +3/+4 | Trusted | Offers quests, discounts, safe houses, shares secrets |
| +5 | Champion | Full faction resources available, seats at the table, legend status |

### What Shifts Reputation
- Completing a faction quest: **+1 to +2**
- Significant favor or gift: **+1**
- Saving a faction member's life: **+1 to +2**
- Betraying the faction: **-2 to -3**
- Attacking faction members: **-3**
- Working with a rival faction (if discovered): **-1 to -2**
- Public act aligned with faction values: **+1**
- Public act against faction values: **-1**

### Threshold Effects
- **+2:** Faction offers side quests and discounts (10-20% off)
- **+4:** Access to faction secrets, safe houses, and restricted resources
- **-2:** Faction refuses service; NPCs are cold or dismissive
- **-4:** Faction actively works against the player (sends agents, spreads rumors, blocks resources)

### NPC vs Faction Disposition
- Individual NPC disposition is tracked separately in their `.md` file
- An NPC can like the player even if their faction doesn't (and vice versa)
- Faction reputation sets the default; personal interactions adjust from there

---

## Time & Calendar

Track the passage of in-world time. The current date and time are recorded in `game/campaign/world.md` under the Calendar section.

### Time Rules
- **Advance time explicitly:** Travel, rests, downtime, and waiting all cost time. Announce it: *"Two days pass on the road..."*
- **Short rest** = 1 hour | **Long rest** = 8 hours
- **Travel time** = per the connection table in location files
- **Downtime** = the player declares how long; advance accordingly

### At Each Dawn (In-World)
1. Advance any time-based tension clocks
2. Check for random events if the situation warrants it
3. Update the calendar in `world.md`

### World Advancement
When significant time passes (days or more):
- Advance faction clocks in `game/campaign/clocks.md`
- Update NPC situations if their goals would have progressed
- The world doesn't wait — threats advance, NPCs pursue their own agendas, situations evolve
- Briefly narrate what has changed when the player next interacts with affected elements
