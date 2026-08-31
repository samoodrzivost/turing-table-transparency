# Pilot episode — complete record

- `transcript.md` — every aired turn, verbatim, in order.
- `record.json` — the full machine record: per turn, the system prompt and user
  message **as sent**, the sampling parameters **as sent**, the model the API
  **reported**, tokens, latency, take number and status; plus all trims and
  discarded takes (this episode: 1 trims, 0 discarded takes).

Engines, as recorded per turn:
- August — gpt-5-2025-08-07
- Cash — grok-4.3
- Vera — claude-opus-5

The cold open in the video is a continuous verbatim excerpt of two turns that
air in full later in the episode (turn ids in `record.json`); it is a cut, not
an edit — word deletions at the boundaries only.

SHA-256 at publish:
- transcript.md `ea7396665ed2c4136e6c02d27f0fabe25015e9e8192a55e116419868a7107e40`
- record.json `3ad25d8253a36bdcffc57b0743cd8412e02d45884507077d6b0be74e2a374de9`
