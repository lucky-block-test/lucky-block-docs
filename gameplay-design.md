# Lucky Block — Gameplay Design

## Overview
Lucky Block is a mobile puzzle game (iOS & Android) built in Godot Engine.
Players place and match blocks on a grid, clear rows, earn scores and coins,
and compete for Solana jackpot payouts.

---

## Game Modes

Lucky Block has two core modes:

| Mode | Theme | Purpose |
|------|-------|---------|
| Classic Mode | Retro Casino (fixed) | Endless jackpot gameplay |
| Adventure Mode | Neon Arcade, Pixel Jungle, Space Station | Theme based progression |

---

## Classic Mode (Endless)

### What it is
Endless puzzle gameplay locked to the Retro Casino theme.
This is the jackpot mode. Every session contributes to the jackpot pool.
The casino aesthetic is permanent here — it reinforces the jackpot experience.

### Gameplay Loop
```
start session
     |
Retro Casino theme loads automatically
     |
place blocks on grid
     |
clear rows
     |
score increases
     |
coins earned
     |
jackpot entry calculated
     |
session ends
     |
score submitted to backend
```

### What the player earns
- Score (leaderboard ranking)
- Coins (used to unlock Adventure themes)
- Jackpot entries (based on score thresholds)

### Jackpot Types

| Type | Trigger |
|------|---------|
| Mini Jackpot | Score threshold reached in session |
| Major Jackpot | Random lucky trigger during gameplay |
| Mega Jackpot | Global pool reaches milestone |

### Jackpot Visual
Massive pixel slot machine hits 777.
Coin shower animation.
Casino bells sound effect.
Lucky Dog in tuxedo celebrates.

### Special Block — Wild Block
- Acts as any color, completes any match
- Animation: Slot machine spin before locking into color

---

## Adventure Mode (Theme Based)

### What it is
Theme based puzzle gameplay with unlock progression.
Players unlock and play across 3 unique worlds.
Each world has its own visual identity, soundtrack,
Lucky Dog costume, and unique special block.

### Gameplay Loop
```
select unlocked theme
     |
enter theme world
     |
place blocks on grid
     |
clear rows
     |
reach target score to unlock next theme
     |
earn coins and rewards
     |
unlock next theme
```

### Unlock Path
```
Neon Arcade    ✅ Unlocked by default
     |
     |--- Collect 500 coins OR reach 5,000 score in one session
     v
Pixel Jungle   🔒
     |
     |--- Reach 10,000 score in one session
     v
Space Station  🔒
```

---

## Adventure Themes

### 1. Neon Arcade
- Status: Unlocked by default
- Visual: Neon city, arcade machines, electric colors
- Soundtrack: Synthwave / electronic
- Lucky Dog Costume: Arcade jacket
- Jackpot Visual: Giant glowing arcade machine
- Special Block: **Zapper Block**
  - Clears the entire column when matched
  - Animation: Electric shock down the column

### 2. Pixel Jungle
- Status: Locked
- Unlock Condition: Collect 500 coins OR reach 5,000 score in one session
- Visual: Ancient jungle, treasure, golden ruins
- Soundtrack: Jungle drums, tribal beats
- Lucky Dog Costume: Explorer hat
- Jackpot Visual: Ancient treasure chest
- Special Block: **Vine Block**
  - Connects to all adjacent blocks and clears them together
  - Animation: Lucky Dog digs it up, vines spread outward

### 3. Space Station
- Status: Locked
- Unlock Condition: Reach 10,000 score in one session
- Visual: Cosmic environment, energy cores, stars
- Soundtrack: Ambient space music
- Lucky Dog Costume: Astronaut suit
- Jackpot Visual: Cosmic energy reactor
- Special Block: **Gravity Block**
  - Temporarily flips the board direction
  - Animation: Zero gravity effect, blocks float upward briefly

---

## Special Blocks Summary

| Mode | Theme | Block Name | Ability |
|------|-------|-----------|---------|
| Classic | Retro Casino | Wild Block | Acts as any color |
| Adventure | Neon Arcade | Zapper Block | Clears entire column |
| Adventure | Pixel Jungle | Vine Block | Clears all adjacent blocks |
| Adventure | Space Station | Gravity Block | Flips board direction temporarily |

---

## Lucky Dog

Lucky Dog is the game mascot present in every theme.

### Roles
- Reacts to big combos
- Celebrates jackpot wins
- Guides theme unlock challenges
- Has a unique costume per theme

### Costumes

| Mode | Theme | Costume |
|------|-------|---------|
| Classic | Retro Casino | Tuxedo |
| Adventure | Neon Arcade | Arcade jacket |
| Adventure | Pixel Jungle | Explorer hat |
| Adventure | Space Station | Astronaut suit |

---

## Scoring Rules

- Row clear = base points
- Combo clears = score multiplier
- Special block activation = bonus points
- Score determines jackpot entry tier in Classic Mode
- Score determines theme unlock eligibility in Adventure Mode

