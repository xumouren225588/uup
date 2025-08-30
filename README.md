# About (OUTDATED)

This creates an iso file with the latest Windows available from the [Unified Update Platform (UUP)](https://docs.microsoft.com/en-us/windows/deployment/update/windows-update-overview).

This shrink wraps the [UUP dump](https://git.uupdump.net/uup-dump) project into a single command.

This can be executed in a Windows x64 or arm64 host (min. 21H2).

This supports the following Windows Builds:

* `windows-10`: Windows 10 19045 (aka 22H2)
* `windows-11old`: Windows 11 22631 (aka 23H2)
* `windows-11`: Windows 11 26100 (aka 24H2)
* `windows-11beta`: Windows 11 26120 (aka 24H2 BETA)
* `windows-11new`: Windows 11 26200 (aka 25H2)
* `windows-11dev`: Windows 11 26220 (aka 25H2 DEV)
* `windows-11canary`: Windows 11 Insider Preview (aka CANARY)

## Usage

Get the latest Windows Server 2022 iso:

```bash
powershell uup-dump-get-windows-iso.ps1 windows-2022
```

When everything works correctly, you'll have the iso in the `output` directory at, e.g., `output/windows-2022.iso`.

## Tags structure

```text
  .------------------------------- OS Build
  |    .-------------------------- System Revision
  |    |    .--------------------- Release Channel/Version
  |    |    |    .---------------- System Edition
  |    |    |    |   .------------ CPU architecture
  |    |    |    |   |  .--------- Language
  |    |    |    |   |  |  .------ Image is compressed by ESD
  |    |    |    |   |  |  | .---- Additional drivers is included
  |    |    |    |   |  |  | | .-- .NET Framework 3.5 is included
__|__ _|__ _|__ _|_ _|_ |_ | | |
26100.4946.24H2.PRO.X64.PL.E.D.N
```

## Related Tools

* [Rufus](https://github.com/pbatard/rufus)
* [Fido](https://github.com/pbatard/Fido)
* [windows-evaluation-isos-scraper](https://github.com/rgl/windows-evaluation-isos-scraper)

## Reference

* [UUP dump home](https://uupdump.net)
* [UUP dump source code](https://git.uupdump.net/uup-dump)
* [Unified Update Platform (UUP)](https://docs.microsoft.com/en-us/windows/deployment/update/windows-update-overview)
