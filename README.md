# claude-dnd

A D&D 5e game engine plugin for [Claude Code](https://claude.com/claude-code). Claude becomes your Dungeon Master — all game state lives in markdown files, with transparent dice rolling and full 5e rules.

## What is this?

[Claude Code](https://docs.anthropic.com/en/docs/claude-code) is Anthropic's CLI tool for working with Claude in your terminal. It supports **plugins** — packages that give Claude new skills and commands.

This plugin turns Claude into a D&D 5th Edition Dungeon Master. You play a solo campaign in your terminal, and the entire campaign state is stored as plain markdown files you can read, edit, and version-control with git.

## Features

- **Persistent world state in markdown** — Characters, NPCs, locations, quests, inventory, and session history all live in `game/` as `.md` files. Game state is only what's written in the files.
- **Full 5e rules engine** — Combat, spells, ability checks, death saves, and more following Rules as Written from the Player's Handbook.
- **Transparent dice rolls** — A dedicated `roll` script handles all dice with batch support: attacks, damage, initiative, advantage/disadvantage, and ability score generation in a single call.
- **Secrets-first quest design** — Every quest has a pre-defined truth, evidence trail, and NPC knowledge seeds baked in at creation. Clues are seeded across locations and NPCs, producing coherent mysteries instead of improvised narratives.
- **NPC sub-agent system** — Each named NPC is played by a dedicated sub-agent that stays in character, only knows what the NPC would know, and maintains its own conversation history.
- **Tension clocks** — Off-screen threats and faction agendas advance based on triggers, even when you're not interacting with them.
- **Faction reputation system** — Your actions shift how organizations treat you, from Nemesis (-5) to Champion (+5), with mechanical effects at each tier.
- **Random event tables** — Town, road, wilderness, and dungeon encounter tables that tie into active quest threads.
- **Solo-play balanced** — Encounter difficulty, healing access, and safety nets tuned for a single player character.
- **Session save/restore** — Save mid-session and pick up where you left off, even across conversations.
- **Git-friendly** — Plain text means you can commit your campaign, branch timelines, or share saves.

## Install

In Claude Code, run `/plugin`, select **Marketplace**, and paste:

```
https://github.com/SergeyKhval/claude-dnd
```

Or load locally with `claude --plugin-dir /path/to/claude-dnd`.

## Quick start

```
/claude-dnd:new-campaign
```

That's it. You'll build the world and your character together, then start playing.

## Commands

| Command | What it does |
|---------|-------------|
| `/claude-dnd:new-campaign` | Create a new world and character |
| `/claude-dnd:start-session` | Resume from your last save |
| `/claude-dnd:add-quest [count]` | Add new quests mid-campaign |
| `/claude-dnd:save` | Save progress mid-session |
| `/claude-dnd:end-session` | Save + narrative wrap-up |

Between commands, just talk — the DM runs automatically during gameplay.
