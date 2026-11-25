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
| 2026-11-23 | VALUE | Pramaan — AI Originality & Plagiarism Checker | Posted | https://www.instagram.com/reel/DgEa7elzUb4/ |
| 2026-11-23 | VALUE | Nano Banana (Gemini free photo-fix trick) | Posted | https://www.instagram.com/reel/DgFy3tgDFK_/ |
| 2026-11-24 | WORKSHOP AD | Zero-Code AI Workshop ("Nov ka last weekend" hook, batch 28-29 Nov) | Posted | https://www.instagram.com/reel/DgHDBeTjVGS/ |
| 2026-11-25 | VALUE | ChatGPT Study Mode (free built-in tutor mode) | Rendered, awaiting Vicky yes | - |

Next type due: VALUE (then WORKSHOP AD) — 1 VALUE reel owed before next ad, per the 2:1 ratio (once 2026-11-25 is posted).

2026-11-10 gemini-notebook-v3.mp4 / -v4.mp4: earlier draft iterations of the already-posted Gemini Notebook reel (DfjyQxYFKgY) — not separate pending posts, do not publish.

2026-11-23/24 entries were reconstructed on 2026-11-25 from vidiq_instagram_owner_insights (live IG data) — the session(s) that made and posted those 3 reels never committed their files or updated this log, so this repo has no video/script record for them. reels/2026-11-21-gemini-nano-banana.mp4 is a leftover unused draft from that gap (never sent to Vicky, never posted) — it is NOT the Nano Banana reel that actually went live (DgFy3tgDFK_, posted 2026-11-23); do not publish it, it can be deleted whenever convenient.

## Notes
- Voice: gemini-3.8-flash-tts, Puck, one request per scene ~25 s apart (429 on back-to-back calls; retry after ~20–40 s). Keep only WAV data chunk.
- STT QA: gemini-3.5-flash.
- Renderer: Python + PIL + ffmpeg, navy+gold, cover first 3 s, synthesized music ducked.
- rocket-launch-register.lovable.app is not reachable from the cloud sandbox (network allowlist); workshop details taken from earlier captions.
- 2026-11-25: default `python3` (3.11) has a broken Pillow (missing matching `_imaging` .so for that interpreter) in this sandbox — use `python3.13` instead, which has a working Pillow install. `numpy` is not installed; wrote the background-music synth in pure Python (no numpy) instead.
- Render approach that worked well: per-scene icon/motion drawn with PIL primitives only (no emoji font — compositing color-emoji glyphs is unreliable), full video rendered frame-by-frame at 30fps (1275 frames in ~30s on this box) rather than trying to do motion via ffmpeg filters; captions kept out of y>1540 (bottom-reserved) and the CTA scene's own card carries its own text so a duplicate caption box on top of it was dropped as redundant clutter.
- Nothing in this repo persists the renderer/TTS scripts between sessions (not committed, scratchpad is ephemeral) — each run currently rebuilds the whole pipeline from scratch.

## WORKSHOP BATCH DATE RULE (set 2026-11-20, Vicky's instruction — do not hardcode a fixed date again)
Every month has TWO batches, always:
- Batch A: the 2nd Saturday–Sunday of the month
- Batch B: the 4th Saturday–Sunday of the month
("2nd Saturday" = the 2nd Saturday counting from day 1 of that month; the batch is that Saturday + the next day, Sunday.)

For every new WORKSHOP AD Reel: compute TODAY's date, find the next upcoming batch (A or B, whichever comes first that hasn't already passed/started), and use ONLY that batch's real calendar dates in the script/caption. Never reuse a date from a previous Reel once it has passed. If genuinely unsure which batch is "next" (e.g. today falls between the two), ask Vicky once rather than guessing.

Time: 6–9 PM IST. Price: ₹199 (reg ₹599) unless Vicky has said a new price in this chat. Register at https://rocket-launch-register.lovable.app.

Example (do NOT hardcode this — recompute live each time): for December 2026, Batch A = 12–13 Dec, Batch B = 26–27 Dec.
