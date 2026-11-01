## About this fork

This is a fork of [ryochack/UsbipdWinGui](https://github.com/ryochack/UsbipdWinGui),
a system-tray GUI for managing USB devices with
[usbipd-win](https://github.com/dorssel/usbipd-win) (bind, attach, detach).

### What's changed
- The Setup project (`Setup/Setup.vdproj`) is switched from Japanese to
  English (US), including the dialog names and the .NET Desktop Runtime
  prerequisite labels.
- Added `installer-wix/` and `build-msi.ps1`, an alternative way to build the MSI
  with WiX and the .NET 8 SDK, without Visual Studio.
- Added `UsbipdGui/Properties/PublishProfiles/FolderProfile.pubxml`, which the
  Setup project needs in order to build.
- The application source and behavior are unchanged.

### Building the MSI
**Visual Studio 2022:** install the *Microsoft Visual Studio Installer Projects*
extension and the .NET desktop development workload. Set the configuration to
**Release**, rebuild `UsbipdGui`, then rebuild `Setup`. The MSI is at
[Setup/Release/UsbipdGui-v1.0.1-Setup.msi](https://github.com/sudiptatalgaon/UsbipdWinGui-English/blob/main/Setup/Release/UsbipdGui-v1.0.1-Setup.msi).

**Command line:** run `build-msi.ps1` with the .NET 8 SDK installed.

### Requirements
Windows, [.NET 8 Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/8.0)
and usbipd-win.

### Credits and license
All credit for the application goes to the original author, ryochack.
This fork keeps the original license; see `LICENSE`.
