# claude-dnd

A D&D 5e game engine plugin for [Claude Code](https://claude.com/claude-code). Claude becomes your Dungeon Master — all game state lives in markdown files, with transparent dice rolling and full 5e rules.

## Install

In Claude Code, run `/plugin` and add this marketplace URL:

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
| `/claude-dnd:save` | Save progress mid-session |
| `/claude-dnd:end-session` | Save + narrative wrap-up |

Between commands, just talk — the DM runs automatically during gameplay.
