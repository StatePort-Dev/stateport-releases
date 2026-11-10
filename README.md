# StatePort releases

This is the official public binary distribution channel for StatePort, maintained by [StatePort-Dev](https://github.com/StatePort-Dev).

## Install for coding agents

```sh
npx stateport@latest
```

Use Node.js 24.x. The stable transparent installer downloads and verifies the
signed platform engine, then automatically configures every detected supported
Codex, Claude Code, Cursor and VS Code/Copilot connection. Add `--choose-agents`
for the optional interactive picker. System Chrome/Edge is used by default; pinned Chromium is a separate
optional download. Installation does not start a trial.

Installer, engine and skills have independent versions. A new install resolves
the signed stable engine; existing pins and update consent are preserved.
The default update policy is Notify. See the
[installation guide](https://docs.stateport.dev/getting-started/install/)
and [npm package](https://www.npmjs.com/package/stateport).

Current versions: transparent installer **1.1.0**, signed runtime **1.1.0**, skills
**beta.84**. Claude Code IDE extensions are detected without a standalone CLI.
Versioned data compatibility permits recognized older installs to preserve Cards.
Known agent connections migrate automatically with private scoped records; Claude
standalone setup needs no third-party marketplace and preserves corporate policy.
Functional checks for this release ran locally on Ubuntu; native archives were
built on three OSes without remote functional qualification.
Protected per-agent conflicts remain visible while setup continues for others.
Package publication and native build checks do not establish every coding-host,
model or human workflow.

## Start with a State Card

StatePort saves a supported browser and API bug setup as a reviewed **State Card**. Reopen that Card against your running local app after a code change, then compare the runs without rebuilding the setup.

- [Capture your first State Card](https://docs.stateport.dev/getting-started/first-state-card/) — capture, review, and save a reproduction in the managed browser.
- [Reproduce a saved Card](https://docs.stateport.dev/getting-started/open-a-state/) — work against current local code. Capture is free; reproduction and comparison need Developer access, with a 14-day trial that requires no payment card.
- [Connect a coding agent](https://docs.stateport.dev/getting-started/install/) — use the npm installer. Account/model access and host trust remain separate from installation.

Signed runtime archives and their integrity files are published as this repository's [GitHub Releases](https://github.com/StatePort-Dev/stateport-releases/releases). The `main` branch contains distribution documentation and issue/PR templates; binaries are release assets, not files committed to Git.

The StatePort application source code is maintained separately. This repository's public visibility and its documentation reuse permission do **not** make the application open source or grant a license to its binaries. See [DISTRIBUTION.md](DISTRIBUTION.md) for the distinction and [RELEASES.md](RELEASES.md) for release names and verification expectations.

For installer, update, or download problems, use the [issue form](https://github.com/StatePort-Dev/stateport-releases/issues/new/choose). **Do not disclose vulnerabilities in a public issue**; follow [SECURITY.md](SECURITY.md) instead.
