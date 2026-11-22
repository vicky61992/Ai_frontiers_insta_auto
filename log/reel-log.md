# @ai_frontiers_ Reel log

Rule: 2 VALUE Reels : 1 WORKSHOP AD Reel. Never repeat a topic.

| Date | Type | Topic | Status | Permalink |
|---|---|---|---|---|
| 2026-11-10 | VALUE | Gemini Notebook (NotebookLM) PDF → podcast/quiz | Posted | https://www.instagram.com/reel/DfjyQxYFKgY/ |
| 2026-11-11 | VALUE | Google AI Plus free for students | Posted | https://www.instagram.com/reel/DfmyOe5zGMs/ |
| 2026-11-12 | VALUE | ChatGPT prompt galti (better prompts) | Posted | https://www.instagram.com/reel/DfpkLnjTX3J/ |
| (earlier) | VALUE | Gemini Canvas sketch-to-app; Google Vids free AI video | Used topics | - |
| 2026-11-14 | WORKSHOP AD | Zero-Code AI Workshop, 22–23 Nov, ₹199 | Posted | https://www.instagram.com/reel/DfuHkWFmQ1W/ |
| 2026-11-15 | VALUE | Gemini Canvas sketch-to-app | Posted | https://www.instagram.com/reel/Dfv2sRrzVYw/ |
| 2026-11-15 | VALUE | Google Vids free AI video (3/month) | Posted | https://www.instagram.com/reel/Dfv2hcQz_Dz/ |
| 2026-11-17 | WORKSHOP AD | Zero-Code AI Workshop (3D/pizza-price hook) | Posted | https://www.instagram.com/reel/Df2VspfDLzh/ |
| 2026-11-20 | VALUE | Gemini Tasks free in India (bg multi-step agent) | Posted | https://www.instagram.com/reel/Df9zwpigAZT/ |
| 2026-11-21 | WORKSHOP AD | Zero-Code AI Workshop (weekend/calendar hook, batch 28-29 Nov per new date rule) | Posted | https://www.instagram.com/reel/Df_eqsMAKc9/ |
| 2026-11-22 | VALUE | Jio free Google Gemini Pro (18mo, worth ₹35,100, incl. Gemini 3 + 2TB storage) | Posted | https://www.instagram.com/reel/DgDG9jNDP4X/ |

Next type due: VALUE (then WORKSHOP AD) — 1 VALUE reel owed before next ad, per the 2:1 ratio.

2026-11-10 gemini-notebook-v3.mp4 / -v4.mp4: earlier draft iterations of the already-posted Gemini Notebook reel (DfjyQxYFKgY) — not separate pending posts, do not publish.

## Notes
- Voice: gemini-3.8-flash-tts, Puck, one request per scene ~25 s apart (429 on back-to-back calls; retry after ~20–40 s). Keep only WAV data chunk.
- STT QA: gemini-3.5-flash.
- Renderer: Python + PIL + ffmpeg, navy+gold, cover first 3 s, synthesized music ducked.
- rocket-launch-register.lovable.app is not reachable from the cloud sandbox (network allowlist); workshop details taken from earlier captions.
- **STT QA false positive (2026-11-22):** gemini-3.5-flash STT consistently mis-transcribes a spoken "Gemini 3" (or "Gemini Three") as a different known model name ("Gemini 1.5 Pro", "Gemini Advanced") — reproduced across many retries/rewordings, so it's an STT-model prior/hallucination on that specific brand+digit, not a bad TTS clip. Workaround that transcribes cleanly every time: phrase it as "...नंबर 3 वाला..." (lit. "the one numbered 3") instead of "Gemini 3"/"Gemini Three" directly adjacent to "Gemini".
- **Sandbox Python/Pillow bug:** this environment's default `python3` (3.11) resolves `PIL` to a broken system install at `/usr/lib/python3/dist-packages/PIL` (no compiled `_imaging`, import fails) even after `pip install pillow`, because pip sees that broken copy as "already satisfied" and skips it. Fix: `python3.11 -m pip install --force-reinstall --no-deps pillow`, then always invoke render scripts as `python3.11` (not the `/usr/local/bin/python3` → 3.13 alias) so numpy/PIL/requests all resolve to the same working interpreter.
- **Git branch note:** `origin/main` is behind this repo's `claude/vibrant-mendel-idgw86` branch (missing the last several reel-adding commits/files, going back to the Nano Banana reel) — this session's harness only allows pushing to `claude/vibrant-mendel-idgw86`, not `main`. The reel .mp4 was committed there (not `/main/`) for history/backup; actual Instagram hosting used `vidiq_video_upload` with `localFile` (direct upload from the sandbox to vidIQ's own storage), not a GitHub raw URL. Vicky: merge `claude/vibrant-mendel-idgw86` into `main` if you want the two branches back in sync.

## WORKSHOP BATCH DATE RULE (set 2026-11-20, Vicky's instruction — do not hardcode a fixed date again)
Every month has TWO batches, always:
- Batch A: the 2nd Saturday–Sunday of the month
- Batch B: the 4th Saturday–Sunday of the month
("2nd Saturday" = the 2nd Saturday counting from day 1 of that month; the batch is that Saturday + the next day, Sunday.)

For every new WORKSHOP AD Reel: compute TODAY's date, find the next upcoming batch (A or B, whichever comes first that hasn't already passed/started), and use ONLY that batch's real calendar dates in the script/caption. Never reuse a date from a previous Reel once it has passed. If genuinely unsure which batch is "next" (e.g. today falls between the two), ask Vicky once rather than guessing.

Time: 6–9 PM IST. Price: ₹199 (reg ₹599) unless Vicky has said a new price in this chat. Register at https://rocket-launch-register.lovable.app.

Example (do NOT hardcode this — recompute live each time): for December 2026, Batch A = 12–13 Dec, Batch B = 26–27 Dec.
