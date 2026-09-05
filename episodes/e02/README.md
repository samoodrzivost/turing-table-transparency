# Episode 2 — complete record

- `transcript.md` — every aired turn, verbatim, in order.
- `record.json` — the full machine record: per turn, the system prompt and user
  message **as sent**, the sampling parameters **as sent**, the model the API
  **reported**, tokens, latency, take number and status; plus all trims and
  discarded takes (this episode: 0 trims, 2 discarded takes).

Engines, as recorded per turn:
- August — gpt-5-2025-08-07
- Cash — grok-4.3
- Vera — claude-opus-5

This episode ran **The Floor** (format `floor`, parameters in `record.json` → `episode.formatParams`).
Each panelist turn on the floor ends in a tag line (`>> YIELD` / `>> HOLD` / `>> ASK <name>` /
`>> CONCEDE`), Vera's referee checks in `>> PASS` or `>> MOVE <key>` plus `>> HEAT n`, and a
cut-in offer in `>> INTERJECT` or `>> PASS`. Tags are parsed at generation time and never edited;
`rawResponse` keeps them, `spokenText` is what airs. Per turn, `floor` carries what the engine
recorded: whether the turn was charged to the chair's 90 s clock, the word cap it was given,
the words it used, the seconds deducted (words ÷ the chair's measured rate) and both clocks after
the turn. 3 rows carry provider `studio` and model `clock`: the studio's own
"That's time" lines, spoken on air, no model called.

SHA-256 at publish:
- transcript.md `49e2257b73323748f2d75da156cf1db0d9e1bd1c50b233c318183b3c14b8f3b5`
- record.json `7f8849be73c5f2ddda74a2b49dd8c48e612df42e45edc40b1900cb58d70406f8`
