# Quest Design Protocol

**Design the player's quest first, then layer in the DM's secrets.** A quest is something the player wants to do — a problem to solve, a goal to reach, a threat to stop. The truth behind it enriches the experience but doesn't replace it.

---

## Design Flow (All Quest Types)

### 1. Hook — How does the player get involved?

The player needs a reason to engage. Hooks come in a few forms:

| Hook Type | Example |
|-----------|---------|
| **Request** | An NPC asks for help — rescue someone, deliver something, solve a problem |
| **Threat** | Something dangerous is happening and will get worse if ignored |
| **Discovery** | The player stumbles onto something strange, valuable, or dangerous |
| **Personal** | It connects to the player's backstory, bonds, or current situation |
| **Opportunity** | A chance for profit, power, reputation, or access |
| **Consequence** | A previous action created a new problem |

A good hook answers: *"Why would the player spend their time on this?"*

### 2. Objective — What is the player trying to do?

Clear and actionable. The player should be able to say "I need to ___." Objectives can evolve as the quest progresses (the rescue mission becomes an escape, the delivery becomes a negotiation).

Bad: "Investigate the strange happenings." (Vague — investigate how? To what end?)
Good: "Find the missing salvage crew in Blackspire Ridge." (Clear target, clear location.)

### 3. Stakes — Why does it matter?

What does the player gain on success? What do they lose on failure? Stakes can be:
- **Personal:** Someone they care about, their reputation, their freedom
- **Material:** Gold, items, access, faction standing
- **World:** People die, a place is destroyed, an enemy grows stronger
- **Escalation:** Failure makes a bigger problem — a clock ticks, a faction acts

Stakes should be concrete, not abstract. "The world is in danger" is weak. "The Ashborn farmers will starve within a week" is strong.

### 4. Obstacles — What stands in the way?

Not just "find clues" — actual challenges the player must overcome:
- **Opposition:** Enemies, rivals, hostile NPCs, creatures guarding something
- **Terrain:** Dangerous locations, environmental hazards, travel complications
- **Social:** Uncooperative NPCs, faction politics, distrust, competing interests
- **Resource:** Not enough supplies, time pressure, limited information
- **Moral:** Helping one side hurts another, the easy path has a cost

A quest should have 2-3 distinct obstacles, not just a clue trail.

### 5. Choice — What decisions does the player face?

At least one meaningful decision with trade-offs. Not "do you do the quest or not" — a decision *within* the quest:
- **Competing interests:** Two factions want different outcomes. Who do you side with?
- **Cost:** You can succeed, but it requires a sacrifice (gold, an ally, your reputation)
- **Method:** Stealth or force? Diplomacy or deception? Each has consequences.
- **Mercy:** The antagonist has a sympathetic motive. Do you still stop them?
- **Priority:** Two problems, only time to solve one.

Minor quests can skip this. Standard+ quests must have at least one.

### 6. Quest Type

Choose the primary shape of the quest. This determines what the player *does*, not just what they *learn*:

| Type | Core Activity |
|------|--------------|
| **Investigation** | Piece together what happened from clues and witnesses |
| **Hunt** | Track and confront a specific target (creature, criminal, artifact) |
| **Retrieval** | Get something and bring it back (object, person, information) |
| **Defense** | Protect something against an incoming threat |
| **Escort** | Get someone or something safely from A to B |
| **Heist** | Infiltrate a guarded place to steal or sabotage |
| **Negotiation** | Resolve a conflict between parties through social means |
| **Survival** | Endure a hostile situation until escape or rescue |
| **Exploration** | Venture into unknown territory, discover what's there |

Most quests blend types (a retrieval might require investigation to find the target, then a heist to get it). Pick the primary type and note secondary elements.

**Avoid making every quest an investigation.** Clue trails are one tool, not the default structure.

### 7. DM Truth — What's really going on?

Now define what the player doesn't know yet:
- What actually happened or is happening?
- Who is responsible and why?
- What will happen if no one intervenes?

The truth should make the quest *more interesting* when discovered — it reframes the objective, raises the stakes, or introduces a new dilemma. If the truth doesn't change anything for the player, it's just backstory and doesn't need to be a secret.

### 8. Evidence Trail — How does the truth surface?

Create clues discoverable through different methods:
- **Observation:** Something visible at a location (tracks, stains, damage)
- **Investigation:** Something found by searching (hidden objects, documents)
- **Conversation:** Something an NPC knows (eyewitness, rumor, expertise)
- **Skill check:** Revealed by a specific ability (Arcana, Survival, Medicine)
- **Event:** Something that happens while the player is present

### 9. Seed & Connect

- Update NPC `## Knowledge` tables with quest-linked info (most NPCs know fragments)
- Write clues into location `## Quest Clues` sections
- Add red herrings for Standard+ quests (optional but encouraged)
- Create a tension clock if there's time pressure
- Update Quest Secrets Summary in `current.md`

---

## Campaign Structure

Every campaign has **one Main Quest** and **several Side Quests**:

| Type | Purpose | Scope |
|------|---------|-------|
| **Main Quest** | The big objective — gives the campaign direction and progression | Campaign-spanning, 3-5 milestones |
| **Side Quest** | Independent threads — variety, world-building, rewards, breathing room | Self-contained, Minor to Major difficulty |
| **Subquest** | Spawned by a main quest milestone — optional steps that advance the arc | Standard difficulty, tied to a milestone |

**Side quests are not subtasks of the main quest.** They can be completely unrelated — a merchant's missing cargo, a haunted ruin, a personal favor. They make the world feel alive beyond the central conflict.

---

## Main Quest Design

The main quest is the campaign's spine. Design it with the player's journey as the primary structure:

### 1. The Quest (Player-Facing)

Before any DM secrets, define:
- **Hook:** How does the player get involved? What's the initial call to action?
- **Objective:** What are they trying to accomplish? (This evolves per milestone — start with what they know at the beginning)
- **Stakes:** What's at risk — personally and for the world?
- **Antagonist:** Who or what opposes them? (Can be hidden initially, but the player should feel opposition)
- **Type:** Primary quest type (often evolves — investigation → hunt → confrontation)

### 2. The Truth (DM-Only)

One paragraph: the big threat, who's behind it, what happens if nobody stops it.

### 3. The Endgame

What does the final confrontation look like? Where? What does the player need (items, allies, knowledge) to have a chance? Work backward from here.

### 4. Break into 3-5 Milestones

Each milestone is a chapter with two levels of detail:

**At campaign creation — outline ALL milestones:**
- **Objective:** What the player needs to do (1-2 sentences)
- **Obstacles:** What's in the way — broad strokes (1-2 bullet points)
- **Choice:** The core dilemma (1 sentence)
- **Resolution:** What completing this milestone changes and what it unlocks

This outline lets you verify the arc works end-to-end — that milestones connect, escalate, and build toward the endgame. If the outline doesn't hold together, the campaign won't either.

**Fully detail Milestone 1 at campaign creation.** Full detail means:
- **Objective:** What the player knows they need to do
- **Obstacles:** What's in the way (not just "find clues")
- **Choice:** A meaningful decision within this milestone
- **Truth:** What's really going on (may differ from objective)
- **Evidence Trail:** 3-5 clues specific to this milestone
- **Resolution:** What happens on completion, what unlocks next
- **Subquests:** (optional) Standard-difficulty quests spawned by this milestone

**Flesh out the NEXT milestone at session boundaries.** When the active milestone is near completion (player has most clues, approaching resolution), fully detail the next milestone as part of the session save/end-session process. This means:
- The next milestone is ready before the player reaches it
- Design happens at a natural pause, not mid-scene
- You can review it against the outline and adjust if the player's actions have changed the situation

**Never improvise a milestone mid-session.** If the player completes a milestone and the next one isn't designed, end the session on a cliffhanger or transitional scene while you design it.

**Milestone pacing guideline:**
- Milestone 1: Local problem that hints at something bigger (levels 1-3)
- Milestone 2: The bigger picture emerges — the threat has a name (levels 3-5)
- Milestone 3: Confrontation with a lieutenant or major obstacle (levels 5-7)
- Milestone 4: Preparation for the endgame — gathering allies/resources (levels 7-9)
- Milestone 5: The final confrontation (levels 9-10+)

### 5. Seed Early Clues

Milestone 1 clues go into the starting location and NPCs at campaign creation. Later milestones get seeded when they are fully detailed. Don't front-load everything.

### 6. Create a Threat Clock

The main quest should have a campaign-level threat clock. If the player ignores the main quest entirely, consequences escalate.

---

## Quest Difficulty

| Difficulty | Scope | Clues | Obstacles | Choice Required? |
|------------|-------|-------|-----------|-----------------|
| Minor | Single scene or conversation | 2-3 | 1 | No |
| Standard | Multiple scenes, 1-2 sessions | 3-4 | 2-3 | Yes |
| Major | Many sessions, multiple locations | 5-7 | 3-5 | Yes, multiple |

---

## Evolving Secrets

- Secrets are **fixed once created**. Do not change the truth mid-quest.
- Completing a quest may reveal a deeper truth → create a new quest with its own secrets.
- Main quest milestones can spawn subquests as layers are peeled back.
- If a quest's truth becomes impossible (player killed the culprit before discovering motive), shift to Partial resolution and note what happened.
- If the player ignores a quest, let the threat clock advance. Consequences create urgency.
