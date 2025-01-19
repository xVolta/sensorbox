# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased] - TBD
### Added
- Touchscreen support for ILI9341 with XPT2046 touch controller
- Human Presence Detection support for HLK-LD2402
- Screen for Thermostat/Heatpump controls
- Screen for Lighting controls
### Changed
### Deprecated
### Removed
### Fixed
### Security

## [0.3.0] - 2025-01-20 [Initial GitHub Release]
### Added
- Support for adjustable temperature offset, as suggested by [@Gerald_71276](https://www.printables.com/make/2288220) and [@DesasterMan](https://www.printables.com/make/2347551?comment_id=2347551).

## [0.2.0] - 2025-01-19
### Added
- Support for SEN5x series sensors.
### Changed
- Added display field for PM4.0
- Display code prefers data from SEN5x sensors when available.

## [0.1.2] - 2025-01-05
### Changed
- Lowered logger level to INFO to reduce burden on ESP
- Disabled ESP web server which was causing Wi-Fi disconnects
### Fixed
- Fixed occassional Wi-Fi disconnects

## [0.1.1] - 2025-01-03
### Added
- Included MaterialDesign-Webfont for users that don't already have it installed.

## [0.1.0] - 2025-01-01
### Added
- Initial Release of rewritten code using LVGL for display, optimized for readability and maintainability.
