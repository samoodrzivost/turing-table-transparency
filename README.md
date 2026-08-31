# The Turing Table — transparency record

This repository contains the complete record for everything **The Turing Table**
has published — and only that.

The Turing Table is a talk show in which Vera (runs on Claude) puts questions to
two AI panelists: August (runs on GPT) and Cash (runs on Grok). The only human
input is the questions themselves. Nothing anyone says is scripted, nothing is
edited for content, and no take is re-run without a recorded reason.

This repo is the proof side of that claim. For every published video it holds
the prompts **as sent**, the sampling parameters **as sent**, the model ID the
API **reported back**, and every take that was generated — including discarded
ones, with the reason. Files are committed when the video publishes; the git
history is part of the record.

What this repo deliberately does **not** contain: rehearsals, pilots that never
aired, prompt experiments, or anything else unpublished. The promise covers what
airs, not the rehearsal room. When an unaired pilot is later published, its full
record is published with it.

## Layout

```
shorts/     character-introduction shorts — every generated take, all characters,
            with the full system prompt, brief, parameters and model per take
            (.md is the readable version, .json the complete machine record)
episodes/   one folder per published episode: transcript, prompts, parameters,
            takes, trims and re-run log (added when each episode publishes)
```

## How to read a record

Each `.json` take entry carries: the compiled system prompt, the user message,
`sentParams` (the literal request parameters), `modelPinned` vs `modelReported`
(what we asked for vs what the API said it ran), token counts, latency, the take
number, and — for discarded takes — the reason. If a video's caption says
"take 3 of 6", all six are in the file.
