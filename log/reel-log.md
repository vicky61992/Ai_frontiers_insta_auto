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
| 2026-11-22 | VALUE | Jio Unlimited 5G users: Google Gemini Pro 18 months free (Gemini 3 + 2TB) | Posted (found live on IG, backfilled into log — was never logged by the run that made it) | https://www.instagram.com/reel/DgDG9jNDP4X/ |
| 2026-11-23 | VALUE | Gemini Nano Banana free photo trick (old photo repair / 3D figurine) | Rendered + QA'd, sent to Vicky for review, awaiting his "yes" to post | reels/2026-11-21-gemini-nano-banana.mp4 (local, not yet posted) |

Next type due: WORKSHOP AD, once the 23 Nov Nano Banana reel above is approved and posted — the 2 VALUE reels owed after the 21 Nov ad are now both done (22 Nov Jio + 23 Nov Nano Banana).

2026-11-10 gemini-notebook-v3.mp4 / -v4.mp4: earlier draft iterations of the already-posted Gemini Notebook reel (DfjyQxYFKgY) — not separate pending posts, do not publish.

2026-11-21-gemini-nano-banana.mp4: was fully rendered (voice + video) in an earlier run but never logged, sent, or posted before that run moved on to make the 21 Nov workshop-ad reel instead. Recovered, QA'd (re-transcribed audio, re-verified Nano Banana claims + 28-29 Nov batch dates still valid) and sent for approval on 23 Nov. **Lesson: always log a reel the moment it's rendered, even before it's sent/approved, so work like this isn't orphaned.**

2026-11-23: an Instagram reel ("Pramaan — AI Originality & Plagiarism Checker", linking to pramaan-plagiarism-check.vsbaghel.co.in, shortcode DgEa7elzUb4) appeared on the account outside this pipeline entirely — no matching mp4, no log entry, doesn't follow the Hinglish-skill format or workshop CTA. Flagged to Vicky to confirm it was his own post; not touched or claimed by this log.

## Notes
- Voice: gemini-3.8-flash-tts, Puck, one request per scene ~25 s apart (429 on back-to-back calls; retry after ~20–40 s). Keep only WAV data chunk.
- STT QA: gemini-3.5-flash.
- Renderer: Python + PIL + ffmpeg, navy+gold, cover first 3 s, synthesized music ducked.
- rocket-launch-register.lovable.app is not reachable from the cloud sandbox (network allowlist); workshop details taken from earlier captions.
- The Instagram account can and does get posts from outside this pipeline (manual posts by Vicky, or other tools) — check vidiq_instagram_owner_insights at the start of each run, not just this log, to see what's actually live before assuming the log is the full picture.

## WORKSHOP BATCH DATE RULE (set 2026-11-20, Vicky's instruction — do not hardcode a fixed date again)
Every month has TWO batches, always:
- Batch A: the 2nd Saturday–Sunday of the month
- Batch B: the 4th Saturday–Sunday of the month
("2nd Saturday" = the 2nd Saturday counting from day 1 of that month; the batch is that Saturday + the next day, Sunday.)

For every new WORKSHOP AD Reel: compute TODAY's date, find the next upcoming batch (A or B, whichever comes first that hasn't already passed/started), and use ONLY that batch's real calendar dates in the script/caption. Never reuse a date from a previous Reel once it has passed. If genuinely unsure which batch is "next" (e.g. today falls between the two), ask Vicky once rather than guessing.

Time: 6–9 PM IST. Price: ₹199 (reg ₹599) unless Vicky has said a new price in this chat. Register at https://rocket-launch-register.lovable.app.

Example (do NOT hardcode this — recompute live each time): for December 2026, Batch A = 12–13 Dec, Batch B = 26–27 Dec.
