# Example packs

**Modified edition:** Landscape 16:9 throughout; duration must be asked and confirmed for every new film, with no default. Use this repository’s modified PLAYBOOK.md. Adapted from [ai-playbooks/realistic-consistent-character-videos](https://github.com/ai-playbooks/realistic-consistent-character-videos); the upstream repository remains unchanged.

Copy-ready reference productions built exactly to [`PLAYBOOK.md`](../PLAYBOOK.md): same clip math, settings (Creative mode ON), Character Descriptions, World and Voice Locks, prompt templates and pacing rules. Every prompt is written out in full, with the realism tag, the full Character Descriptions, Short Tags and Voice Locks spelled out each time, so nothing has to be filled in.

| Pack | Cast (accent) | Format | Length | Pacing | Clips | Structure |
|---|---|---|---|---|---|---|
| [realistic-rooftop-tickets.md](realistic-rooftop-tickets.md) | MAYA (Australian) · LEO (neutral British) | Vertical 9:16 | ~30 s (trim sum ≈ 29.4 s) | Multi-shot, 2 hard cuts per clip | 4 × 8 s (+ a 5 s Single-shot C01 variant) | Hook: tickets on the table → Leo "busy" → twist: he bought the same pair → payoff: spare pair to the couple at the next table |

**What the pack contains:** Character Descriptions (90–140 words each, face feature by feature plus the Wardrobe Lock), Short Tags, Voice Locks, World Lock, settings table, both anchor-portrait image prompts, and for each clip the start-image prompt (~300–400 words, because the full descriptions are pasted in verbatim), the video prompt (one speaker, one line of ≤8 words, Voice Lock verbatim, ending with "no music"), the clip length and a trim target.

## How to use it

- **The AI producer** can study it to see the expected density: a hook in C01, one speaker per clip with the line in Shot A, the listener "lips closed, and does not speak", Short Tags repeated after every cut, a twist at about 70% and a warm payoff. The workflow doesn't require reading these files.
- **A person** can paste the pack into VideoExpress clip by clip:
  1. Upload the two reference photos: **Media Library → My Media → Images → Upload file → + Add files**, name them `MAYA - reference photo` / `LEO - reference photo`, **Upload files**. Then **Create with AI → Create Video From Prompt → Landscape 16:9**, tick **Use Consistent Character** (click **I Agree** on the one-time Disclaimer).
  2. Make each anchor portrait with only that character's photo in **Reference Photo** and **Creative mode ON**, click the closest of the 2 carousel images so it has the ✓, then **+ Consistent Character** (it saves to **My AI Images** and fills the next empty slot). For the clips: **Reference Photo** = MAYA's anchor, **Reference Photo 2** = LEO's anchor.
  3. For each clip: apply the settings table, clear the prompt box and confirm it's empty, paste the **Image Prompt**, click **Create Image**, check the image, paste the **Video and Audio Prompt**, untick **Automatically enhance my video prompt** (ON by default), set **Manual Video Length** to 8 s, uncheck the public gallery, then click **Create Video** once.
  4. Put C01 → C04 on track 1, click **Auto Align Clips**, trim heads and tails to the targets, align again, then Save and Export.
- **Your own people:** the MAYA and LEO descriptions are fictional, written as if read from close, front-facing reference photos. In a real run the Character Description comes from the user's photos: replace the face and hair traits feature by feature, keep the wardrobe, World Lock and structure, or swap the story beats.

Generated clips vary, so trim by what's actually on screen and treat the targets as a guide. Background on the prompt style: [`docs/video-prompting.md`](../docs/video-prompting.md).
