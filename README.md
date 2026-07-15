# ZUS — Releases

Official installers for **ZUS**, a fast, lightweight AI IDE by [Siden Technologies](https://github.com/8syncdev).

This repository hosts release binaries only. Head to the [**Releases**](https://github.com/8syncdev/zus-releases/releases/latest) page to download.

## Install

### Windows
Download `ZUS_x.y.z_x64-setup.exe` from the latest release, or:

```powershell
# Scoop
scoop bucket add zus https://github.com/8syncdev/scoop-zus
scoop install zus

# winget
winget install 8syncdev.ZUS
```

> **SmartScreen note:** installers are not yet code-signed. If Windows shows
> "Windows protected your PC", click **More info → Run anyway**. Verify your
> download against `SHA256SUMS.txt` below first.

### macOS (Apple Silicon)
Download `ZUS_x.y.z_aarch64.dmg`. The app is unsigned — on first open:
right-click the app → **Open** → **Open**, or run
`xattr -dr com.apple.quarantine /Applications/ZUS.app`.

### Linux
- Debian/Ubuntu: `sudo apt install ./ZUS_x.y.z_amd64.deb`
- Fedora/RHEL: `sudo dnf install ./ZUS-x.y.z-1.x86_64.rpm`
- Any distro: `ZUS_x.y.z_amd64.AppImage` (`chmod +x` then run)

## Verify a download

```bash
sha256sum -c --ignore-missing SHA256SUMS.txt
```

`SHA256SUMS.txt` is attached to each release. Update artifacts (`.sig`,
`latest.json`) are signed with the ZUS updater key; the app verifies them
automatically.

## Auto-updates

Installed apps check `latest.json` in the latest release here and update
themselves in place.
