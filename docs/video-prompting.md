# Video prompting for realistic talking characters (VideoExpress)

A practical reference for writing image-to-video prompts for the VideoExpress video model when the clip must show real-looking people who speak with lip sync, keep a steady accent and stay recognizable across cuts. It is the background to Section 7 of [`PLAYBOOK.md`](../PLAYBOOK.md), where VideoExpress's "Video and Audio Prompt" field runs the video model on 3–10 s clips.

---

## 1. Write it the way a polished prompt reads

The video model responds best to prompts that read like a clean, descriptive caption of the finished clip. Write in that style from the start:

1. Open on the action or a visual detail, never "The scene opens…", "We see…" or "There is…".
2. Only observable content: visible cues instead of named emotions.
3. Full detail for setting, light and people, with multiple people consistently differentiated.
4. For every shot, the **shot type**, **camera motion** (or "the camera remains static") and **viewpoint**, woven into prose, not tags.
5. A full soundscape: dialogue quoted exactly, tone of voice, music, ambience.
6. Real-time order with "Initially…", "A moment later…", "Simultaneously…".
7. One paragraph, no bullets or "Audio:" labels, roughly 150–220 words.
8. An opening that matches the reference image exactly, and a single continuous take unless you deliberately write a cut.

Also: describe only what changes from the image (an inaccurate restatement of the image can cause unwanted scene cuts), weave audio through the action, pair each quote with its voice quality and accent, never alter the dialogue, no timestamps.

How much to restate the first frame: one short opening clause naming each person by traits that are visible in the start image, with no new attributes, then spend the remaining words on motion, speech, camera and sound.

---

## 2. Structure rules

**The six elements**: (1) shot and scale, (2) scene: light, palette, textures, (3) action as a natural beginning-to-end sequence where every sentence has a doing verb, (4) characters: age, hair, clothing, emotion shown physically, (5) camera movement, including how the subject looks after the move, (6) audio: ambience, music, speech, with dialogue in quotation marks plus language and accent.

**Form**
- One flowing paragraph, present tense. Dialogue-heavy scenes may be written screenplay-style, with speaker cues, a delivery note and a "(beat)".
- Lead with the main action.
- Write the pauses you want. The model will not stretch a moment or add a pause you did not prompt for.
- Few characters, one coherent light logic per shot, and layer detail over iterations rather than all at once.

**Avoid**
- Emotion labels without a visual cue.
- Readable text, signage and logos (still unreliable; add in post).
- Chaotic physics: jumping, juggling, spins. Dancing is fine.
- Piling up characters, layered actions and objects: the more you ask for, the more gets dropped.
- Conflicting light sources.
- Prompts copied from other models in tag or shot-list syntax.

**More habits**
- A bare noun-phrase opening tends to come out near-static; open on a verb.
- Labelled fields look assembled; write prose. No "Sound:" lines.
- No negative prompt; describe the positive end state.
- Resolution and duration are request parameters, not prompt text.
- Give every action an end state, or the clip drifts or loops.

---

## 3. Dialogue and lip sync

**Core rules**
- Spoken words go in **double quotation marks**, with language and accent stated where needed.
- Delivery is attached to the verb: "says softly", "mutters defensively", "exhales, slightly annoyed". Useful vocabulary covers voice quality (resonant, monotone, gravelly) and volume (whisper, mutter, shout).
- Pair every quote with a voice description and never change the words.
- For lip-synced dialogue in one framing, prefer a single continuous take.

**Timing and delivery**
- Budget about **2.5 spoken words per second**, with a beat of silence at each end.
- A line that starts on frame one gives lip sync nothing to lock onto; leave a short breath first.
- Keep speech out of the final second, where it tends to arrive half-finished.
- Keep the camera static or slow while someone talks; 24/25 fps reads better than 50 for dialogue.
- Describe the voice with tonal or physical words ("a warm, measured voice"), not an emotion, and keep one speaker per line.
- Pin micro-motions to phrases: a blink, a small nod on the last word, a brow lift on a key word.

**Keeping the listener's mouth closed.** Name the speaker immediately before every line, keep the two people visually distinct, give the listener a concrete silent action, keep lines short, and fall back to one speaker per clip.

Our rules for realistic two-person clips:
- One speaker per clip.
- The speaker's identifying tag sits right before the quote.
- The other person "listens, lips closed, and does not speak".
- Never more than two visible people, since more faces tend to merge.

---

## 4. Accent phrasing

- Name the language and accent you want. A clear template: `[Speaker] is speaking [Language/Accent], saying: "[Dialogue]"`.
- Phrasings that work: "English with a slight German accent", "in a calm British accent".
- The model does not translate; write non-English lines in their own language and script.

Accent stability across clips depends on repetition more than on wording. Fix one **Voice Lock** per character, a voice line plus an accent phrase, and paste it word for word before every line that character speaks:

```
says in a warm, mid-pitched, confident female voice, speaking English with a natural Australian accent: "…"
```

Changing even an adjective between clips invites a different voice.

---

## 5. Multi-shot cuts inside one clip

**Supported.** The video model can generate several shots in one clip while keeping identity, setting, light, voice and style across cuts. There is no shot-count parameter: cuts are written in the prompt.

**Phrasing**
- Still one chronological paragraph. No shot list, numbered beats or sluglines unless the cut is also described in prose.
- Name the transition: "A hard cut transitions to…", "The view cuts to a close-up of…", "A match cut connects…", "The image dissolves into…".
- At each cut:
  - name the transition;
  - re-establish scale, angle, who is in frame, and light if it changed;
  - reuse the same visual identifiers for returning people;
  - state what the audio does ("the score continues across the cut").
- Plan 2–4 shots, each with a job: establish, detail, reaction.

**How many cuts per clip**: a shot needs about 3 s to register; a cut every 2 s reads like a slideshow. Stop at 3 shots for 8–10 s, never more than 4.

**Identity across cuts**: re-identify people with the same visible descriptors, not names or pronouns; the model cannot see a name, and an unannounced subject can return as someone else.

**Rules of thumb**
- 5–6 s: one shot. 8 s: 2–3 shots. Never more than 2 cuts in 8 s.
- Change shot size by at least one step at each cut.
- Keep each sentence of dialogue inside one shot.
- Don't use "[0–3s]" timestamps or "Shot 1:" numbering.

---

## 6. Image-to-video rules

- **The image sets the look; the prompt says what happens.** The model already knows what the scene looks like from the image, so spend the words on motion, camera and audio. Re-captioning the still with new traits causes identity drift.
- **Keep the opening consistent with the frame.** Open by matching the image without inventing or contradicting anything.
- **Cuts from a start image are off the default path.** A first-frame clip defaults to a single take unless you intentionally describe a cut away from it. So:
  - Shot A is the start image's framing and carries the dialogue, because the image anchors identity and lip sync best.
  - Later shots change scale or angle of the same people in the same place (medium → close-up, or a reverse angle on the listener), re-identified by their visible traits.
  - Anyone who appears after a cut should already be visible in the start image.
- **Small, supported motion.** Big camera swings or people walking into frame force the model to invent unseen detail. Add "gentle" or "slow" to hair and fabric movement.
- **Camera vocabulary**: follows, tracks, pans, tilts, pushes in, pulls back, handheld, over-the-shoulder, static frame; slow dolly-ins and over-the-shoulder framings help consistency. Say where a move ends.
- **Fixing a frozen start:** open on a verb and give a concrete first micro-movement (an inhale, a blink, a head turn) before the first word.

---

## 7. Audio and "no music"

- Describe ambience, effects, speech and music in prose, with plain, concrete settings such as café noise and rain.
- Every sound should have a visible source and be tied to its action ("the slap of paper on wood"); abstract mood audio lands less reliably.
- Mix in words: voice up front, effects with the motion, the ambient bed underneath, with volume words ("a distant murmur").
- **No music.** For a vocal-only track, say "no music" explicitly. It is the single most useful audio direction, because the model otherwise often adds its own score.
- **No captions.** Quoted dialogue is spoken, not rendered as on-screen text. Don't mention subtitles or captions at all, since naming them can invite them. If text appears anyway, add "no on-screen text" once at the end; negative phrasing is weak in the video model, so keep it to one clause.

---

## 8. Prompt enhancer: off

- The enhancer is an LLM rewrite. It helps most with short, rough prompts or prompts written for another model, least with prompts that already follow the structure. Leave it off if you want your prompt submitted exactly as written.
- Leaving it on with a hand-written multi-shot prompt risks four things:
  - It tends to write one continuous take, so it may strip your cuts.
  - It adds aesthetic descriptors you didn't ask for.
  - It expands the text to 150–220 words, which can shift dialogue timing.
  - It may reword your Voice Lock, which loosens the accent.
- **Recommendation:** switch any "enhance my video prompt" toggle **off**, and write in the polished style of Section 1 anyway so that any server-side rewrite changes little.

---

## 9. Word budgets

| Clip | Spoken words (max) | Prompt length | Shots |
|---|---|---|---|
| 5 s, Single-shot | **10** | 80–150 words | 1 |
| 8 s, Multi-shot | **16** total, ~8 per line, max 2 lines | 130–200 words | 2–3 |
| 10 s | 20–25 | 150–220 words | up to 3 |

The spoken budget is ~2.5 words/s minus ~1.5 s of silence (a breath before the first word, a beat after the last). Fewer words is always safer: if words get skipped or rushed, shorten the line before anything else. Keep prompts within about 200 words; 150–220 is the comfortable range for 10 s.

---

## 10. Failure modes and fixes

| Symptom | Fix |
|---|---|
| Face drifts or morphs | Don't re-describe the still with new traits; keep motion small; reuse identical descriptors after cuts; max two people |
| Static or frozen opening | Open on a verb with a concrete first micro-movement |
| Extra, skipped or rushed words | ~2.5 words/s, silence at both ends, nothing in the last second |
| Wrong person's mouth moves | Name the speaker right before the line; distinct looks; silent action for the listener; one speaker per clip |
| Loose lip sync | Steady camera, one framing for the line, a beat before the first word |
| Accent wanders between clips | Identical Voice Lock in every prompt; enhancer off |
| Unwanted score | End with "no music" |
| Cut ignored, or a camera move instead of a cut | Name the cut ("A hard cut transitions to…"), change shot size, re-establish framing; enhancer off |
| Thin or silent audio | Close, concrete sound sources tied to visible actions |
| Garbled text or logos | Leave them out; add in post |
| Clip loops or drifts at the end | Give the action an end state; end on the action or the last word |

---

For fill-in templates that put all of this together (Multi-shot 8 s and Single-shot 5 s), see `PLAYBOOK.md` Section 7; for a complete worked production, see [`examples/realistic-rooftop-tickets.md`](../examples/realistic-rooftop-tickets.md).

Not verified: how VideoExpress calls the video model internally (whether a server-side enhancer runs, and which frame rate it uses).
