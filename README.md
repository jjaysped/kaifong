# Kaifong 街坊

A daily Hong Kong geography game. Five prompts a day, 25 seconds each. Any correct answer scores, but the rarer it is, the more it's worth.

| Points | Tier |
|---|---|
| 10 | Tourist 遊客 |
| 30 | Local 本地人 |
| 60 | Kaifong 街坊 |
| 85 | Old Hand 老香港 |
| 100 | One in 7.5 Million 七百五十萬分之一 |

## Files

- `index.html` — the game (static, no build step)
- `puzzles.json` — every day's prompts, keyed by date (`YYYY-MM-DD`, Hong Kong time)

## Adding a day

Add an entry to `puzzles.json`:

```json
"2026-11-08": {
  "date": "2026-11-08",
  "prompts": [
    {
      "id": "p1",
      "q": "Name an MTR station on the Island Line",
      "qzh": "說出一個港島綫車站",
      "answers": [
        { "en": "Heng Fa Chuen", "zh": "杏花邨", "tier": 100, "aliases": ["HFC"] }
      ]
    }
  ]
}
```

`aliases` are extra spellings that also count. `"check": true` marks an answer that still needs verifying against an official source.

## Deploying

Hosted on Vercel. Every push to `main` redeploys automatically.
