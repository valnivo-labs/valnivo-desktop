# Valnivo for the desktop

Valnivo as an application you install, rather than a site you visit. Every version is under
[Releases](../../releases); the newest files are always at

- macOS — <https://github.com/valnivo-labs/valnivo-desktop/releases/latest/download/Valnivo-macos.zip>
- Windows — <https://github.com/valnivo-labs/valnivo-desktop/releases/latest/download/Valnivo-windows.exe>

This repository holds no code. Valnivo is not open source; only the packages are published here.

**You do not need any of this to use Valnivo.** The app runs in a browser at <https://valnivo.eu>
with the same features, and your figures live on your own machine either way.

## Opening it the first time

It is **not signed by a developer certificate**, and both operating systems will say so. They are
right: your computer cannot tell who produced the file. That is what the SHA-256 on each release is
for — `shasum -a 256 Valnivo-macos.zip`, or `Get-FileHash Valnivo-windows.exe` in PowerShell.

- **macOS** refuses the first open with *"Apple could not verify Valnivo is free of malware or may
  harm your Mac"*, and offers only **Move to Trash** or **Done**. Press **Done**, then open
  **System Settings → Privacy & Security**, scroll down to Security, and press **Open Anyway**
  beside Valnivo. Recent versions of macOS removed the old right-click → Open shortcut, so that is
  the way now. From a Terminal, `xattr -dr com.apple.quarantine Valnivo.app` does the same thing.
- **Windows** shows a SmartScreen warning. **More info**, then **Run anyway**.

## Before you install

- **It does not update itself.** The website changes; a copy on your disk does not, until you
  replace it with a newer one from here.
- **It opens its window using a browser you already have** — Chrome, Edge or Chromium. Safari cannot
  be used for it.
- **Your ledger lives in a profile beside the application**, not in your normal browsing. Deleting
  that folder deletes your figures, and nobody else holds a copy. Export from Settings → Your data.

## Something wrong?

Bugs and ideas go to [the feedback repository](https://github.com/valnivo-labs/valnivo-feedback/issues),
not here. Issues are disabled on this one.
