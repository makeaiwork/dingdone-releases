<p align="center">
  <img src="screenshots/appicon.png" width="96" height="96" alt="DingDone app icon">
</p>

<h1 align="center">DingDone</h1>

<p align="center">
  <b>Voice notifications for Claude Code and Codex on macOS.</b><br>
  Start a long task, walk away, and hear when your coding agent needs you.
</p>

<p align="center">
  <a href="https://github.com/makeaiwork/dingdone-releases/releases/latest/download/DingDone.dmg"><b>Download for Mac</b></a>
  &nbsp;·&nbsp;
  <a href="https://dingdone.io">Website</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/makeaiwork/dingdone-releases/releases">Release notes</a>
  &nbsp;·&nbsp;
  <a href="PRIVACY.md">Privacy</a>
</p>

<p align="center">
  Apple silicon · macOS 13 or newer · signed and notarized by Apple · free, no account
</p>

---

> **"Claude Code, Kanvi, finished working."**
> **"Codex, benefits, is waiting for a response."**

DingDone is a small menu-bar app. When Claude Code or Codex finishes a task, asks a question,
needs a permission or stops with an error, DingDone plays a short chime and says which agent it
was, in which project, and what happened. You can stop watching the spinner and come back only
when something meaningful changes.

![DingDone overview: today's events, agent status and projects](screenshots/overview.png)

## What it does

- **Tells you who, where and what.** Every alert is built as *chime → agent name → project →
  event*, so you know what needs attention before you look at the screen.
- **Five meaningful events, nothing else.** Completion, waiting for your response, a reminder if
  you still haven't answered, an interim update from long background work, and errors. Routine
  tool calls, plan steps and dev servers left running in the background stay quiet.
- **Works where you already work.** Claude Code and Codex in the terminal or in VS Code. DingDone
  listens to the agents' own hook events. It does not watch your screen.
- **Speaks offline.** The free version uses the Apple voices already on your Mac. Notifications
  are available in 14 languages, and every phrase can be edited.
- **Names your projects properly.** The spoken name comes from the folder, with numeric prefixes
  like `42.` removed. You can set any name in the app.
- **Keeps a log.** See what was said and when, filter by agent or errors, and replay any alert.

## A closer look

**Sound & Phrases.** Pick a chime and a phrase for each event, set the speech rate and volume,
and choose how long DingDone waits before reminding you that an agent is still waiting.

![Sound & Phrases settings: speech rate, volume, agent names and per-event phrases](screenshots/sound.png)

**Voices.** Choose any installed macOS voice, or leave it on *Automatic* to get the best voice
installed for your language.

![Voices: macOS system voices with preview buttons](screenshots/voices.png)

**Log.** A day-by-day history of every spoken notification.

![Log of spoken notifications for Claude Code and Codex](screenshots/log.png)

<sub>Screenshots use demo projects.</sub>

## Get started

1. [Download `DingDone.dmg`](https://github.com/makeaiwork/dingdone-releases/releases/latest/download/DingDone.dmg)
   and drag DingDone to Applications.
2. Launch DingDone and pick a language and voice.
3. Open **Connections** and click **Connect** for Claude Code and/or Codex.
4. Restart your agent session so it picks up the new hooks.
5. Press **Test sound**. Setup usually takes about three minutes.

Connecting adds a clearly marked DingDone block to `~/.claude/settings.json` or
`~/.codex/config.toml`. DingDone backs up each file before changing it and keeps up to three
copies. Disconnecting removes only the DingDone block.

DingDone updates itself through a signed update feed. You can also check manually from the menu
bar.

## Free and Pro

The voice notifications described above are free, with no time limit and no account.

Pro is optional and adds:
- the **Agent Cockpit**, a widget at the edge of the screen with your active sessions;
- **jump to session**: click a notification to open that exact Claude Code session in VS Code;
- **more voices**: hosted voices, or your own ElevenLabs key.

You can try the widget free for 14 days inside the app.

## Privacy

- DingDone receives only the event type, the project folder and the session ID from the agent.
  It never reads or logs your prompts, your code or the agent's replies.
- Apple voices run entirely on your Mac.
- The local log keeps only the event type, the folder and the phrase that was spoken.
- Hosted voices (Pro) receive only the short notification phrase.

Read the full [privacy policy](PRIVACY.md).

## Support

Questions and bug reports: [support@dingdone.io](mailto:support@dingdone.io).

---

<sub>This repository hosts DingDone's signed release builds (see
[Releases](https://github.com/makeaiwork/dingdone-releases/releases)) and the Sparkle update
feed `appcast.xml` used by the app. The source code is not published here.</sub>
