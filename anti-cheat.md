# Lucky Block — Anti-Cheat Rules

## Game Side (Godot Developer)

- Generate a random game_seed at session start
- Track move_count throughout gameplay
- Track duration_seconds of session
- Send all of these with every score submission

## Backend Side

- Replay score using game_seed to verify legitimacy
- Reject scores that don't match expected progression
- Rate limit score submissions per user
- Flag duplicate submissions

## Blockchain Side

- Payout cannot be claimed twice
- Jackpot contract cannot be drained externally
- All transactions are logged on-chain
