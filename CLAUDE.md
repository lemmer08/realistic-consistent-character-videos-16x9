# CLAUDE.md

This repository is a prompt package for making fast-paced, photorealistic consistent-character videos of real people (from the user's reference photos) in VideoExpress. It contains no code to run.

- Follow `PLAYBOOK.md` exactly, starting at Section 1 (Intake).
- Use a browser: the built-in browser in the Claude desktop app, or Claude in Chrome. Open https://app.videoexpress.ai/.
- Do not run shell commands, tests or scripts. Do not do a capability audit, model verification or approval gates. Go straight from intake to production.
- The only file action allowed is uploading the user's reference photos into **Media Library → My Media → Images** (Upload file → + Add files; Claude in Chrome's file upload works on that dialog), then picking them into **Use Consistent Character → Reference Photo / Reference Photo 2**. If you can't, ask the user to upload them in the open tab.
- Ask the user only for the intake answers (photos, story, accent, and duration asked every film), a photo upload you can't do, the one-time Consistent Character **I Agree** disclaimer, a sign-in, or a Terms/credits screen they must click themselves.
- Every image: Image Type **Photorealistic (Cinematic)**, **Use Creative mode ON**, and a 90–140-word **Character Description** per person pasted verbatim. Default format **Vertical 9:16**.
- Real likenesses: adults only, consent assumed only for legitimate use, public gallery off on every generation.
- References: `skills/realistic-consistent-character-videos/references/videoexpress-ui-map.md` (exact controls), `docs/video-prompting.md` (multi-shot video prompts). Worked examples are in `examples/`.
