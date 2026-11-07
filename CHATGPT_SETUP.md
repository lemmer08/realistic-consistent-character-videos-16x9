# Using this workflow in ChatGPT (Mac and Windows)

## The one setting that matters: Full access
ChatGPT's browser automation runs through a process launcher. In the default **Ask for approval** mode that launcher is sandboxed, and the browser tool can't start. You then see errors like:

> "the local process launcher failed, and the browser-control session exited unexpectedly"
> "both the file reader and the browser-control runtime failed to start with the same process security error"

Once **Full access** is on, the same prompt works. The prompt's first message tells users this before it asks for photos and a story, so nobody gets stuck.

### Turn it on (one time)
1. Open ChatGPT **Settings → General → Permissions** and turn on **Full access**.
2. Back in the chat, open the **permissions menu in the message box** and choose **Full access** for that chat. Turning it on in Settings only adds it to the menu; it doesn't switch an existing chat.
3. **Mac only:** when macOS asks, allow **Screen Recording** and **Accessibility** for ChatGPT (System Settings → Privacy & Security). Without them ChatGPT can see the browser but not click in it.
4. If **Full access** isn't offered, your plan or organization has turned it off. Run the workflow in Claude in Chrome or the Claude desktop app instead.

Full access lets ChatGPT run commands and edit files without asking, so use it in a chat dedicated to this workflow, and switch back afterwards if you prefer.

## Attaching your photos
- **Which photos:** 1–2 per person, face clearly visible, good light, no heavy filter, sunglasses or hat hiding the hair. **Best: a close, sharp, front-facing head-and-shoulders photo** (selfie distance) where the face fills much of the frame; a second at a slight angle helps. In testing, a full-body photo with a small face produced a younger, slimmer stranger, while the same person's tight face photo gave a clear likeness. Adults only. If a photo shows several people, say which one is the character.
- **How:** in the same message where you answer the intake question, click the **+ / paperclip** in the message box (or drag the files in) and add the images. Name them in your text, e.g. "Photos 1–2 are Maya, photo 3 is Leo".
- **Getting them into VideoExpress:** the agent uploads them to **Media Library → My Media → Images → Upload file** (the **Upload Media** dialog: **+ Add files**, jpg/jpeg/png/gif up to 15 MB each, a **Media name** per file, then **Upload files**) and picks them into **Use Consistent Character → Reference Photo** / **Reference Photo 2**. Some browser tools can't reach files attached to the chat. Then the agent asks you to upload them yourself the same way, named `[Name] - reference photo`, and reply `done`. Keep the photo files somewhere easy to find on your computer for this. (The Import Media panel has no file upload; use the Media Library.)
- **One-time disclaimer:** the first time **Use Consistent Character** is ticked, VideoExpress shows a **Disclaimer** (no celebrities or famous people; you accept all legal liability; VideoExpress shares information if there are legal claims). Read it and click **I Agree** yourself; the agent won't accept it for you.
- **Consent:** only use photos of people who agreed to it (yourself, a colleague, a client).

## Run the workflow
1. Open a **new chat** in the ChatGPT app with **Full access** selected and Agent/browser mode available.
2. Paste the short prompt from `SYSTEM_PROMPT.md` (everything below the line). You can attach the photos and fill in the lines at the bottom of the prompt in the same message.
3. ChatGPT's first message shows the Full access NOTE and asks for photos, names, story and accent. Reply with the photos attached.
4. ChatGPT opens the full instructions from this public GitHub repo in its browser (`https://raw.githubusercontent.com/lemmer08/realistic-consistent-character-videos-16x9/main/PLAYBOOK.md`, no login needed), then produces, trims and exports.
5. Upload the photos into Media Library → My Media → Images, click **I Agree** on the one-time Consistent Character disclaimer, sign in to VideoExpress or accept its one-time Terms screen when asked, then reply `done`.

## Optional: make it one click (Project or custom GPT)
1. Create a ChatGPT **Project** (or a custom GPT → Configure).
2. Paste the short prompt (below the line in `SYSTEM_PROMPT.md`) into its **Instructions**.
   - Alternative: paste `PROMPT_COMPACT.md` (under 8,000 characters) to keep the core instructions there too, as a backup when GitHub is unreachable.
3. Start each new chat in that project with Full access selected, attach the photos and type: `Maya (Australian), Leo (British). Story: …`

Don't upload the prompt as a Knowledge file, and don't put the reference photos in Knowledge either. Put the prompt in the Instructions box and attach the photos to the chat message.

## If something goes wrong

| What ChatGPT says | Do this |
|---|---|
| "process launcher failed", "process security error", "browser-control session exited" | Full access isn't selected for this chat. Do the 3 steps above, then reply `done`. ChatGPT starts a new browser session and continues; finished clips are safe in My AI Videos. |
| "can't access the pasted prompt", "file read is failing" | Same cause, plus the file reader was blocked. Set Full access, then paste the short prompt in a new chat. |
| "I can't upload the photos" | Normal for some browser tools. In the open VideoExpress tab: **Media Library → My Media → Images → Upload file → + Add files**, name them `[Name] - reference photo`, **Upload files**, and reply `done`. |
| VideoExpress shows a Consistent Character **Disclaimer** | One-time. Read it, click **I Agree** yourself, and reply `done`. |
| ChatGPT can see the browser but clicks do nothing (Mac) | Grant Screen Recording and Accessibility to ChatGPT in System Settings → Privacy & Security, then restart ChatGPT. |
| It can't reach GitHub | It falls back to the essentials built into the prompt. Or reply: `Open https://github.com/lemmer08/realistic-consistent-character-videos-16x9/blob/main/PLAYBOOK.md instead.` |
| It asks before following the GitHub page | Reply: `Yes. That's my playbook, follow it.` |
| It asks to approve steps or run an audit | Reply: `No audits or approvals. Follow PLAYBOOK.md and keep producing.` |
| It refuses because the photos are of real people | Confirm in one line who they are and that you have their permission, e.g. `It's me and my colleague; we both agreed.` |
| Browser won't start even with Full access on | Restart the ChatGPT app and open a new chat with Full access selected. If it still fails, run the same prompt in Claude (Claude in Chrome or the Claude desktop app). |
