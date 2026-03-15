# Lucky Block — System Architecture

## High Level Flow

Mobile Game (Godot)
        |
        | HTTPS API
        v
Game Backend (Node.js)
        |
        | Redis Queue
        v
Jackpot Engine
        |
        | Bridge Service
        v
Solana Network

## Core Principles

1. Gameplay is fully off-chain
2. Backend validates all scores
3. Blockchain layer only handles payouts
4. Game never touches blockchain directly
```

---
