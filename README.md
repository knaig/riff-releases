# riff - releases

This repo hosts the downloadable install packages for [riff](https://riff-site-chi.vercel.app). It has no source code; the source is private. Each release is a packed npm tarball.

A team of AI characters that builds with you, on the record. Riff runs on your
own computer, opens in your browser, and talks, listens and draws diagrams while
you work. You bring one API key; your messages go to the model provider that
key belongs to, and riff itself keeps everything else on your machine.

Free. Runs locally at `127.0.0.1`. Windows 10/11 and macOS, with Chrome, Edge
or Safari 16.4+.

## Install on Windows

1. **Install Node 22 or newer.** Download the LTS installer from
   [nodejs.org](https://nodejs.org) and accept the defaults. Then open
   **PowerShell** from the Start menu and check:

   ```powershell
   node -v
   ```

   It should print `v22` or higher. If it does not, close PowerShell and open a
   new window.

2. **Install riff.** Paste this into PowerShell:

   ```powershell
   npm install -g riff-build
   ```

   If PowerShell says `running scripts is disabled on this system`, run this
   once, then repeat the install:

   ```powershell
   Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
   ```

3. **Open riff.**

   ```powershell
   riff launch
   ```

   Your browser opens a page that lists your projects, with Open and Stop
   buttons. To open one project directly, use its full path:

   ```powershell
   riff start C:\Users\you\Projects\myapp
   ```

4. **Paste your key.** On first run the browser shows a settings page. Paste one
   OpenRouter key from [openrouter.ai/keys](https://openrouter.ai/keys) and click
   Save. Riff checks chat, listening and speaking, then shows "Open the room".
   The one key covers all three. You can enter your own keys for any of them
   under "Other providers and models".

5. **When you are done:** `riff stop --all`.

## Install on macOS

1. Install Node 22 or newer from [nodejs.org](https://nodejs.org), then open
   **Terminal** and check `node -v`.
2. Install riff:

   ```sh
   npm install -g riff-build
   ```

3. Run `riff launch`, or `riff start ~/Projects/myapp`.
4. Paste your OpenRouter key on the settings page, as above.

## What works

| | Windows | macOS |
|---|---|---|
| Room, cast, typed chat, canvas and diagrams | yes | yes |
| Voice in the browser (microphone and speaker) | yes | yes |
| Hands-free call | not yet confirmed | needs `brew install livekit` |
| Watching your screen or coding terminal | not yet | yes |

Windows has not been through automated tests yet. If a step fails, copy the
error text and send it to us.

## Update

Run `npm install -g riff-build@latest`.

## Troubleshooting

- **`riff` is not recognized:** close the terminal and open a new window so it
  picks up the new PATH.
- **`node` is not recognized:** repeat step 1, then open a new window.
- **No key yet:** the room still runs on a built-in demo model, so you can look
  around before spending anything.

All releases: [github.com/knaig/riff-releases](https://github.com/knaig/riff-releases/releases).
