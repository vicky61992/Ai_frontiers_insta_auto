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
| 2026-11-24 | WORKSHOP AD | Zero-Code AI Workshop ("Nov ka last weekend" hook, batch 28-29 Nov) | Posted (discovered via vidIQ Instagram insights on 27 Nov — was NOT logged when it went out; added retroactively) | https://www.instagram.com/reel/DgHDBeTjVGS/ |
| 2026-11-25 | VALUE | ChatGPT Study Mode (free, step-by-step guided learning) | Posted | https://www.instagram.com/reel/DgLKCF6BVG_/ |
| 2026-11-26 | VALUE | Google Search AI Mode free practice quizzes (JEE/NEET, all subjects) | Rendered, awaiting Vicky yes | - |
| 2026-11-27 | WORKSHOP AD | Zero-Code AI Workshop ("walk out with 3 ready projects" outcome/portfolio hook, batch 12-13 Dec) | Rendered, awaiting Vicky yes | - |

Next type due: VALUE (x2), per the 2:1 ratio — three WORKSHOP AD reels (21, 24, 27 Nov) now sit ahead of the VALUE count once the 26 Nov and 27 Nov reels post.

2026-11-10 gemini-notebook-v3.mp4 / -v4.mp4: earlier draft iterations of the already-posted Gemini Notebook reel (DfjyQxYFKgY) — not separate pending posts, do not publish.

## Notes
- Voice: gemini-3.8-flash-tts, Puck, one request per scene ~25 s apart (429 on back-to-back calls; retry after ~20–40 s). Keep only WAV data chunk.
- STT QA: gemini-3.5-flash.
- Renderer: Python + PIL + ffmpeg, navy+gold, cover first 3 s, synthesized music ducked.
- rocket-launch-register.lovable.app is not reachable from the cloud sandbox (network allowlist); workshop details taken from earlier captions.
- 27 Nov run: gemini-3.8-flash-tts free-tier daily quota (10 req/day) ran out after 4 scenes (quota is shared across the whole day/key, not per-session) — fallback gemini-2.5-flash-preview-tts covered the remaining 3 scenes cleanly, same Puck voice, no audible quality gap. STT QA transcript matched the script exactly.
- 27 Nov run: chose Dec 12-13 (Batch A) over the literal "next" calendar batch (Nov 28-29) because (a) today is Nov 27, one day before that batch starts — zero runway for a fresh ad to convert, (b) that batch was already advertised twice (21 Nov and the just-discovered 24 Nov reel). Posting a fresh ad for a batch starting tomorrow would be wasted reach; always sanity-check "next upcoming" against lead time, not just the raw date-rule math.
- Found via vidiq_instagram_owner_insights (mode=reels) that a workshop reel went out 2026-11-24 (DgHDBeTjVGS) that was never added to this log — likely a session that posted but skipped the log-write step. Always cross-check vidiq_instagram_owner_insights against this table before computing "next type due" / "topics used", not just this file.
- 25 Nov ChatGPT Study Mode reel performance (for context): 125 views, 2 likes, 1 save, avg watched 4.6% — low retention, hook likely needs to land faster in future VALUE reels.

## WORKSHOP BATCH DATE RULE (set 2026-11-20, Vicky's instruction — do not hardcode a fixed date again)
Every month has TWO batches, always:
- Batch A: the 2nd Saturday–Sunday of the month
- Batch B: the 4th Saturday–Sunday of the month
("2nd Saturday" = the 2nd Saturday counting from day 1 of that month; the batch is that Saturday + the next day, Sunday.)

For every new WORKSHOP AD Reel: compute TODAY's date, find the next upcoming batch (A or B, whichever comes first that hasn't already passed/started), and use ONLY that batch's real calendar dates in the script/caption. Never reuse a date from a previous Reel once it has passed. If genuinely unsure which batch is "next" (e.g. today falls between the two), ask Vicky once rather than guessing.

Time: 6–9 PM IST. Price: ₹199 (reg ₹599) unless Vicky has said a new price in this chat. Register at https://rocket-launch-register.lovable.app.

Example (do NOT hardcode this — recompute live each time): for December 2026, Batch A = 12–13 Dec, Batch B = 26–27 Dec.
