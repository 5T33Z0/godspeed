# Changelog

## [2026-05-15] v1.4

- ADDED: Inno Setup installer for Windows 10/11 (64-bit)
- ADDED: Portable `.zip` release
- ADDED: `BUILD.md` guide for building from source
- ADDED: Relative paths in installer script for portability across systems
- REMOVED: Auto-updater and related tooling (no longer functional)
- REMOVED: Bundled .NET 4.0 installer (unnecessary on modern Windows)

## [2024-03-14] v1.3

- ADDED: Russian (ru-RU) language (partial)
- ADDED: SharpCompress library for improved archive support
- ADDED: Human-readable file sizes on the panel
- ADDED: Open file panel in FTP
- FIXED: Xbox Unity title recognizer
- FIXED: SizeConverter display and translation
- FIXED: Search URL for Google
- FIXED: Null pointer exception
- FIXED: File size display on replace dialog
- FIXED: Drive handling after USB device removal
- REMOVED: Hungarian (hu-HU) language resource
- REMOVED: x86 build target (x64 only)
- REMOVED: WIX installer (replaced with Inno Setup)

## [Unreleased] v1.2

- ADDED: DashLaunch FTPdll plugin support (ftpdll.xex)
- ADDED: Large icons view
- ADDED: Title/Name column mode switch (Ctrl+Click on the Title/Name column)
- ADDED: Title bar to the context menu (Open with Explorer action for local contents)
- ADDED: File operation options to the context menu
- ADDED: View and sorting options to the context menu
- ADDED: FATX file name and path limitations awareness
- ADDED: "Overwrite all older" has been replaced with "Overwrite all smaller"
- ADDED: Write error dialog refactor
- ADDED: Renaming a file now supports overwrite
- ADDED: Favorite folders
- ADDED: UI improvements
- ADDED: System default icons for well-known extensions
- ADDED: Recognize game demos
- ADDED: Signed in profiles can be recognized using F3Plugin WebUI (supported by F3 and Aurora)
- ADDED: Ctrl+R (Refresh) refactor — now refreshes cached contents too
- ADDED: ISO to GOD conversion (partial rebuild not available yet)
- ADDED: Auto updater for quick hotfixes
- FIXED: Active pane behavior refactor
- FIXED: Transfer timer and speedometer refactor
- FIXED: name.txt content validation and text overflow
- FIXED: More fail-safe compressed file support (password protected archives not supported)
- FIXED: Navigation into AvatarAssets folder within a profile package
- FIXED: File existence check cache to speed up transfer
- FIXED: File date issues in F3
- FIXED Issue #509: Null reference exception in FTP CloseDataStream
- FIXED Issue #512: Directory listing refactor to support folders with large number of files
- FIXED Issue #513: Null reference exception in TransferManagerViewModel.ProcessError
- FIXED Issue #516: Null file item name property in ExecuteChangeDirectoryCommand
- FIXED Issue #538: Null reference exception in GetCorrespondingScanFolder
- FIXED Issue #562: File does not exist in the package: Account
- FIXED Issue #585: Error getting StorageInfo in Aurora 0.1a
- FIXED Issue #606: Handle HTTP GET errors
- FIXED Issue #611: Error when pressing Pause button during delete
- FIXED Issue #727: Collection was modified; Main window was hit test visible during population
- REMOVED: Facebook and Codeplex notifications

## [2014-09-04] v1.1

- ADDED: DashLaunch FTP (DLiFTPD) support
- ADDED: XeXMenu and DashLaunch FTP cannot be accessed in PASV anymore
- ADDED: Better support of reparse points
- ADDED: Completely rewritten copy mechanism
- ADDED: Completely rewritten caching mechanism
- ADDED: FTP stream handling refactor
- ADDED: Aurora support
- ADDED: FSD/F3 Content Scan Trigger
- ADDED: File hash verification after upload/download
- ADDED: Launch games via HTTP
- ADDED: Launch .xex file via FTP
- ADDED: FSD Database Checker and Clean up
- ADDED: Shutdown PC and/or Xbox after transfer completed
- ADDED: Displaying version number of Title Updates
- ADDED: FTP Log Viewer
- ADDED: Hungarian language
- ADDED: New About window
- ADDED: Grid splitter presets
- FIXED Issue #61: Null reference when showing non-closable notification message
- FIXED Issue #135: DialogResult can be set only after Window is created and shown as dialog
- FIXED Issue #168: Application crashes if item cannot be deleted
- FIXED Issue #171: Uploading and empty folder browsing with XeXMenu
- FIXED Issue #173: Do not let multiple instances to run
- FIXED Issue #177: Throwing the cache of a non-cached item
- FIXED Issue #181: Application crashes if parent folder doesn't exist anymore but I call an UpDirectory
- FIXED Issue #182: Application crashes if folder cannot be renamed
- FIXED Issue #187: Application crashes if reparse points cannot be accessed
- FIXED Issue #220: Handle errors on the right thread during changing directory
- FIXED Issue #237: STFS DateTime parsing
- FIXED Issue #244: Special characters in FTP item names
- FIXED Issue #267: No application is associated with URLs
- FIXED Issue #283: Handle permission denied errors on FTP
- FIXED: Black Window on Windows 7 Aero theme
- FIXED: Misbehaving .. folder on local file system
- FIXED: Stored participation answer isn't displayed if I open the User Participation Window again
- FIXED: Editing connection highlight name as an already existing one
- FIXED: Drive selector combobox shows wrong drive letter after unsuccessful drive change
- FIXED: Can't open profile by right clicking on its profile
- FIXED: Can't interact with a profile if the cache was just erased before
- FIXED: Trimming of long connection names
- FIXED: Cannot abort second transfer if the first one was aborted too
- FIXED: Title recognition after rename
- FIXED: Folder creation within Xbox folder structure
- FIXED: Folder name validation
- FIXED: Skip All doesn't remember decision
- FIXED: Move deletes skipped files

## [2014-03-24] v1.0 RC3

- FIXED: File existence check on FTP

## [2014-03-21] v1.0 RC2

- ADDED: New FTP client library (based on the work of J.P. Trosclair, https://netftp.codeplex.com/), removing dependency on Limilabs' Ftp.dll
- ADDED: User Notification Service
- ADDED: Sanity checker — checks dependencies, migrates cached data from old versions
- ADDED: User Statistics
- ADDED: Partial recognition notification
- ADDED: New version detection
- ADDED: Full FSD 1.x (MinFTPD) support
- ADDED: Pause/Continue buttons in the Windows 7 taskbar thumbnail
- ADDED: Select drive in dropdown by initial letter key press
- ADDED: Shows "?" in Size column while calculating
- ADDED: Size calculation can now be aborted by pressing Esc or changing directory
- FIXED Issue #9: Polish month abbreviations in LIST results
- FIXED Issue #18: "No error" exception when calling GetDrives()
- FIXED Issue #28: Null reference exception after DeleteError
- FIXED Issue #33: Folder creation on a device with no space left throws no exception
- FIXED Issue #35: Null reference exception in FtpConnectError
- FIXED Issue #36: Null reference exception during the disposal of a non-connected FTP ViewModel
- FIXED Issue #40: Copying a grid row to clipboard
- FIXED Issue #44: Lost connection can screw up directory navigation
- FIXED Issue #45: .NET version checker doesn't do its thing
- FIXED Issue #48: Null reference exception after CopyError
- FIXED Issue #62: Can't connect back to an FTP where the last visited folder doesn't exist anymore
- FIXED Issue #63: Remove server has not initiated the connection exception
- FIXED Issue #64: Null reference exception in FTP file renaming
- FIXED Issue #84: Null reference exception during Title Recognition
- FIXED: Recognize standalone SVOD packages
- FIXED: Clear Cache UI freeze
- FIXED: PASV usage
- FIXED: UTF-8 error reporting
- FIXED: Special characters in path screws up Remote Copy
- FIXED: Recognition can freeze if an unexpected error happens
- FIXED: Remember last used sort order
- FIXED: Close FTP pane if connection cannot be reestablished or user decides to do so
- FIXED: Progress indication fix in case of skipping/retrying partially transferred files
- FIXED: Access of read-only files
- FIXED: Something went wrong exception doesn't have a stack trace

## [2014-02-08] v1.0 RC1

- ADDED: Indicate inaccessible files
- ADDED: Indicate inaccessible profiles
- ADDED: Cache item won't be invalidated if refreshing fails
- ADDED: Invalid items won't be cached anymore
- ADDED: Sending screenshot attached to error reporting
- FIXED Issue #4: Handle connection callback errors
- FIXED Issue #10: Connection name existence check
- FIXED Issue #12: Handle lost connection when calling up directory
- FIXED Issue #24: Null reference exception in FTP connection error callback

## [2014-01-27] v1.0 Beta 4

- ADDED: Compressed file support (Zip, Rar, Tar, GZip, 7Zip)
- ADDED: Invert Selection (Num *)
- ADDED: Quick Search
- ADDED: File/Directory rename
- ADDED: .NET version detection (Quick Search and Renaming requires .NET 4.0.30319.18408 or newer)
- ADDED: XeXMenu support
- ADDED: Active mode enabled and became default for FTPs (Passive Mode still available)
- ADDED: Warning messages can be ignored with "Don't show this message again" checkbox
- ADDED: NTFS Junction Point support
- ADDED: File transfer notification during Indirect Copy
- ADDED: Clear Cache command
- ADDED: Navigate to parent folder and closing nested pane by pressing Backspace
- ADDED: PS3 Free space indication
- ADDED: Removable device support
- ADDED: Error reporting of unhandled exceptions
- FIXED: Title caching (directory change speed up 500–1000%)
- FIXED: Displaying wrong folder size before copy
- FIXED: Profile detection error
- FIXED: Last visited path per connection
- FIXED: New version detection
- FIXED: Executing the Rename command from context menu
- FIXED: Title recognition in STFS packages
- FIXED: STFS package saving
- FIXED: Refreshing directory shows random percentage
- FIXED: Speedmeter using Remote Copy
- FIXED: Remote Copying files with "&" in path
- FIXED: PS3 contents aren't treated as Xbox anymore

## [2013-11-15] v1.0 Beta 3

- ADDED: Progress indication in taskbar
- ADDED: Recognition progress indication
- ADDED: Elapsed time indication, remaining time calculation
- ADDED: Transfer speed calculation
- ADDED: Local to local progress indication
- ADDED: Local to local file transfer abortion
- ADDED: Pause & Resume file transfer
- ADDED: Context-aware "New folder" dropdown
- ADDED: Save and restore locations and sort settings
- ADDED: User settings
- ADDED: Custom Window Chrome can now be disabled
- ADDED: Remote Copy support between NAS and FTP (Telnet and LFTP required)
- ADDED: Delete existing connection
- ADDED: Anonymous login
- ADDED: Minor PS3 FTP support
- FIXED: Upload to FTP (was malfunctioning with FSD 2.2)
- FIXED: FTP upload error handling
- FIXED: FTP download progress indication
- FIXED: UI freeze caused by FTP download
- FIXED: Displaying selection size after queue population
- FIXED: Main window is not hit test visible during transfer
- FIXED: Free space update
- FIXED: Slim E icon was missing

## [2013-10-23] v1.0 Beta 2

- ADDED: Open command in profile item's context menu to ease STFS access
- ADDED: Version checker
- FIXED: Keyvault resources were missing from Core
- FIXED: Move command now works properly
- FIXED: File existence detection during FTP download
- Slight performance tweak
- Minor UI related bugfixes

## [2013-10-21] v1.0 Beta 1

Initial public release.
