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
| 2026-11-23 | VALUE | Pramaan — AI Originality & Plagiarism Checker | Posted (found via IG insights, was missing from this log) | https://www.instagram.com/reel/DgEa7elzUb4/ |
| 2026-11-23 | VALUE | Gemini Nano Banana — free AI photo trick (old photo fix / 3D figurine) | Posted (found via IG insights, was missing from this log) | https://www.instagram.com/reel/DgFy3tgDFK_/ |
| 2026-11-24 | WORKSHOP AD | Zero-Code AI Workshop ("Nov ka LAST weekend" hook, batch 28-29 Nov) | Posted (found via IG insights, was missing from this log; no source mp4 in repo) | https://www.instagram.com/reel/DgHDBeTjVGS/ |
| 2026-11-25 | VALUE | ChatGPT Study Mode (free, step-by-step guided learning) | Posted | https://www.instagram.com/reel/DgLKCF6BVG_/ |
| 2026-11-26 | VALUE | Google Opal — free no-code AI mini-app builder (India available) | Awaiting Vicky's "yes" to post | reels/2026-11-26-google-opal.mp4 |

Next type due: WORKSHOP AD (once the 2026-11-26 Opal reel is posted), per the 2:1 ratio.

2026-11-10 gemini-notebook-v3.mp4 / -v4.mp4: earlier draft iterations of the already-posted Gemini Notebook reel (DfjyQxYFKgY) — not separate pending posts, do not publish.

## Notes
- Voice: gemini-3.8-flash-tts, Puck, one request per scene ~25 s apart (429 on back-to-back calls; retry after ~20–40 s). Keep only WAV data chunk.
- STT QA: gemini-3.5-flash. Occasionally returns 503 "high demand" or a socket read timeout — just retry after ~60 s, it comes back.
- Renderer: Python + PIL + ffmpeg, navy+gold, cover first 3 s, synthesized music ducked.
- rocket-launch-register.lovable.app is not reachable from the cloud sandbox (network allowlist); workshop details taken from earlier captions.
- **IMPORTANT — this log can silently fall behind actual posts.** On 2026-11-26 we found 3 posted Reels (2 VALUE on 23 Nov, 1 WORKSHOP AD on 24 Nov) that were live on Instagram but never recorded here, and one of the repo's own unposted-looking draft files (`reels/2026-11-21-gemini-nano-banana.mp4`) had in fact already been posted two days later. **Before picking a topic or reusing any `reels/*.mp4` file, cross-check against `vidiq_instagram_owner_insights` (mode "reels", free, 0 credits) — it is the ground truth for what's actually live, not this file.** Update this log immediately after every post, same session, so it doesn't drift again.
- **Python/Pillow gotcha in this sandbox:** the default `python3` (3.11) resolves to an apt-installed Pillow whose compiled `_imaging` module is for Python 3.12, so `import PIL` raises `ImportError: cannot import name '_imaging'`. Use `/usr/bin/python3.12` (or `/usr/local/bin/python3.13`) for any script that imports PIL/Pillow.

## WORKSHOP BATCH DATE RULE (set 2026-11-20, Vicky's instruction — do not hardcode a fixed date again)
Every month has TWO batches, always:
- Batch A: the 2nd Saturday–Sunday of the month
- Batch B: the 4th Saturday–Sunday of the month
("2nd Saturday" = the 2nd Saturday counting from day 1 of that month; the batch is that Saturday + the next day, Sunday.)

For every new WORKSHOP AD Reel: compute TODAY's date, find the next upcoming batch (A or B, whichever comes first that hasn't already passed/started), and use ONLY that batch's real calendar dates in the script/caption. Never reuse a date from a previous Reel once it has passed. If genuinely unsure which batch is "next" (e.g. today falls between the two), ask Vicky once rather than guessing.

Time: 6–9 PM IST. Price: ₹199 (reg ₹599) unless Vicky has said a new price in this chat. Register at https://rocket-launch-register.lovable.app.

Example (do NOT hardcode this — recompute live each time): for December 2026, Batch A = 12–13 Dec, Batch B = 26–27 Dec.
