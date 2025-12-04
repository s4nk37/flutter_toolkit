# Changelog

All notable changes to this project will be documented in this file.

## [3.0.0] - 2025-12-04

### Added
- **CLI Argument Support**: You can now run tasks directly using flags (e.g., `--clean`, `--analyze`, `--pod-install`).
- **Project Validation**: The script now verifies it is running in a valid Flutter project root (checks for `pubspec.yaml`).
- **Platform Checks**: Android and iOS tasks now check for the existence of `android/` and `ios/` directories before execution.
- **Help Command**: Added `--help` flag to list all available commands.

### Changed
- Improved error handling for missing directories.
- Refactored main loop to support both interactive and non-interactive modes.

## [2.0.0] - Previous Version
- Interactive menu system.
- Basic Flutter and Dart commands.
