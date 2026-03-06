# Quest Design — Secrets-First Protocol

**Every quest must have a defined truth before the player encounters it.** The resolution is decided when the quest is created, then clues are seeded across NPCs, locations, and events.

---

## Creating a Quest

1. **Define the Truth first.** What actually happened or is happening? Who is responsible? Why? Write this before anything else.
2. **Build the Evidence Trail.** Create clues discoverable through different methods:
   - **Observation:** Something visible at a location (tracks, stains, damage)
   - **Investigation:** Something found by searching (hidden objects, documents)
   - **Conversation:** Something an NPC knows (eyewitness, rumor, expertise)
   - **Skill check:** Revealed by a specific ability (Arcana, Survival, Medicine)
   - **Event:** Something that happens while the player is present (the culprit acts again)
3. **Seed NPC Knowledge.** Update relevant NPCs' `## Knowledge` tables with quest-linked info. Most NPCs know fragments, not the full truth.
4. **Seed Location Clues.** Write discoverable clues into relevant location files' `## Quest Clues` section. These should appear naturally in scene descriptions.
5. **Add Red Herrings** (optional, encouraged for Standard+). Misleading details that can be investigated and ruled out.
6. **Set Resolution Conditions.** Success, failure, and partial outcomes.
7. **Create a Tension Clock** if the quest has time pressure.
8. **Update Quest Secrets Summary** in `game/sessions/current.md`.

---

## Quest Difficulty

| Difficulty | Scope | Clues | Template |
|------------|-------|-------|----------|
| Minor | Single scene or conversation | 2-3 | Lightweight (prose) |
| Standard | Multiple scenes, 1-2 sessions | 3-4 | Full |
| Major | Many sessions, multiple locations | 5-7 | Full |
| Arc | Campaign-spanning | 7+ (layered) | Full |

---

## Quest Templates

### Minor Quest (prose format)

Use this for small, contained quests. No tables needed.

```
## <Quest Name>

**Status:** Active | **Given By:** NPC or event | **Reward:** —

**Objective:** What the player needs to do.

**Progress:** Steps completed so far.

### DM Secrets
**Truth:** One sentence — the actual answer.
**Clues:** (1) What and where. (2) What and where.
**Resolution:** What happens on success / failure.
```

### Standard+ Quest (structured format)

Use this for quests that span multiple scenes or sessions. See the template in `quests.md` for the full format with evidence trail table, NPC knowledge seeds, red herrings, and resolution conditions.

---

## Evolving Secrets

- Secrets are **fixed once created**. Do not change the truth mid-quest.
- Completing a quest may reveal a deeper truth → create a new quest with its own secrets.
- Arc quests can spawn Standard sub-quests as layers are peeled back.
- If a quest's truth becomes impossible (player killed the culprit before discovering motive), shift to Partial resolution and note what happened.
- If the player ignores a quest, let the threat clock advance. Consequences create urgency.
