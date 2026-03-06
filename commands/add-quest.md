---
description: Add new quests to the campaign using the secrets-first protocol
args: count
disable-model-invocation: true
---

# Add Quests

Add {{ count | default: 1 }} new quest(s) to the campaign.

## Steps

1. **Read context:** Load `game/sessions/current.md`, `game/campaign/quests.md`, and `game/GAME.md` to understand the current campaign state, active quests, and world.

2. **Read the quest design protocol:** `${CLAUDE_PLUGIN_ROOT}/skills/dm/quest-design.md` — follow it exactly.

3. **For each quest to create:**
   a. Collaborate with the player on what kind of quest they want (or propose options that fit the current narrative). Ask about preferred difficulty (Minor / Standard / Major / Arc).
   b. **Define the Truth first** — the actual resolution, before writing anything else.
   c. Build the evidence trail, seed NPC knowledge, and seed location clues per the protocol.
   d. Use the **Minor (prose) template** for Minor quests, **structured template** for Standard+.
   e. Write the quest to `game/campaign/quests.md` under Active Quests.
   f. Update relevant NPC files' `## Knowledge` tables with quest-linked information.
   g. Update relevant location files' `## Quest Clues` tables with seeded clues.
   h. Create a tension clock in `game/campaign/clocks.md` if the quest has time pressure.
   i. Update the Quest Secrets Summary in `game/sessions/current.md`.

4. **Update `game/GAME.md`** if new NPCs or locations were created.

5. **Present the quest hook** to the player narratively — describe how they learn about it in-world. Do NOT reveal any DM Secrets.
