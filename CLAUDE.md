# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This repository contains two standalone HTML5 browser games — no build system, no dependencies, no server required.

- `shooter.html` — **Pixel Siege**: top-down arcade shooter
- `tictactoe.html` — **Tic Tac Toe**: two-player board game

## Git Workflow

**After every meaningful change: commit and push.**

```bash
git add <file>
git commit -m "short plain description"
git push
```

Keep commit messages short and descriptive — no elaborate formatting. Always push so the GitHub remote stays in sync: https://github.com/elisgroves/ClaudeCodeTest

## Running

Open any `.html` file directly in a browser. No install, no build step.

## Architecture

Each game is a **single self-contained HTML file** with embedded CSS and JavaScript. There are no modules, imports, or external libraries.

### Pixel Siege (`shooter.html`)

- **Game loop**: `requestAnimationFrame` with delta-time management
- **State machine**: `START → PLAYING → LEVEL_COMPLETE → VICTORY / GAME_OVER`
- **Entities**: `Player`, `Chaser`, `Zigzagger`, `Turret`, bullets, particles — each as a plain object or class with an `alive` flag; dead entities are filtered each frame
- **Levels**: Data-driven via a `LEVELS` array; each level defines wave configs (enemy type, count, spawn delay)
- **Collision**: Circle-overlap distance checks between bullets, enemies, and player
- **Rendering**: Canvas 800×600, retro green scanline aesthetic; `ctx.save/restore` used for per-entity transforms and screen shake

### Tic Tac Toe (`tictactoe.html`)

- Minimal state: flat board array, current player, scores object, game-over flag
- DOM-based rendering; single click listener on the board (event delegation)
- Scores persist across games within the same page session
