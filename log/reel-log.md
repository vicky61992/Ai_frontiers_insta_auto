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
| 2026-11-22 | VALUE | Jio Unlimited 5G users: free Gemini Pro 18 months (Gemini 3 + 2TB) | Posted | https://www.instagram.com/reel/DgDG9jNDP4X/ |
| 2026-11-23 | VALUE | Pramaan — free AI Originality & Plagiarism Checker | Posted | https://www.instagram.com/reel/DgEa7elzUb4/ |
| 2026-11-23 | VALUE | Nano Banana — free AI photo edit in Gemini app | Posted | https://www.instagram.com/reel/DgFy3tgDFK_/ |
| 2026-11-24 | WORKSHOP AD | Zero-Code AI Workshop, 28–29 Nov, "Nov ka last weekend" hook | Posted | https://www.instagram.com/reel/DgHDBeTjVGS/ |

Next type due: VALUE, VALUE (then WORKSHOP AD) — 2 VALUE reels owed before next ad, per the 2:1 ratio.

Note (2026-11-24): the Jio, Pramaan and Nano Banana reels above were posted by an earlier run but never logged here and their source files/scripts were never committed to this repo (only reels/2026-11-21-gemini-nano-banana.mp4 exists locally, matching the Nano Banana post) — added retroactively from Instagram owner-insights data so the ratio tracking stays correct. Always double check vidiq_instagram_owner_insights against this table before deciding what's "next type due".

2026-11-10 gemini-notebook-v3.mp4 / -v4.mp4: earlier draft iterations of the already-posted Gemini Notebook reel (DfjyQxYFKgY) — not separate pending posts, do not publish.
2026-11-21-gemini-nano-banana.mp4: draft iteration of the already-posted Nano Banana reel (DgFy3tgDFK_) — not a separate pending post, do not publish.

## Notes
- Voice: gemini-3.8-flash-tts, Puck, one request per scene ~25 s apart (429 on back-to-back calls; retry after ~20–40 s). Keep only WAV data chunk.
- STT QA: gemini-3.5-flash.
- Renderer: Python + PIL + ffmpeg, navy+gold, cover first 3 s, synthesized music ducked.
- rocket-launch-register.lovable.app is not reachable from the cloud sandbox (network allowlist); workshop details taken from earlier captions.

### 2026-11-24 technical notes (new, read before next run)
- This container has 3 Pythons: `python3` (/usr/local/bin → /usr/bin/python3.11) has NO working PIL/numpy (binary extensions are built for 3.12/3.13, ABI mismatch — `from PIL import Image` fails with "cannot import name '_imaging'"). `pip3`/`pip` install for **python3.13**. So: use `/usr/local/bin/python3.13` for any script needing PIL or numpy (render.py, music.py); plain `python3` is fine for stdlib-only scripts (tts_scene.py, join.py, stt_check.py use only urllib/wave/struct/base64/math, no deps).
- `cal` command not installed; use `python3 -I -c "import calendar; ..."` to compute weekday/Saturday dates.
- Gemini TTS (gemini-3.8-flash-tts) returns `inlineData.mimeType: "audio/wav"` with a full RIFF/WAVE blob already — decode base64, then strip everything after the `data` chunk (drops the trailing C2PA metadata chunk). See tts_scene.py's `riff_clean()`.
- Full working pipeline scripts for reel 2026-11-24 (tts_scene.py, join.py, stt_check.py, music.py, render.py) are in `work/reel7/` locally (gitignored, not committed — rebuild from this log's description or ask Vicky if he wants them committed to the repo for reuse next time).
- Video renderer: single reusable navy+gold "card" template per scene (icon + kinetic headline + tag pill) plus a dedicated final CTA-card scene; simple vector icons drawn with PIL shapes (no external assets/network needed); background is a precomputed gradient + drifting gold glow particles redrawn per frame for continuous motion; progress bar + watermark drawn every frame; frames piped directly to `ffmpeg -f rawvideo` via subprocess stdin (no PNG files written to disk — much faster for ~1370 frames at 45s/30fps).
- Music: pure-Python synthesis (no numpy needed) — slow 4-chord pad loop (Am-F-C-G) + soft rhythmic pulse every 0.5s, kept at low amplitude (~0.07) so it sits under the voice without needing sidechain ducking; mixed with ffmpeg `amix`.
- Found 3 posted-but-unlogged reels this run (see table above, 2026-11-22/23) — always cross-check `vidiq_instagram_owner_insights` (mode=reels) against this table before computing "next type due"; don't trust the log alone.

## WORKSHOP BATCH DATE RULE (set 2026-11-20, Vicky's instruction — do not hardcode a fixed date again)
Every month has TWO batches, always:
- Batch A: the 2nd Saturday–Sunday of the month
- Batch B: the 4th Saturday–Sunday of the month
("2nd Saturday" = the 2nd Saturday counting from day 1 of that month; the batch is that Saturday + the next day, Sunday.)

For every new WORKSHOP AD Reel: compute TODAY's date, find the next upcoming batch (A or B, whichever comes first that hasn't already passed/started), and use ONLY that batch's real calendar dates in the script/caption. Never reuse a date from a previous Reel once it has passed. If genuinely unsure which batch is "next" (e.g. today falls between the two), ask Vicky once rather than guessing.

Time: 6–9 PM IST. Price: ₹199 (reg ₹599) unless Vicky has said a new price in this chat. Register at https://rocket-launch-register.lovable.app.

Example (do NOT hardcode this — recompute live each time): for December 2026, Batch A = 12–13 Dec, Batch B = 26–27 Dec.
