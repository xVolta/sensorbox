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

## [0.5.1] - 2025-08-16
### Fixed
- Adjusted PM sensor configuration to allow long-term data tracking.

## [0.5.0] - 2025-08-16
### NOTICE
- Any existing device configuration files will need to be edited when upgrading to this version!
  - sensorbox/globals.yaml has been removed, and will need to be removed from your per device config.
  - sensorbox/controls.yaml has been added, and will need to be added as an include in your per device config.
### Added
- Control to select on-device temperature display units.
### Changed
- Sensor code refactored to use lvgl calls to set display colors
- Display code refactored for better maintainability
- Proper handling of sensor display for devices without all sensor types.
- Top button now increases display brightness 20% per push, up to 100%, then resets to 0% (off).
### Removed
- Global variables
- Hacky display workarounds using text sensors.
### Fixed
- No longer displays placeholder sensor fields and categories before sensor data is available.

## [0.4.1] - 2025-08-15
### Fixed
- Hide display fields for missing sensor data (not present, not reporting, etc.)

## [0.4.0] - 2025-08-14
### Added
- Temperature now also exposed to HA in Freedom Units.
### Changed
- Tweaks for better integration with Home Assistant dashboards.
  - Expose backlight as a control instead of a light.
  - Expose temperature and humidity offsets as configuration entities instead of control entities.
  - Expose best available sensor data for Temperature, Humidity, Pressure, CO2, PM, VOC, and CH2O to HA, using the same logic used for on-device LVGL display.
  - Individual sensor data disabled by default to avoid polluting HA dashboards.

## [0.3.1] - 2025-02-24
### Fixed
- Adjusted hardware.yaml for breaking changes in ESPHome 2025.2.0

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
