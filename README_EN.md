# Qtalis NavLink

[Chinese](README.md) | [English](README_EN.md)

**GNSS receiver communication, monitoring, evaluation, and correction-data tool for Windows.**

[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-1473E6)](https://www.microsoft.com/windows)
[![Version](https://img.shields.io/badge/version-1.2.1-0E7888)](https://github.com/chengjinquan1210-hash/Qtalis_Navlink/releases)
[![Website](https://img.shields.io/badge/Qtalis-Official%20Website-16835B)](https://www.qtalisgnss.com/)

Qtalis NavLink is a Windows desktop application for GNSS receiver communication, raw-data capture, satellite signal monitoring, positioning evaluation, NTRIP correction services, RINEX conversion, and observation-quality analysis.

## Download

Download the latest Windows x64 ZIP package from the repository's [Releases](https://github.com/chengjinquan1210-hash/Qtalis_Navlink/releases) page.

1. Download `QtalisNavLink-vX.Y.Z-win-x64.zip`.
2. Extract the complete ZIP package to a writable directory.
3. Run `QtalisNavLink.exe`.
4. Do not copy the EXE by itself. Keep all required DLLs and the `Updater` and `Tools` directories together with the executable.

> Windows may display a SmartScreen warning for an unsigned build. Verify that the package was downloaded from this repository before running it.

## Features

### Data Terminal

- Connect up to two independent devices through serial ports or TCP.
- Send and receive ASCII or HEX data with timestamps, auto-scroll, and timed transmission.
- Configure common commands, standard NMEA messages, and SinoGNSS custom logs from quick menus.
- Capture high-rate raw data while monitoring write queues, serial errors, and capture integrity.
- Pause protocol parsing while saving to prioritize lossless high-rate binary capture.

### Satellite Signals and Positioning

- Supports GPS, BDS, GLONASS, Galileo, QZSS, SBAS, and NavIC.
- Parses NMEA, ComNav M925, Unicore SATSINFOB, and u-blox raw satellite information.
- Displays multi-frequency C/N0 charts, a complete frequency table, and a sky plot.
- Provides online maps through AMap and OpenStreetMap.
- Parses BESTPOS, GPGGA, GPVTG, HEADINGA, and HEADING2A messages.

### Position Evaluation

- Displays ENU position scatter, error time series, and heading visualization.
- Supports dual-device comparison, configurable assessment thresholds, and result export.
- Exports HTML reports containing result tables, horizontal scatter plots, and error charts.

### Correction Service

- Includes an NTRIP client that can monitor and save RTCM without a connected receiver.
- Fetches mountpoints and supports manual-coordinate VRS GGA and dual-device RTCM forwarding.
- Decodes RTCM message types in real time and reports CRC integrity, per-second coverage, and reception completeness.
- Saves, renames, and deletes reusable NTRIP profiles.

### RINEX and Log Tools

- Records and plays back logs with speed control and raw-data export.
- Integrates RINEX conversion tools.
- Reports observation period, sample rate, epoch completeness, cycle-slip events, MP1/MP2 RMS, and C/N0 statistics by constellation.
- Displays multi-frequency C/N0 time series for individual satellites.

### Additional Tools

- Switches between Chinese and English interfaces.
- Includes common operating modes, radio configuration, and an OEM command reference.
- Provides documentation, firmware, product, and official support resource directories.
- Supports GitHub-based OTA updates.

## Quick Start

1. Connect a GNSS device and confirm that Windows recognizes its serial port, or obtain the device's TCP address.
2. Open **Terminal**, select the port and baud rate, and click **Connect Device 1**.
3. Monitor receiver output or use the quick-command controls to configure receiver messages.
4. Open **Satellite Signals** to inspect multi-constellation, multi-frequency C/N0 data and the sky plot.
5. Open **Position** or **Position Evaluation** to monitor real-time position and accuracy.
6. Open **Correction Service** to connect to an NTRIP caster and select an RTCM forwarding target.

For detailed instructions, see the [Qtalis NavLink Operation Manual](docs/Qtalis_NavLink_操作手册_v1.0.7.md).

## OTA Updates

Qtalis NavLink silently checks for updates after startup and checks again every six hours while running. When a new version is available, the user can approve the download and installation process:

1. Download the GitHub Release ZIP package.
2. Verify its SHA-256 checksum.
3. Close the main application and let the standalone updater replace the installed files.
4. Restore the previous files if the update fails.
5. Restart the application automatically after a successful update.

The update process does not modify saved GNSS logs, RINEX files, or exported reports.

## System Requirements

- Windows 10 or Windows 11, x64
- Recommended display resolution: 1366 x 768 or higher
- Correct USB or serial drivers for connected receiver hardware
- Network access for online maps, NTRIP, documentation links, and software updates
- .NET 8 Desktop Runtime for the current lightweight distribution

## Release Maintenance

To publish a new version:

1. Generate the complete Windows x64 publish directory.
2. Compress the directory contents as `QtalisNavLink-vX.Y.Z-win-x64.zip`. The ZIP root must contain `QtalisNavLink.exe`.
3. Create a matching Git tag and GitHub Release, then upload the ZIP package.
4. Calculate the ZIP package's SHA-256 checksum.
5. Update the repository-root `update.json` with the version, direct Release download URL, checksum, and release notes.
6. Confirm that the Release asset is publicly downloadable before publishing the manifest.

See [update-manifest.example.json](docs/update-manifest.example.json) for the manifest format and the [OTA Release Guide](docs/Qtalis_NavLink_OTA发布说明.md) for the complete workflow.

## Support and Resources

- [Qtalis Official Website](https://www.qtalisgnss.com/)
- [Qtalis Resource Hub](https://www.qtalisgnss.com/pages/resource-hub)
- [Qtalis Forum](https://www.qtalisgnss.com/community/forum)
- [GitHub Issues](https://github.com/chengjinquan1210-hash/Qtalis_Navlink/issues)

## Notice

Qtalis NavLink is intended for GNSS receiver integration, testing, monitoring, and engineering evaluation. Verify receiver commands, firmware compatibility, radio parameters, and correction-service credentials before use in production environments.

Copyright (c) Qtalis. All rights reserved.
