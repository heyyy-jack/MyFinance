MY FINANCE — UPDATE (Firebase removed)

Replace these files in the ROOT of your GitHub repository:
- index.html
- service-worker.js

Keep manifest.json and the icons folder unchanged.

What changed
- Firebase and push notifications removed (no Firebase scripts, config, or device token).
- Service worker now only provides offline caching. Pages load network-first, so UI updates reach users without bumping cache versions.
- Budget alerts and daily summaries appear under the bell icon while the app is open.
- Fixed: "Clear" in notifications no longer brings the same alerts back.
- Fixed: "today" now uses your local date (previously UTC, which showed yesterday's date between midnight and 05:30 IST).
- "Saved" on the Summary is renamed "Left over" (income minus expenses).
- Accessibility: form labels are linked to inputs, dialogs close with Escape, larger delete buttons, decimal keypad for amounts.
- Your local data key (myFinance_v1) is unchanged, so existing data is kept.

After deploying
1. Reopen the installed app once online so the new service worker takes over.
2. You can delete the Firebase project in the Firebase Console; the app no longer uses it.
