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

Next type due: WORKSHOP AD — 3 VALUE reels posted since the last ad (2026-11-21), ratio already satisfied/exceeded, so the next Reel must be a WORKSHOP AD.

Note (2026-11-24): the Jio, Pramaan and Nano Banana reels above were posted by an earlier run but never logged here and their source files/scripts were never committed to this repo (only reels/2026-11-21-gemini-nano-banana.mp4 exists locally, matching the Nano Banana post) — added retroactively from Instagram owner-insights data so the ratio tracking stays correct. Always double check vidiq_instagram_owner_insights against this table before deciding what's "next type due".

2026-11-10 gemini-notebook-v3.mp4 / -v4.mp4: earlier draft iterations of the already-posted Gemini Notebook reel (DfjyQxYFKgY) — not separate pending posts, do not publish.
2026-11-21-gemini-nano-banana.mp4: draft iteration of the already-posted Nano Banana reel (DgFy3tgDFK_) — not a separate pending post, do not publish.

## Notes
- Voice: gemini-3.8-flash-tts, Puck, one request per scene ~25 s apart (429 on back-to-back calls; retry after ~20–40 s). Keep only WAV data chunk.
- STT QA: gemini-3.5-flash.
- Renderer: Python + PIL + ffmpeg, navy+gold, cover first 3 s, synthesized music ducked.
- rocket-launch-register.lovable.app is not reachable from the cloud sandbox (network allowlist); workshop details taken from earlier captions.

## WORKSHOP BATCH DATE RULE (set 2026-11-20, Vicky's instruction — do not hardcode a fixed date again)
Every month has TWO batches, always:
- Batch A: the 2nd Saturday–Sunday of the month
- Batch B: the 4th Saturday–Sunday of the month
("2nd Saturday" = the 2nd Saturday counting from day 1 of that month; the batch is that Saturday + the next day, Sunday.)

For every new WORKSHOP AD Reel: compute TODAY's date, find the next upcoming batch (A or B, whichever comes first that hasn't already passed/started), and use ONLY that batch's real calendar dates in the script/caption. Never reuse a date from a previous Reel once it has passed. If genuinely unsure which batch is "next" (e.g. today falls between the two), ask Vicky once rather than guessing.

Time: 6–9 PM IST. Price: ₹199 (reg ₹599) unless Vicky has said a new price in this chat. Register at https://rocket-launch-register.lovable.app.

Example (do NOT hardcode this — recompute live each time): for December 2026, Batch A = 12–13 Dec, Batch B = 26–27 Dec.
