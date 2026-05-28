# Building GODspeed from Source

## Prerequisites

- Windows 10 or 11 (64-bit)
- [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-8.0.421-windows-x64-installer) - required for NuGet package restore to work
- [Visual Studio Build Tools 2022](https://visualstudio.microsoft.com/downloads/) — scroll down to "Tools for Visual Studio", select the **.NET desktop build tools** workload during install
- [Inno Setup 6](https://jrsoftware.org/isinfo.php) — only needed if you want to build the installer

## 1. Clone the repository

```cmd
git clone https://github.com/YourFork/godspeed.git
cd godspeed
```

## 2. Download NuGet

```cmd
curl -o nuget.exe https://dist.nuget.org/win-x86-commandline/latest/nuget.exe
```

## 3. Restore NuGet packages

```cmd
nuget.exe restore Neurotoxin.Godspeed\Neurotoxin.Godspeed.sln
```

## 4. Build

Open a **Visual Studio Developer Command Prompt** and run:

```cmd
msbuild Neurotoxin.Godspeed\Neurotoxin.Godspeed.sln /p:Configuration=Release
```

The compiled output will be in:

```
Neurotoxin.Godspeed\Neurotoxin.Godspeed.Shell\bin\Release\
```

You can run `Neurotoxin.Godspeed.Shell.exe` directly from there — no installation needed.

## 5. Build the installer (optional)

1. Open `Install\GODspeed_Setup.iss` in Inno Setup
2. Click **Build → Compile**
3. The installer will be output to the `output\` folder in the repo root

## Notes

- The `x86\` and `x64\` subfolders inside `bin\Release\` contain native C++ helper DLLs — don't delete them
- The app targets x64 — the installer installs to `Program Files` (not `Program Files (x86)`)
- .NET 4.0 or newer is required at runtime, which is already present on any modern Windows installation
