# FocusGuard FAQ

## What is FocusGuard?

FocusGuard is a Windows productivity app that blocks selected executables until a configured unlock time. It helps you maintain focus by preventing access to distracting applications.

## Can I lock multiple apps?

Yes. Each lock is independent and can have its own reason and unlock time. You can manage multiple locks simultaneously from the app's interface.

## What is emergency unlock?

Emergency unlock pauses lock enforcement for 15 minutes so you can recover from accidental lock setups. This safety feature should be used responsibly.

## Why does emergency unlock message sometimes stay visible?

This was fixed in recent versions. The status now resets automatically once emergency unlock expires.

## Does FocusGuard auto-update?

Yes. It can check updates on startup, download in the background, and restart automatically to install new versions. You can configure this in Settings.

## Why did I see the default Electron icon before?

Some packaged builds were missing runtime icon paths. This was fixed by packaging `assets/**` and adding robust icon resolution fallbacks. Current versions display the FocusGuard icon correctly.

## Can I choose a different language?

Yes. Use **Settings > Language** and choose from: English, Dutch, Swedish, German, Spanish, or French. All UI text, buttons, and messages will change immediately.

## Is FocusGuard anti-tamper software?

No. FocusGuard is user-space productivity software, not a kernel-level security or anti-cheat system. It runs with your user permissions and is designed for personal focus management.

## Can someone else publish updates to my release repo?

Only users with repository write permissions and a valid GitHub token can publish releases. Keep your tokens private and never share them.

## Where are release installers hosted?

Installers are published at:

- https://github.com/Squiddoo/focusguard-releases/releases

Each release includes:
- `FocusGuard-Setup-X.X.X.exe` (installer)
- `FocusGuard-Setup-X.X.X.exe.blockmap` (incremental update data)
- `latest.yml` (auto-update metadata)

## How do I create and publish a new version?

1. Bump version in `package.json`
2. Add changelog notes in `CHANGELOG.md`  
3. Run `npm run dist:win` to build the installer
4. Run the publish script:
   ```powershell
   powershell -NoProfile -ExecutionPolicy Bypass -File ./scripts/publish-release.ps1 `
     -Owner Squiddoo `
     -Repo focusguard-releases `
     -Tag v1.0.14 `
     -ReleaseDir ./release `
     -ChangelogPath ./CHANGELOG.md
   ```

The publish script will handle changelog sync, asset upload, and README updates automatically.

## What languages does FocusGuard support?

FocusGuard supports 6 languages with complete UI translation:
- 🇬🇧 English
- 🇳🇱 Dutch (Nederlands)
- 🇸🇪 Swedish (Svenska)
- 🇩🇪 German (Deutsch)
- 🇪🇸 Spanish (Español)
- 🇫🇷 French (Français)

## Is there a development version?

Yes. Check the main project repository for source code, contribution guidelines, and development setup.

## Why is GH_TOKEN mentioned in the publish script?

The release script needs GitHub credentials to upload installers and update release metadata. Set `GH_TOKEN` as an environment variable with a Personal Access Token that has `repo` and `workflow` scopes.

## How long can I lock an app for?

For safety, single locks are limited to **365 days**. You can create multiple locks if you need longer periods.

## What happens to my settings when FocusGuard updates?

Your locks and all settings (language choice, notifications preferences, fullscreen setting, etc.) are preserved during updates. Updates are transparent and don't require manual action.

## Can I use FocusGuard on multiple computers?

Yes. FocusGuard settings are stored locally per computer. You can install it on multiple machines independently. Locks and settings do not sync between computers.

---

**Need more help?** Check the [main project repository](https://github.com/Squiddoo/focusguard) for additional resources and contribution information.
