# StatePort releases

This is the official public binary distribution channel for StatePort, maintained by [StatePort-Dev](https://github.com/StatePort-Dev).

## Install for coding agents

```sh
npx stateport@latest
```

Use Node.js 24.x. The stable transparent installer downloads and verifies the
signed platform engine, then offers Codex, Claude Code, Cursor and VS Code/Copilot
setup. System Chrome/Edge is used by default; pinned Chromium is a separate
optional download. Desktop is optional. Installation does not start a trial.

Installer, engine and skills have independent versions. A new install resolves
the signed stable engine; existing pins and update consent are preserved.
The default update policy is Notify. See the
[installation guide](https://github.com/StatePort-Dev/stateport-agent-skills/blob/main/AGENT_INSTALL.md)
and [npm package](https://www.npmjs.com/package/stateport).

## Start with a State Card

StatePort saves a supported browser and API bug setup as a reviewed **State Card**. Reopen that Card against your running local app after a code change, then compare the runs without rebuilding the setup.

- [Download the current prerelease](https://stateport.dev/download/?utm_source=github&utm_campaign=releases_readme) — check the exact version, operating system, architecture, and installer before downloading. The download page is the source of truth for availability.
- [Capture your first State Card](https://docs.stateport.dev/getting-started/first-state-card/) — capture, review, and save a reproduction in the managed browser.
- [Reproduce a saved Card](https://docs.stateport.dev/getting-started/open-a-state/) — work against current local code. Capture is free; reproduction and comparison need Developer access, with a 14-day trial that requires no payment card.
- [Connect a coding agent](https://github.com/StatePort-Dev/stateport-agent-skills/blob/main/AGENT_INSTALL.md) — use the npm installer, or the optional Desktop setup. Account/model access and host trust remain separate from installation.

Installers and their integrity files are published as this repository's [GitHub Releases](https://github.com/StatePort-Dev/stateport-releases/releases). The `main` branch contains distribution documentation and issue/PR templates; binaries are release assets, not files committed to Git.

The StatePort application source code is maintained separately. This repository's public visibility and its documentation reuse permission do **not** make the application open source or grant a license to its binaries. See [DISTRIBUTION.md](DISTRIBUTION.md) for the distinction and [RELEASES.md](RELEASES.md) for release names and verification expectations.

For installer, update, or download problems, use the [issue form](https://github.com/StatePort-Dev/stateport-releases/issues/new/choose). **Do not disclose vulnerabilities in a public issue**; follow [SECURITY.md](SECURITY.md) instead.
