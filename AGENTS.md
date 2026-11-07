# AGENTS.md

This repository is a **prompt package**. It contains no software.

## What to do
1. Open `PLAYBOOK.md` (the full instructions) and follow it exactly, starting at **Section 1 (Intake)**.
2. Do all production work in the VideoExpress web app (https://app.videoexpress.ai/) with your **browser tool**.
3. The one file action allowed is uploading the user's reference photos into **Media Library → My Media → Images** (Upload file → + Add files → Upload files), then picking them into **Use Consistent Character → Reference Photo / Reference Photo 2**. If your browser tool can't upload files, ask the user to do it in the open tab and reply "done".
4. Optional reading: `examples/` (worked jobs to imitate), `docs/video-prompting.md` (multi-shot video prompting) and `skills/realistic-consistent-character-videos/references/` (UI click map).

## What NOT to do
- Do not run any commands, scripts, tests, installs, linters, Python, Node or shell.
- Do not build, validate, scan or package anything. There is no CLI.
- Do not run a capability audit, readiness check, model verification or approval gate.
- Do not ask the user for anything except the Section 1 intake (photos, story, accent, and duration asked every film), a photo upload you can't do, the one-time Consistent Character **I Agree** disclaimer, a sign-in, or a Terms/credits screen they must click themselves. Never click I Agree yourself.
- Do not make sexual, humiliating, hateful, political-impersonation, fake-news or deceptive content of the real people in the photos, and never work with photos of children.

## Why
Sandboxed agents such as Codex tend to launch local processes. The sandbox refuses them with a "process security error", which can also take down the browser runtime, and the job stops before any video is made. This workflow needs nothing but the browser.
