---
name: realistic-consistent-character-videos
description: Produce a fast-paced photorealistic 16:9 video of the requested duration of one or two real people from their reference photos, end to end in the VideoExpress web app with a browser - detailed character descriptions and voice locks, Consistent Character anchors, multi-shot image-to-video clips with lip-synced dialogue in a chosen English accent, dead-air trimming and export. Use when the user attaches photos of real people and asks for a consistent-character video, a video "starring" themselves or a colleague, a realistic talking scene with their face, or a VideoExpress consistent character video.
---

MANDATORY FOR EVERY NEW FILM: Ask "Wie lang soll der Film sein (in Sekunden oder Minuten)?" and wait for a valid positive duration, even when photos/story are complete or a duration was prefilled (ask to confirm that duration). Never reuse a previous film's duration or assume 30 seconds. If missing or unclear, ask again before any generation. Use Landscape 16:9 throughout images, clips, timeline and export (1920×1080). Plan enough 8 s multi-shot or 5 s single-shot clips for the requested duration plus trimming allowance; use as many waves of at most 5 renders as necessary. Adjust final clip durations within the app's supported 3–10 s range and trim to the target without cutting dialogue. Check the final timeline duration; if the app cannot achieve the target, ask the user before substituting another duration. This rule overrides any older upstream defaults, example lengths and instructions to skip intake or never pause.


# Realistic Consistent Character Videos in VideoExpress

The full recipe is `../../PLAYBOOK.md` at the repository root (public URL: https://raw.githubusercontent.com/lemmer08/realistic-consistent-character-videos-16x9/main/PLAYBOOK.md). Follow it exactly. It is self-contained.

## Non-negotiables
1. **Browser only.** Work at https://app.videoexpress.ai/. Run no code, shell, tests or file processing. The only file action is uploading the user's reference photos (Media Library → My Media → Images → Upload file → + Add files → Upload files).
2. **No preflight.** No capability audit, readiness check, model verification, cost estimate or approval gate.
3. **One question.** Ask for 1–2 photos plus a name per character (1 or 2 characters; best a close, sharp, front-facing head-and-shoulders photo), a story, an English accent per character, and required length (ask every film and wait), fixed Landscape 16:9, and optional pacing (Multi-shot default or Single-shot). Then produce without stopping.
4. **Consent.** Adults only, real likenesses the user has the right to use. No sexual, humiliating, hateful, political-impersonation, fake-news or deceptive content of a real person.
5. **Realistic only.** Create Video From Prompt → **Landscape 16:9** (default) → Image Type **Photorealistic (Cinematic)**, **Use Creative mode ALWAYS ON** (anchors, start images, retries), **Automatically enhance my image prompt OFF**, Lipsync HD and Narration OFF, **public gallery OFF** on every generation.
6. **Identity.** Write a very detailed **Character Description** per person (90–140 words: age/build, face shape, cheeks, jaw, chin, eyes, brows, nose, lips, skin, ears/facial hair, hair, accessories, plus a garment-by-garment Wardrobe Lock) and paste it verbatim into every image prompt; a Short Tag goes in video prompts. **Use Consistent Character** ON (the user clicks **I Agree** on the one-time Disclaimer). Make one chest-up anchor per character from only their photo in **Reference Photo**, select the closest carousel image (✓) and click **+ Consistent Character**. Then **Reference Photo** = Character 1's anchor, **Reference Photo 2** = Character 2's anchor.
7. **Voice Lock.** One voice line plus the normalized accent phrase per character, word for word identical in every video prompt. English only.
8. **Multi-shot.** Variable clip count from the confirmed duration, with 8 s source clips, 2–3 shots per clip joined by "A hard cut transitions to…". Single-shot = 5 s clips, no cuts. Advanced Mode → **Automatically enhance my video prompt OFF** (it is ON by default). Every prompt starts with `C## —`.
9. **5 in parallel.** Never more than 5 videos rendering; work in waves.
10. **Dead-air trim** at each clip's head and tail only, never inside a clip, then **Auto Align Clips**. Export High / FullHD / mp4 and deliver the My Videos link.

## Only stop for
A photo upload your browser can't do, the one-time Consistent Character Disclaimer (**I Agree**), a login page, a one-time Terms screen, or an out-of-credits screen. The user does it, says "done", and you continue where you stopped.

## References
- `references/videoexpress-ui-map.md`: every control, label, default and quirk
- `../../docs/video-prompting.md`: how to write multi-shot video prompts
- `../../examples/README.md` and `../../examples/realistic-rooftop-tickets.md`: a worked job with every prompt written out
