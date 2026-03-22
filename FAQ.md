# FocusGuard FAQ

## What is FocusGuard?

FocusGuard is a Windows productivity app that blocks selected executables until a configured unlock time. It helps you maintain focus by preventing access to distracting applications during work or study sessions.

## How does FocusGuard work?

1. Select an app you want to lock
2. Set a reason for the lock (e.g., "Study time")
3. Choose an unlock time
4. The app is blocked until that time passes
5. Windows-critical processes are protected and cannot be locked

## Can I lock multiple apps at once?

Yes. Each lock is independent and can have its own reason and unlock time. You can manage multiple locks simultaneously from the app's interface. This is useful if you want to block several distracting apps together (email, messaging, social media, etc.).

## What if I accidentally lock something too long?

Use **emergency unlock**. It pauses all locks for 15 minutes, giving you time to recover. This is the safety feature built in for exactly this situation.

## How long can I lock an app for?

You can lock an app for any duration up to **365 days**. If you need longer periods, you can create multiple locks that restart one after another.

## What is emergency unlock exactly?

Emergency unlock temporarily disables all active locks for 15 minutes. After those 15 minutes expire, all locks become active again. You can only use emergency unlock when you have at least one active lock.

## Can I set different unlock times for different apps?

Yes. Each lock has its own unlock time. You can have one app unlocking at 3 PM and another at 6 PM on the same day.

## Does FocusGuard use my computer's resources heavily?

No. FocusGuard is lightweight and uses minimal CPU and memory. It runs in the background without noticeable impact on performance.

## What happens if I restart my computer?

Your locks persist even after restart. They remain active until their unlock time, even if you turn off your computer.

## Can I see which apps are currently locked?

Yes. The app shows an "Active locks" section listing all locked apps, their paths, reasons, and remaining time until unlock.

## What if I need to unlock an app before the set time?

You can use **emergency unlock** to temporarily lift all locks for 15 minutes. This is the intended way to handle urgent situations. After 15 minutes, locks reactivate unless you remove them (removal requires emergency unlock first).

## Is there a way to remove a locked app permanently?

Yes, but it requires **emergency unlock** first. Once emergency unlock is active, you can confirm the removal by typing "REMOVE". This safety measure prevents accidental lock removal.

## Can I choose a different language?

Yes. Open **Settings > Language** and choose from:
- English
- Dutch (Nederlands)
- Swedish (Svenska)
- German (Deutsch)
- Spanish (Español)
- French (Français)

All UI text changes immediately when you select a new language.

## Do my settings (language, notifications, etc.) get saved?

Yes. All settings are saved locally on your computer:
- Language preference
- Notifications setting
- Fullscreen preference
- Auto-update preference

These settings persist between sessions and survive app updates.

## Does FocusGuard check for updates automatically?

Yes, if you enable "Auto-check updates on startup" in Settings. Updates download silently in the background and restart the app automatically after 3.5 seconds.

## Will updating FocusGuard delete my locks?

No. Updates preserve all your locks and settings. Everything is kept safe through the update process.

## Can I use FocusGuard on multiple computers?

Yes. FocusGuard works on each computer independently. Settings and locks do not sync between machines—each computer has its own separate configuration.

## Is FocusGuard an anti-cheat or security system?

No. FocusGuard is **user-space productivity software**, not a kernel-level security system. It runs with your user permissions and is designed for personal focus management. System-critical Windows processes cannot be locked for safety reasons.

## Can someone bypass FocusGuard?

Users with administrative privileges could technically bypass it since it's user-space software. FocusGuard is designed for voluntary personal focus management, not forced enforcement against skilled users.

## Does FocusGuard work with admin-level apps?

Some admin-level applications may not be lockable due to Windows protection. The app warns you if you try to lock Windows-critical processes, which are protected for system stability.

## What if an app crashes while locked?

That's fine. The lock remains active. You can use emergency unlock to temporarily lift it and close/restart the app if needed.

## Does FocusGuard block notifications from locked apps?

Yes, if you enable "Block notifications" in Settings. This prevents notifications from locked apps from interrupting your focus.

## Can I add a custom reason for each lock?

Yes. When creating a lock, you can add a reason like "Study time", "Deep work", "Project deadline", etc. This helps you remember why you locked the app.

## What if I forget why I locked something?

The app shows the reason you entered when creating the lock. Just check the "Active locks" section to see your note.

## Is there a log of my lock history?

FocusGuard doesn't keep a detailed history log, but you can see current active locks at any time. The app focuses on present and future locks rather than past activity logs.

---

**Still have questions?** The app includes a "Release docs" button that links to the official releases page for additional resources.

