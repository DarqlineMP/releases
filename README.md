# DarqlineMP releases

Official downloads of DarqlineMP, a free, non-commercial multiplayer platform for
Grand Theft Auto: San Andreas – The Definitive Edition on Windows.

> **Closed test.** DarqlineMP is in a closed test. Anyone can download it, but the test servers are open by
> invitation only. The public alpha comes later.

## Install

1. Open the newest **Launcher** release and download `DarqlineMP_<version>_x64-setup.exe`.
2. Run it. It installs for your Windows user only, in `%LOCALAPPDATA%\DarqlineMP`, and doesn't ask for administrator
   rights.
3. Start DarqlineMP. On first start it shows the client license, downloads the DarqlineMP client, finds the game and
   asks for a nickname.

You need Windows 10 or 11 and your own legal copy of the game. The Steam copy is supported. DarqlineMP doesn't distribute
or change any game files.

From then on, the launcher updates itself and the client. You never need to download anything from this page again.

## “Windows protected your PC”

DarqlineMP is not Authenticode-signed yet, so Windows may show a SmartScreen warning the first time you run the
installer. Before continuing, check the installer as described below. Then choose **More info → Run anyway**.

Updates are downloaded and checked by the launcher itself and don't show this warning.

## Check a download

Every release lists the SHA-256 of its files in `SHA256SUMS`. In PowerShell:

```powershell
Get-FileHash .\DarqlineMP_<version>_x64-setup.exe -Algorithm SHA256
```

The hash must match the line in `SHA256SUMS`.

Everything DarqlineMP publishes is also signed with the project's [minisign](https://jedisct1.github.io/minisign/) key:

```
RWRqpLwd08q7pLgX9ahLFW6lhFohMXCfzLAgo23LJ75qTaforf2W1U6b
```

To check the installer with its signature:

```
minisign -Vm DarqlineMP_<version>_x64-setup.exe -P RWRqpLwd08q7pLgX9ahLFW6lhFohMXCfzLAgo23LJ75qTaforf2W1U6b
```

The launcher checks the same key before it installs any client or launcher update, and refuses anything else.

## What the releases contain

| Release | Contents |
|---|---|
| `launcher-v<version>` | The installer, its `.minisig` signature and `SHA256SUMS` |
| `client-v<version>` | The client files, each named by its SHA-256. The launcher downloads them; you don't need to |

## What DarqlineMP does and doesn't do

- It loads the DarqlineMP client into the game when you start it from the launcher. It never changes game files.
- It installs no drivers, services or startup entries. Crash reports stay on your computer and are never sent
  automatically.
- The launcher connects to DarqlineMP services, GitHub to download release files, and the servers you join. What
  this processes is listed in the [Privacy Notice](https://darqline.com/privacy/).

## Only official sources

Download DarqlineMP only from this page or from links on [darqline.com](https://darqline.com/). Repackaged or unofficial builds aren't
supported, aren't allowed by the client license, and may be malware.

## Antivirus warnings

A launcher that loads a library into a game can look suspicious to antivirus software, especially when it isn't
signed. Builds are sent to Microsoft for false-positive analysis before release. If your antivirus quarantines a
DarqlineMP file:

1. Check the file's SHA-256 against `SHA256SUMS`.
2. [Open an antivirus issue](https://github.com/DarqlineMP/releases/issues/new?template=antivirus.yml) with the hash and
   the name of the detection.

Please don't turn your antivirus off. Add an exclusion for the DarqlineMP folder only as a last resort, after
checking the hash.

## Report a problem

[Open an issue](https://github.com/DarqlineMP/releases/issues/new/choose). The form asks for what we need.
Questions and ideas go to [Discussions](https://github.com/DarqlineMP/releases/discussions).

Report security issues privately to `security@darqline.com`, not in public issues.

## Licenses

- The launcher is licensed under MPL-2.0. Its source code will be published with the public alpha.
- The client is closed source under the DarqlineMP Client License. The launcher shows the license before installing,
  and each client release includes it.
- Third-party components keep their own licenses, listed in the notices shipped with each release.

---

DarqlineMP is an independent, non-commercial project. It is not affiliated with, endorsed or sponsored by Rockstar
Games or Take-Two Interactive. Grand Theft Auto and Grand Theft Auto: San Andreas are trademarks of Take-Two
Interactive Software, Inc. You need your own legal copy of the game to use DarqlineMP.
