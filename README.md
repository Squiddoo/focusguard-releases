# FocusGuard

FocusGuard is a Windows desktop app that helps users stay focused by temporarily blocking distracting applications until a chosen unlock time.

## Current Version

- App version: `1.0.12`
- Platform: Windows (x64)
- Distribution: NSIS installer with GitHub Releases auto-update

## Core Features

- App locking with independent timers per executable.
- Forced-close protection when a blocked app is launched.
- Emergency unlock mode (15 minutes) with safety constraints.
- Lock removal guardrails with explicit confirmation.
- Settings drawer with persistent preferences.
- First-open update notes sourced from GitHub release notes.
- Tray integration (open, minimize, quit, and single-click open).
- Language selection support with locale-based settings.

## Technology Stack

- Electron
- React
- Vite
- TypeScript
- electron-builder
- electron-updater

## Project Structure

- `electron/`: Electron main process, preload bridge, process guard logic.
- `src/`: React renderer UI and styling.
- `scripts/`: release and build automation scripts.
- `assets/`: app icon and brand assets used by installer/runtime.
- `release/`: generated installers and updater metadata.

## Local Development

Install dependencies:

```bash
npm install
```

Run in development mode:

```bash
npm run dev
```

## Build and Packaging

Build renderer and Electron bundles:

```bash
npm run build
```

Create Windows installer:

```bash
npm run dist:win
```

Output artifacts are written to `release/`.

## Auto-Update and Release Workflow

FocusGuard uses `electron-updater` with GitHub Releases.

1. Bump version in `package.json`.
2. Add a matching entry in `CHANGELOG.md`.
3. Build installer artifacts.
4. Publish via script:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File ./scripts/publish-release.ps1 -Owner Squiddoo -Repo focusguard-releases -Tag v1.0.12 -ReleaseDir ./release -ChangelogPath ./CHANGELOG.md
```

The publish script automatically:

- Creates or updates the tagged GitHub release.
- Keeps only updater-required assets:
	- `FocusGuard-Setup-<version>.exe`
	- `FocusGuard-Setup-<version>.exe.blockmap`
	- `latest.yml`
- Syncs release notes from `CHANGELOG.md`.
- Updates README release references (remote + local).

## Runtime Behavior Notes

- Lock enforcement runs in user space and polls running processes.
- Emergency unlock expires automatically and enforcement resumes.
- Window close hides to tray unless user explicitly quits.
- Auto-update can install silently and restart the app.

## Security Notes

- Never commit secrets or personal access tokens.
- Keep `GH_TOKEN` private and scoped minimally.
- Rotate token immediately if exposure is suspected.

## Product Limitations

- FocusGuard is a productivity guard, not a kernel-level anti-tamper system.
- Admin-level users can still bypass restrictions outside normal user flow.

## Support and Releases

- Release repository: `https://github.com/Squiddoo/focusguard-releases`
- Main repository (code/issues): `https://github.com/Squiddoo/focusguard`



