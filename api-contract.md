# Lucky Block — API Contract

This document defines all communication between the Godot game client and the backend server.
Both teams build to this contract exactly.

---

## Base URL
https://api.luckyblock.gg(Placeholder)

---

## 1. Submit Score

**Endpoint:** POST /api/score/submit

**Game Sends:**
{
  "user_id": "string",
  "score": "integer",
  "game_seed": "string",
  "move_count": "integer",
  "duration_seconds": "integer"
}

**Game Receives:**
{
  "success": "boolean",
  "jackpot_entry": "boolean",
  "jackpot_type": "string (mini | major | mega | null)",
  "current_jackpot_value": "float"
}

---

## 2. Authentication

**Endpoint:** POST /api/auth/login

**Game Sends:**
{
  "device_id": "string"
}

**Game Receives:**
{
  "success": "boolean",
  "user_id": "string",
  "token": "string"
}

---

## 3. Get Leaderboard

**Endpoint:** GET /api/leaderboard

**Game Receives:**
{
  "success": "boolean",
  "players": [
    {
      "username": "string",
      "score": "integer",
      "rank": "integer"
    }
  ]
}

---

## 4. Get Jackpot Status

**Endpoint:** GET /api/jackpot/status

**Game Receives:**
{
  "mini": "float",
  "major": "float",
  "mega": "float"
}
```

---
