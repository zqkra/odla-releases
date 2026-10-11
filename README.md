<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/odla-logo-dark.svg">
    <img alt="Odla" src="assets/odla-logo-light.svg" width="320">
  </picture>
</p>

<h3 align="center">The agentic development environment, built to be the best in the world.</h3>

<p align="center">
  Run Claude Code, Codex and Pi side by side, let them open subagents, and watch every change land.<br>
  Fast, light and focused, with the files, terminal and browser in the same window.
</p>

<p align="center">
  <a href="https://github.com/zqkra/odla-releases/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/zqkra/odla-releases?label=release&color=111111&labelColor=111111"></a>
  <img alt="macOS on Apple silicon" src="https://img.shields.io/badge/macOS-Apple%20silicon-111111?logo=apple&logoColor=white&labelColor=111111">
  <a href="https://github.com/zqkra/odla-releases/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/zqkra/odla-releases/total?color=111111&labelColor=111111"></a>
</p>

<p align="center">
  <a href="https://github.com/zqkra/odla-releases/releases/latest/download/Odla-0.1.0-arm64.dmg"><strong>Download Odla 0.1.0 for Mac</strong></a>
  &nbsp;·&nbsp;
  <a href="#install">Install</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/zqkra/odla-releases/issues/new">Report a bug</a>
</p>

<br>

<p align="center">
  <img alt="Odla with a chat on the left and the Files panel showing syntax-coloured Rust on the right" src="assets/screenshot-workspace.png" width="100%">
</p>

## Why Odla

Most tools for coding agents are either a terminal you have to babysit or a heavy editor with an agent bolted on. Odla is built around the agents themselves: every decision in it serves one goal, getting good work out of many agents with the least effort and the least noise.

- **Fast.** Odla opens in under a second on Apple silicon, and heavy viewers such as PDF and charts load only when you open them.
- **Focused.** One primary action per screen, no automation clutter, and quiet states that tell you only what changed.
- **Honest.** You always see what an agent is doing, how full its context is, and what it changed before you merge.
- **Native.** Liquid glass, smooth motion and keyboard shortcuts that feel at home on a Mac.

## Features

### Agents

- **Every major agent.** Claude Code, Codex, Pi and agents that speak the Agent Client Protocol, each with its own models and effort levels.
- **Subagents first.** A parent agent opens children, and they report back. The orchestration map shows who opened whom and what each one is doing right now.
- **Steer at any time.** Send a message while an agent works and it reaches the running turn. Queue the next one or stop with a click.
- **Autonomy levels.** Ask, Edit, Build or Full, chosen per chat.

### Workspace

- **Files.** Type icons, syntax colours in the Odla palette, wrapped lines, and previews for images, SVG, PDF, video, audio and Markdown.
- **Terminal.** The chat's own shell, in the project folder, next to the conversation.
- **Browser.** A built-in browser that agents can drive for real QA, with a floating view while they work.
- **Review.** Every change an agent makes, as a diff, before it lands.

### Insight

- **Context meter.** See how full each agent's context window is, what fills it, and where auto-compaction starts.

  <img alt="The context panel with a cell grid, a legend of categories and the auto-compaction point" src="assets/screenshot-context.png" width="100%">

- **Usage.** Your agent subscriptions and their limits at a glance.
- **Charts and diagrams.** Agents answer with real charts and diagrams right in the chat.
- **Artifacts and memory.** Tickets, plans and notes that agents read, and a memory they share.

## Install

1. Download [`Odla-0.1.0-arm64.dmg`](https://github.com/zqkra/odla-releases/releases/latest/download/Odla-0.1.0-arm64.dmg).
2. Open it and drag Odla into the Applications folder.
3. This build is not signed with an Apple Developer ID yet, so macOS blocks the first launch and may say the app is damaged. Run this once in Terminal:

   ```sh
   xattr -dr com.apple.quarantine /Applications/Odla.app
   ```

4. Open Odla and sign in to an agent.

To check that the download is intact, compare its checksum with `SHA256SUMS.txt` from the same release:

```sh
shasum -a 256 ~/Downloads/Odla-0.1.0-arm64.dmg
```

## Requirements

| | |
| --- | --- |
| Mac | Apple silicon (M1 or later). Intel Macs are not supported. |
| macOS | 13 Ventura or later |
| Agent | An account with at least one supported agent, for example Claude Code or Codex |

## Update

Odla does not update itself yet. Download the newest release, quit Odla and replace the app in the Applications folder. Your chats and settings stay in `~/.odla`.

## Uninstall

Quit Odla and move it to the Trash. To delete your chats and settings as well, remove `~/.odla` and `~/Library/Application Support/Odla`.

## Feedback

Odla is in early testing, and every report helps. [Open an issue](https://github.com/zqkra/odla-releases/issues/new) with your macOS version, the Odla version (Odla > About Odla) and the steps that lead to the problem.

## License

The builds in this repository are provided for testing. Odla includes open source software, listed with its licenses in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
