<img width="963" height="556" alt="godspeed" src="https://github.com/user-attachments/assets/4f4cf6cd-c482-41e2-9fb2-414551336a62" />

# GODspeed

An FTP client specifically built for managing files on JTAG/RGH/DevKit Xbox 360 consoles, with real game names and thumbnails instead of cryptic folder IDs.

## Features

- FTP connection to Xbox 360 running Freestyle Dash, XeXMenu, DashLaunch FTPdll, or Aurora
- Displays real game names and thumbnails instead of folder IDs
- Automatic Gamertag and Gamer picture extraction from profiles
- Automatic game information gathering from game folders and Xbox Unity
- Automatic SVOD package recognition (DLCs, Title Updates, gamesaves, etc.)
- STFS package browsing, content extraction and injection
- Folder size calculation over FTP
- Content-aware folder creation
- Remote Copy support between NAS and FTP (requires Telnet and LFTP)
- Compressed file support (Zip, Rar, Tar, GZip, 7Zip)
- Extended FSD/F3 support: content scan triggering, file hash verification, game/xex launch, shutdown, database checking and cleanup
- Limited PS3 support (multiMAN)

## Requirements

- Windows 10 or 11 (64-bit)
- .NET Framework 4.0 or newer — already built into Windows, no separate download needed
- An Xbox 360 running Freestyle Dash, XeXMenu, DashLaunch FTPdll, or Aurora with FTP enabled

## Download

Head over to the [Releases](../../releases) page to grab the latest installer or portable version.

### Usage

- Double click or Enter on the **New connection...** item in the Connections pane to create a new connection.
- Double click or Enter on a connection item to connect to an FTP (Aurora's default FTP Username and Password are `xboxftp`)
- Browse into your Content folder and wait for your profiles to be recognized. Result will be cached.
- Browse into your Games folder and wait for your games to be recognized. Result will be cached.
- If you see a game with a green Xbox icon and trimmed title, it means the game isn't installed on your console. GODspeed checked the title on covers.jqe360.com as a fallback.
- If you see **Unknown game** it means GODspeed couldn't find it on covers.jqe360.com either.
- Right click and select **Rename** to change an item's title.
- Right click on a profile and select **Recognize Titles from Profile** to update cached game information. More accurate than covers.jqe360.com but significantly slower.
- Network shares are not supported. Map a network drive first if you want to connect to a NAS.
- You can use Total Commander hotkeys in GODspeed: F keys, Alt+F1/F2 for drive change, Space and Ctrl+L for space calculation, etc.

## Building from Source

See [BUILD.md](BUILD.md).

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## Credits

Original project by [mercenaryntx](https://github.com/mercenaryntx/godspeed).  
Updated fork by [Pandoriaantje](https://github.com/Pandoriaantje/godspeed).  

---

<details>
<summary>Original README</summary>

## GODspeed — Original Project Description

GODspeed is a Total Commander like FTP client designed to fasten and clarify file management of JTAG/RGH/DevKit Xbox 360 consoles.

### Main features

- FTP connection to Xbox 360 with Freestyle Dash, XeXMenu, DLi and/or Aurora
- Instead of cumbersome IDs real names and thumbnails are displayed to see who is who and what is what
- Automatic Gamertag and Gamer picture extraction from profiles
- Automatic game information gathering from Game folders and Xbox Unity
- Manual game information gathering from profiles
- Automatic SVOD package recognition (DLCs, Title Updates, gamesaves, etc.)
- STFS package browsing, content extraction/injection
- Folder size calculation on FTP (most annoying deficiency of Total Commander)
- Content-aware folder creation
- Remote Copy support between NAS and FTP (Telnet and LFTP required)
- Compressed file support
- Extended FSD/F3 support:
  - Automatic Content scan triggering
  - File hash verification
  - Game launch
  - Xex launch
  - Shutdown
  - Database checking and disk clean up
- Limited support to PS3 (multiMAN)

### Usage

- Double click or Enter on the **New connection...** item in the Connections pane to create a new connection.
- Double click or Enter on a connection item to connect to an FTP.
- Browse into your Content folder and wait for your profiles to be recognized. Result will be cached.
- Browse into your Games folder and wait for your games to be recognized. Result will be cached.
- If you see a game with a green Xbox icon and trimmed title, it means the game isn't installed on your console. GODspeed checked the title on covers.jqe360.com as a fallback.
- If you see **Unknown game** it means GODspeed couldn't find it on covers.jqe360.com either.
- Right click and select **Rename** to change an item's title.
- Right click on a profile and select **Recognize Titles from Profile** to update cached game information. More accurate than covers.jqe360.com but significantly slower.
- Network shares are not supported. Map a network drive first if you want to connect to a NAS.
- You can use Total Commander hotkeys in GODspeed: F keys, Alt+F1/F2 for drive change, Space and Ctrl+L for space calculation, etc.

</details>
