# ClaudeCodeTest

A collection of standalone HTML5 browser games. No build step, no dependencies — just open a file in your browser.

## Games

### Pixel Siege (`shooter.html`)

A retro top-down arcade shooter with a green scanline aesthetic.

**How to play:**
- `WASD` / Arrow Keys — move
- Mouse — aim
- Click — fire
- `Enter` — start / advance to next sector
- `R` — restart after game over or victory

**Enemies:**
| Enemy | Shape | HP | Behavior |
|---|---|---|---|
| Chaser | Red square | 1 | Charges directly at the player |
| Zigzagger | Cyan triangle | 1 | Approaches with lateral weaving |
| Turret | Magenta octagon | 3 | Stationary; fires back at player every 2s |

**Progression:** 3 sectors of increasing difficulty. Survive all waves in a sector to advance. Score is cumulative across sectors (100–500 pts per enemy).

---

### Tic Tac Toe (`tictactoe.html`)

Classic two-player Tic Tac Toe.

- Click a cell to place your mark (X goes first)
- Win/loss/tie scores persist across games in the same session
- Click **New Game** to reset the board

## Running

Open either `.html` file directly in any modern browser — no server required.
