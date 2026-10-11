# Odla

Odla is an agentic development environment for macOS. It runs coding agents such as Claude Code, Codex and Pi in parallel chats. Each agent works in its own workspace, and the files, terminal, browser and orchestration map sit next to the conversation.

This repository hosts the macOS builds of Odla. The source code is not public yet.

## Requirements

- A Mac with Apple silicon (M1 or later). Intel Macs are not supported.
- macOS 13 Ventura or later.
- An account with at least one supported coding agent, for example Claude Code or Codex. Odla asks you to sign in on first launch.

## Install

1. Download `Odla-0.1.0-arm64.dmg` from the [latest release](https://github.com/zqkra/odla-releases/releases/latest).
2. Open the file and drag Odla into the Applications folder.
3. This build is not signed with an Apple Developer ID yet, so macOS blocks the first launch and may say the app is damaged. Open Terminal and run this once:

   ```sh
   xattr -dr com.apple.quarantine /Applications/Odla.app
   ```

4. Open Odla from the Applications folder.

To check that the download is intact, compare its checksum with `SHA256SUMS.txt` from the same release:

```sh
shasum -a 256 ~/Downloads/Odla-0.1.0-arm64.dmg
```

## Update

Odla does not update itself yet. Download the newest release, quit Odla, and replace the app in the Applications folder. Your chats and settings stay in `~/.odla`.

## Uninstall

1. Quit Odla and move it from the Applications folder to the Trash.
2. To delete your chats and settings as well, remove `~/.odla` and `~/Library/Application Support/Odla`.

## Feedback

Found a bug or have an idea? [Open an issue](https://github.com/zqkra/odla-releases/issues/new). Include your macOS version, the Odla version (Odla > About Odla) and the steps that lead to the problem.

## License

The builds in this repository are provided for testing. Odla includes open source software, listed with its licenses in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
