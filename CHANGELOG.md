# Changelog

## 1.6.20

- The launcher opens over the active webpage with a translucent backdrop. On protected Chrome pages it opens in a separate tab. Escape dismisses it.
- The search field stays in place and appears in the sidebar theme on first paint. Web search comes first, followed by up to five matches each from Open tabs, Archive, and History.
- Includes the sidebar resizing improvements from 1.6.19 and uses the same macOS layout helper.

## 1.6.19

- The launcher search field stays in place as matches appear or disappear. Long result lists scroll beneath it.

- Drag the handle on the right edge of the compact macOS sidebar to make it narrower or wider. Closing the panel restores the window.
- Store users upgrading from the older layout helper can download the 1.6.19 helper in sidebar settings. The migration helper is unchanged.

## 1.6.14 — November 23, 2026

- Focused already-open saved tabs without refreshing them or resetting their current page state.
- Added a separate Return to saved URL control when a saved tab navigates elsewhere.
- Kept the close action and saved sidebar structure unchanged.

## 1.6.13 — November 23, 2026

- Opened saved folder links in place without duplicating them under Open tabs.
- Kept redirected websites associated with their original saved sidebar row.
- Added an X to the active saved row that closes its temporary live tab, returns to the previous tab, and preserves the saved link.

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
