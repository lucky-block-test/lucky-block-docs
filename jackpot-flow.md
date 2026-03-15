# Lucky Block — Jackpot Flow

## How Jackpots Work

1. Player completes a game session
2. Game submits score to backend
3. Backend validates score
4. Backend records jackpot entry
5. Jackpot pool increases
6. Trigger condition is met
7. Backend selects winner
8. Bridge service sends payout on Solana
9. Backend notifies game client
10. Game displays jackpot win animation

## Jackpot Types

| Type | Trigger |
|------|---------|
| Mini | Score threshold reached |
| Major | Random lucky trigger |
| Mega | Global pool milestone |

## Security Rules
- Payout cannot be triggered from game client directly
- All triggers go through backend validation
- Blockchain developer owns everything after step 7
```
