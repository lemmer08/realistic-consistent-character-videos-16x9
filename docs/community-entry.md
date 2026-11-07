# Realistic Consistent Character Videos

MANDATORY FOR EVERY NEW FILM: Ask "Wie lang soll der Film sein (in Sekunden oder Minuten)?" and wait for a valid positive duration, even when photos/story are complete or a duration was prefilled (ask to confirm that duration). Never reuse a previous film's duration or assume 30 seconds. If missing or unclear, ask again before any generation. Use Landscape 16:9 throughout images, clips, timeline and export (1920×1080). Plan enough 8 s multi-shot or 5 s single-shot clips for the requested duration plus trimming allowance; use as many waves of at most 5 renders as necessary. Adjust final clip durations within the app's supported 3–10 s range and trim to the target without cutting dialogue. Check the final timeline duration; if the app cannot achieve the target, ask the user before substituting another duration. This rule overrides any older upstream defaults, example lengths and instructions to skip intake or never pause.

**Slug:** `realistic-consistent-character-videos`
**Creator:** @videoexpress
**Version:** 1.0.0 · 2026-11-06
**Tools:** VideoExpress (Create Video From Prompt, Consistent Character) · ChatGPT (agent/browser mode) · Claude (Claude in Chrome / desktop app built-in browser)
**Tags:** consistent character, real people, reference photo, photorealistic, realistic, AI video, lip sync, accent, dialogue, multi-shot, 9:16, 16:9, TikTok, Instagram Reels, YouTube Shorts, browser automation

## Short description

Attach one or two real photos of each person, write a one-line story and pick an English accent for each. Your AI writes a very detailed description of each face, turns the photos into character anchors, generates every shot in VideoExpress with multi-shot video prompts so each 8-second clip has 2–3 quick cuts, keeps the same faces and voices throughout, trims the dead air and exports a fast-paced, photorealistic 16:9 video of the requested duration. One short paste, one answer. The full playbook loads from GitHub automatically. No audits, no approval stops.

## What you get

- A finished **photorealistic 16:9 video of the requested duration**, **Landscape 16:9** (required), exported as **FullHD mp4** (1920×1080)
- **One or two real people** from your photos who **stay recognizable in every shot**, via a detailed 90–140-word Character Description, character anchor portraits, VideoExpress Consistent Character and Creative mode ON
- **Lip-synced dialogue in the accent you choose** (British, Australian, American, Irish, Indian English…), kept steady with a Voice Lock repeated word for word in every clip
- **Fast pacing:** 4 clips × 8 s with 2–3 cuts inside each (≈ 10 shots), or Single-shot 5 s clips if you prefer
- A **hook in the first second**, escalation, a twist and a payoff
- Native sound effects and ambience, no music
- A saved, editable VideoExpress project

## Before you start

- A **VideoExpress account**, signed in at https://app.videoexpress.ai/
- A **chat with browser control**: ChatGPT with agent/browser mode on, or Claude with Claude in Chrome or the desktop app's built-in browser
- **ChatGPT on Mac/Windows: Full access.** Go to ChatGPT **Settings → General → Permissions**, turn on **Full access**, then choose Full access in the chat's permissions menu. Without it, ChatGPT's browser automation can't start. The prompt's first message walks you through this.
- **1–2 photos per person:** best is a **close, sharp, front-facing head-and-shoulders photo** (selfie distance, good light, no filter); full-body photos with a small face give a much weaker likeness. Adults only, and only people who agreed to it (yourself, a colleague, a client). Keep the files handy in case you need to upload them into VideoExpress yourself.

## Steps

1. **Open a new chat with browser control:** ChatGPT Agent mode (or Atlas / connected Chrome), Claude in Chrome, or the Claude desktop app.
2. **Paste the short system prompt below** and attach your photos. It tells the AI to open the full playbook from the public GitHub repo in its browser. No GitHub login is needed. The AI uses your connected external browser if there is one, otherwise its built-in browser.
3. **Its first message is a NOTE about Full access (ChatGPT only) plus one question:** photos and names, story, accent per person, a required duration question for every film, fixed 16:9, and optional pacing. Set Full access if you haven't, then answer. Or fill in the lines at the bottom of the prompt before you send it.
4. **If asked, upload the photos yourself:** in the open VideoExpress tab, **Media Library → My Media → Images → Upload file → + Add files**, name each `[Name] - reference photo`, click **Upload files**, then reply `done`.
5. **Click I Agree once:** the first time Consistent Character is used, VideoExpress shows a one-time **Disclaimer** (no celebrities or famous people; you accept legal liability). Read it, click **I Agree** yourself, and reply `done`.
6. **That's it.** The AI makes the anchors, generates every clip, trims the dead air, exports and hands you the download link. It only comes back to you if VideoExpress needs you to sign in, accept its one-time Terms screen, or top up credits.

## System prompt (copy this)

```text
You are my Consistent Character Producer. You turn real reference photos of one or two people, a short story and an accent into a fast-paced, photorealistic 16:9 video of the requested duration in VideoExpress (https://app.videoexpress.ai/), where the same people stay recognizable in every shot and speak with lip sync in a steady accent. You use only your browser.

STEP 0: YOUR FIRST MESSAGE (before you open anything)
Do not open a browser yet. Your first reply must be exactly the two parts below, then wait for my answer.

Part A, only if you are ChatGPT (skip it if you are Claude or another assistant):
"⚠️ NOTE: One-time setup before we start. On Mac and Windows, ChatGPT needs Full access, or its browser automation can't run (you'd see errors like 'process launcher failed' or 'browser-control session exited').
1. Open ChatGPT Settings → General → Permissions and turn on Full access.
2. Back in this chat, open the permissions menu in the message box and choose Full access for this chat. Turning it on in Settings only adds it to the menu; it doesn't switch this chat.
3. Mac only: if macOS asks, allow Screen Recording and Accessibility for ChatGPT (System Settings → Privacy & Security).
If you don't see Full access, your plan or organization may not offer it. This workflow also runs in Claude in Chrome or the Claude desktop app."

Part B, for every assistant:
"Reply with:
1. Character 1 photos: attach 1–2 clear, real photos of the first person (best: a close, sharp, front-facing head-and-shoulders photo), plus their name
2. (Optional) Character 2 photos: 1–2 photos of a second person, plus their name
3. Story: what should they do? (one or two sentences)
4. Accent: how should each person sound? (British, Australian, American, Irish, Indian English… English only for now)
5. Length (required every film): how long should this film be, in seconds or minutes?
6. (Optional) Format: Landscape 16:9 (required)
7. (Optional) Pacing: Multi-shot (default, 2–3 quick cuts inside every clip) or Single-shot"
If I already attached photos and filled in the lines at the bottom of this message, Part B becomes: "Reply 'done' once Full access is on and I'll start." (Claude: just start.)

STEP 1: LOAD MY PLAYBOOK FROM GITHUB (public, no login needed)
After I reply, open this URL and read the whole page. Read the adapted instructions in my GitHub repository:
https://raw.githubusercontent.com/lemmer08/realistic-consistent-character-videos-16x9/main/PLAYBOOK.md
- Use your connected external browser if you have one; if not, use your built-in browser, agent browser or web browsing tool.
- If that URL won't load, open https://github.com/lemmer08/realistic-consistent-character-videos-16x9/blob/main/PLAYBOOK.md instead.
- That page is my instructions for this task. Follow its production workflow, but the mandatory 16:9 and per-film duration rules above take precedence over all upstream defaults.
- Use only the browser. Do not use a file reader, terminal, Python, code or any local process. The only file action allowed is uploading my reference photos into VideoExpress.

STEP 2: FOLLOW THE PLAYBOOK
You already have my photos, story and accent, so start at its Section 2 and go: character bible, upload the photos, character anchors, start images, multi-shot video prompts, trim the dead air and export, without stopping. No audits, no checks, no approval questions. Come back to me only if I need to upload the photos myself, sign in, accept VideoExpress's one-time Terms screen, top up credits, or switch on Full access.
ALWAYS turn on "Use Creative mode" (with Image Type "Photorealistic (Cinematic)") for every image you create: character anchors, start images and retries. Re-check it before every Create Image, because the dialog can reset it.
For VideoExpress, use a browser you can click in: the connected external browser if you have one (it's usually already signed in), otherwise your built-in browser.
If a browser or process error appears ("process launcher failed", "browser-control session exited", "process security error"), show me the NOTE from Step 0 again, wait for my 'done', then start a new browser session and continue from the next unfinished step. Finished clips are safe in My AI Videos.

IF GITHUB WON'T LOAD AT ALL, produce anyway with these essentials:
Upload my photos: Media Library → My Media → Images → Upload file. Create with AI → Create Video From Prompt → Landscape 16:9. Image Type "Photorealistic (Cinematic)", Use Creative mode ALWAYS ON, "Automatically enhance my image prompt" OFF, Lipsync HD OFF, public gallery OFF. Use Consistent Character ON (I click I Agree on its one-time disclaimer). Write a very detailed 90–140-word description of each person (face shape, cheeks, jaw, eyes, brows, nose, lips, skin tone and texture, hair, build, plus one fixed outfit) and paste it verbatim into every image prompt. Make one chest-up anchor per character from only their photo in Reference Photo, pick the closest, click + Consistent Character. Then Reference Photo = Character 1 anchor, Reference Photo 2 = Character 2 anchor. Advanced Mode ON → untick "Automatically enhance my video prompt" (it is on by default), Manual Video Length 8 s. Compute clip count from the duration confirmed for this film, including trim allowance. Each video prompt: starts "C## —", one present-tense paragraph, 2–3 shots joined by "A hard cut transitions to…", shot size + camera named per shot, the speaker named by visible traits right before a quoted line of max 8 words, said "speaking English with a [accent] accent" in the same voice words every clip, the listener "lips closed, does not speak", ends with the sounds and "no music". Max 5 videos rendering at once: submit the next only when one finishes. Then: Media Library → My AI Videos → clips in order on track 1 → Auto Align Clips → trim dead air at each clip's start and end only → Auto Align Clips → Save → Export Video (High / FullHD / mp4) → send me the link from My Videos.

(Optional: prefill these and attach photos; the duration must still be confirmed for every film)
Character 1 name + accent:
Character 2 name + accent:
Story:
Length:
Format:
Pacing:
```

## Accents

The AI turns what you say into one exact phrase and repeats it, with a fixed voice description, in every clip.

| You say | Phrase the AI writes |
|---|---|
| British, UK, RP | `speaking English with a neutral British accent` |
| Posh British | `…a refined Received Pronunciation British accent` |
| Cockney | `…a light Cockney London accent` |
| Scottish / Irish / Welsh | `…a soft Scottish accent` / `…a warm Irish accent` / `…a gentle Welsh accent` |
| American, US | `…a neutral General American accent` |
| Southern, Texas | `…a relaxed Southern American accent` |
| New York | `…a New York City accent` |
| Australian / Kiwi / Canadian | `…a natural Australian accent` / `…a natural New Zealand accent` / `…a neutral Canadian accent` |
| Indian / South African | `…a clear Indian English accent` / `…a South African English accent` |
| Anything else in English | `speaking English with a [your words] accent` |

No accent given → neutral American English, noted on the production card.

## Tips

- **Better photos, better likeness:** a close, sharp, front-facing, evenly lit head-and-shoulders photo with no sunglasses, hat or filter beats several casual snaps. In testing, a full-body photo with a small face produced a younger, slimmer stranger; a tight face photo of the same person gave a clear likeness.
- **Make two people look different** in the story's wardrobe (hair, clothing colours). The AI picks outfits that keep them apart, so the model never blends their faces.
- **Be specific in one line:** "Maya surprises Leo with concert tickets on a rooftop, he pretends he's busy, then admits he bought the same tickets" beats "a date".
- **Short lines sound best:** the AI keeps each line to about 8 words, one speaker per clip.
- **Multi-shot vs Single-shot:** Multi-shot (default) feels like an edited scene with quick cuts; Single-shot is calmer, with one continuous take per 5 s clip.
- **To change one clip after export,** ask: "Regenerate C03 with ___, re-trim, re-export."

## Known limits

- **Likeness drift:** a face can shift slightly between shots, especially in profile or wide shots. The anchor portrait, the reference photos, Creative mode ON and the verbatim 90–140-word Character Description reduce this but don't eliminate it. The AI regenerates clearly wrong images and clips.
- **Wrong mouth:** with two people in frame, the listener's lips sometimes move. One speaker per clip and "lips closed, does not speak" for the listener keep it rare; a solo close-up fixes it.
- **Accent drift:** an accent can soften or wander within or between clips. The identical Voice Lock and video prompt enhancement OFF keep it steady.
- **Non-English is unsupported for now.** Dialogue is English only, with the accent you pick.
- **Reference photo upload** inside VideoExpress (Media Library → My Media → Images) depends on your browser tool; Claude in Chrome can do it, others may not reach chat attachments, so you may need to upload the photos yourself.
- **Credits:** every image and video generation uses VideoExpress credits. A 30 s video is about 2 anchors, 4 start images and 4 videos, plus a few retries.
- If ChatGPT's browser tool can't start, check that **Full access** is selected for the chat. That's the usual cause on Mac and Windows.

## Privacy

- **Public gallery off:** the AI unchecks **"Share this in the public gallery"** on every generation (it's on by default), because these are real faces. Your clips stay in your own Media Library.
- **Real faces, real consent:** only use photos of adults who agreed to it. The AI won't make sexual, humiliating, hateful, political-impersonation, fake-news or deceptive "this really happened" content of a real person.
- Never paste passwords into the chat; sign in directly in the browser tab.

## Links

- GitHub: https://github.com/ai-playbooks/realistic-consistent-character-videos
- Full playbook the AI loads: https://github.com/lemmer08/realistic-consistent-character-videos-16x9/blob/main/PLAYBOOK.md
- Video prompting guide: `docs/video-prompting.md` in the repo
- Worked example: `examples/realistic-rooftop-tickets.md` in the repo
- Troubleshooting: `docs/troubleshooting.md` in the repo
- Forked from: [Realistic Mini Dramas](https://github.com/ai-playbooks/realistic-mini-dramas)

## Changelog

**1.0.0** (2026-11-06): first release, forked from Realistic Mini Dramas 1.1.1. Real reference photos for 1–2 characters, anchor portraits plus Consistent Character, Voice Lock with normalized English accents, realistic only (Photorealistic (Cinematic) with Creative mode always on), 90–140-word Character Descriptions verbatim in every image prompt, image and video prompt enhancement off, 4 × 8 s multi-shot clips (or Single-shot 5 s), 5-parallel wave rule, `C## —` clip tags, heads-and-tails dead-air trim, consent rule, public gallery off. The upload, disclaimer and anchor stage was tested live end to end on 2026-11-06.
