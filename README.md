# Arc for Chrome

Arc for Chrome brings an Arc-inspired sidebar workflow to Google Chrome. Organize open tabs and saved sites into Spaces and nested folders, keep frequently used sites in Top Apps, search Chrome history, and restore recently closed tabs from Archive.

> Arc for Chrome is an independent extension and is not affiliated with, endorsed by, or produced by The Browser Company or Google LLC.

## Highlights

- Left sidebar for open tabs, saved sites, Spaces, and folders
- Top Apps for frequently used websites
- Drag-and-drop organization, renaming, pinning, and reordering
- Search across open tabs, saved items, and Chrome history
- Archive for recently closed Chrome tabs and windows
- Local Arc migration on macOS, including locally available history and cached icons
- Exportable sidebar backups for moving between Chrome profiles
- Optional macOS compact-layout and theme-matching companion
- Keyboard shortcuts for the sidebar and previously used tab

## Install and set up

<https://chromewebstore.google.com/detail/mhmfcepflnlphogaaelglppgoljbkklm>

After installation:

1. Select Chrome's extensions button, pin **Arc for Chrome**, and open it.
2. Choose **Start fresh**, **Move from Arc**, or **Restore a backup**. Setup shows only the steps for that choice.
3. Select **Open Chrome appearance**, set Tab position to **Vertical**, and Chrome panels to **Left**.
4. Select **Finish setup**. Create Spaces with **+** and drag tabs onto a Space dot to move them.
5. Install the optional compact macOS helper later only if you want the edge-to-edge window layout.

Detailed setup and support: <https://eshwar-ila.github.io/arc-for-chrome/>

## Move from Arc on macOS

The migration helper creates one local `.arcsidebar` file. It can preserve Spaces, Top Apps, folders, saved tabs, titles, order, Archive, locally available Arc history, and cached icons.

1. [Download the migration helper](https://eshwar-ila.github.io/arc-for-chrome/arc-for-chrome-migration-helper-1.6.2.zip) and unzip it.
2. Open Arc once and wait for its sidebar to finish loading.
3. Control-click `Prepare Arc Migration.command`, select **Open**, then select **Open** again. This is the normal Gatekeeper approval for a downloaded local script.
5. In Arc for Chrome, choose **Move from Arc** and select the `.arcsidebar` file created in Downloads.

The helper reads local Arc data only when you run it. It has no updater, analytics, network connection, or publisher server.

## Move between Chrome profiles

1. In the source profile, open **Setup and privacy**.
2. Select **Export sidebar backup**.
3. In the destination profile, open Arc for Chrome setup.
4. Choose **Sidebar backup** and select the exported JSON file.

## Optional compact layout on macOS

The core sidebar works without the companion. The companion makes the compact window offset and Chrome theme matching more reliable.

1. [Download the compact-layout helper](https://eshwar-ila.github.io/arc-for-chrome/arc-for-chrome-macos-helper-1.6.2.zip) and unzip it.
2. In Arc for Chrome setup, select **Copy extension ID**.
3. Control-click `Install Arc for Chrome Helper.command`, select **Open**, then **Open** again, and paste the ID.
4. If Accessibility opens, select **+**, press **Command-Shift-G**, enter `/usr/bin/osascript`, select Open, and enable it.
5. Return to setup and select **Recheck helper**.

Run `uninstall-macos-helper.sh` from the downloaded helper to remove it. Arc for Chrome will then use Chrome's built-in window API.

## Keyboard shortcuts

| Action | macOS | Windows/Linux |
| --- | --- | --- |
| Open or close the sidebar | `Control+S` | `Alt+S` |
| Switch to the previously used tab | `Control+Q` | `Alt+Q` |

Shortcuts can be changed at `chrome://extensions/shortcuts`.

## Privacy

Arc for Chrome is local-first:

- No account
- No analytics or advertising
- No browsing data sent to the developer
- No sale or sharing of user data
- Imports and backups are processed on the user's device

Chrome permissions are used only to provide the visible sidebar features:

| Permission | Purpose |
| --- | --- |
| `tabs` | Display, activate, create, close, move, and pin tabs |
| `history` | Search Chrome history locally |
| `sessions` | Show and restore recently closed tabs and windows |
| `storage` | Save Spaces, folders, Top Apps, preferences, and imported data locally |
| `favicon` | Display website icons |
| `sidePanel` | Render the primary sidebar interface |
| `nativeMessaging` | Communicate with the optional local macOS companion when installed |
| `system.display` | Keep the compact window aligned to the monitor containing Chrome |

Read the full [privacy policy](https://eshwar-ila.github.io/arc-for-chrome/privacy.html).

## Downloads and verification

- [Arc migration helper 1.6.2](https://eshwar-ila.github.io/arc-for-chrome/arc-for-chrome-migration-helper-1.6.2.zip)
- [macOS compact-layout helper 1.6.2](https://eshwar-ila.github.io/arc-for-chrome/arc-for-chrome-macos-helper-1.6.2.zip)
- [SHA-256 checksums](https://eshwar-ila.github.io/arc-for-chrome/CHECKSUMS.txt)

## Troubleshooting

### The sidebar does not open

Open Chrome's extension menu, select Arc for Chrome, and pin it. You can also use the sidebar shortcut listed above.

### macOS blocks a helper

Control-click the `.command` file, select **Open**, then select **Open** in the confirmation. Download helpers only from the official support page and compare their SHA-256 checksum if desired. The migration helper reads Arc locally and creates one file in Downloads. The optional compact helper can move the front Chrome window and read Chrome's saved theme choice; it cannot read tabs, history, pages, passwords, accounts, or network traffic.

### Accessibility does not show osascript

Select **+**, press **Command-Shift-G**, enter `/usr/bin/osascript`, select Open, and enable it. Return to setup and select **Recheck helper**.

### History or Archive is empty

History shows browsing history available in the current Chrome profile. Archive shows recently closed Chrome tabs and windows. Arc history requires an Arc migration bundle created on the Mac where Arc data is available.

### Website icons are missing after import

Use the macOS Arc migration helper rather than Arc's official export. The migration bundle includes locally cached icons when they are available.

### Remove all extension data

Remove Arc for Chrome from Chrome and choose to clear its data. There is no publisher account or remote copy to delete.

## Repository contents

This repository hosts the public setup guide, privacy policy, checksums, and optional macOS helper downloads. The packaged Chrome extension is distributed through the Chrome Web Store.

For help, open an issue in this repository.
