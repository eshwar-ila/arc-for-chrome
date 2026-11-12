# Changelog

## 1.6.12 — November 12, 2026

- Added drag-and-drop reordering for Chrome's real open tabs.
- Added saved-tab to Open-tabs drag and drop.
- Added same-window duplicate URL prevention: existing tabs are focused and refreshed instead of opening another copy.
- Added automatic cleanup of existing same-window duplicate tabs without adding cleanup closures to Archive.
- Added automatic Archive for web tabs inactive for 24 hours, checked locally about every 30 minutes.
- Protected active, pinned, audible, and Chrome-internal tabs from automatic Archive.
- Kept tab state and duplicate handling independent across Chrome windows.
- Set macOS shortcuts to Control+S for the sidebar and Control+Q for the previously active tab.
- Added shortcut status and a direct link to Chrome's shortcut settings.
- Improved theme fallback so a missing optional helper follows the device light/dark appearance instead of forcing black.
- Added the alarms permission solely for the local inactive-tab Archive schedule.
