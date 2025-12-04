# 🧰 Flutter Toolkit

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Bash](https://img.shields.io/badge/Language-Bash-4EAA25?logo=gnu-bash&logoColor=white)](https://www.gnu.org/software/bash/)
[![Flutter](https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=white)](https://flutter.dev/)

> **A powerful, lightweight CLI assistant to automate your Flutter development workflow.**

`flutter_toolkit` is a robust Bash script designed to save you time by automating repetitive tasks like cleaning builds, generating code, managing dependencies, and preparing releases. It provides a simple, interactive menu to handle everything from "nuclear" project refreshes to precise build operations.

---

## ✨ Features

### 🔍 Project Health & Maintenance
- **🚑 Analyze & Fix**: One-step formatting, dart fix, and analysis.
- **🧹 Deep Clean**: Recursively removes build artifacts (`.dart_tool`, `build`, `pubspec.lock`) and runs `flutter clean`.
- **🗑️ Repair Pub Cache**: Fixes corrupted cache issues.
- **⬆️ Upgrade Dependencies**: Safely upgrades your packages.
- **🔎 Check Outdated**: Quickly spot packages that need updates.

### 🏗️ Code Generation
- **🏭 Run Build Runner**: Runs `build_runner` with `--delete-conflicting-outputs`.
- **👀 Watch Build Runner**: Starts `build_runner` in watch mode for auto-updates.
- **🌍 Generate Translations**: specialized support for `slang` translations.

### 🤖 Android Tasks
- **🐘 Gradle Clean**: Deep clean for the Android module.
- **🏗️ Assemble Release**: Builds the release APK via Gradle.
- **📦 Build Split APKs**: Generates optimized APKs per ABI.
- **🚀 Build Flavor**: Interactive flavor build support.

### 🍎 iOS Tasks
- **📥 Pod Install / Update**: Manages CocoaPods dependencies.
- **🧼 Pod Clean & Reinstall**: The "magic fix" for iOS build errors (deletes Pods/Lockfile and reinstalls).
- **📦 Build IPA**: Creates an iOS archive for distribution.

### 🚀 Release & Utilities
- **🆙 Bump Version**: Interactive version bumping (Major, Minor, Patch, Build) using `cider`.
- **🔄 Full Project Refresh**: The "Nuclear Option" – performs a complete teardown and rebuild of the project to fix persistent weird issues.
- **🧪 Run Tests**: Executes your test suite.
- **🩺 Flutter Doctor**: Checks your environment.
- **❓ Help**: Shows all available CLI options.

---

## 🚀 Getting Started

### Prerequisites
- **Flutter SDK** installed and in your PATH.
- **Bash** (Standard on macOS/Linux).
- **Cider** (Optional, for version bumping): `dart pub global activate cider`
- **Slang** (Optional, for translations): `dart pub add slang`

### Installation

1.  **Copy the script** to your project root:
    ```bash
    cp /path/to/flutter_toolkit.sh .
    ```
2.  **Make it executable**:
    ```bash
    chmod +x flutter_toolkit.sh
    ```

---

## 📖 Usage

Simply run the script from your terminal:

```bash
./flutter_toolkit.sh
```

You will be greeted by an interactive menu:

```text
🔍 PROJECT HEALTH & MAINTENANCE
  1) 🚑 Analyze & Fix (Format, Fix, Analyze)
  2) 🧹 Deep Clean Project (Delete build artifacts)
  ...
```

Enter the number corresponding to the task you want to perform.

### CLI Mode

You can also run tasks directly from the command line without the interactive menu:

```bash
./flutter_toolkit.sh --clean         # Deep clean project
./flutter_toolkit.sh --analyze        # Run analysis and fix
./flutter_toolkit.sh --build-runner   # Run build_runner
./flutter_toolkit.sh --pod-install    # Install iOS Pods
./flutter_toolkit.sh --help           # Show all available options
```

**All available flags:**
| Flag | Description |
|------|-------------|
| `--analyze` | Run analysis and fix |
| `--clean` | Deep clean project |
| `--pub-repair` | Repair pub cache |
| `--upgrade` | Upgrade dependencies |
| `--build-runner` | Run build_runner |
| `--watch` | Watch build_runner |
| `--slang` | Generate translations |
| `--gradle-clean` | Clean Gradle |
| `--assemble` | Assemble Release APK |
| `--pod-install` | Install Pods |
| `--pod-update` | Update Pods |
| `--test` | Run tests |
| `--doctor` | Run Flutter Doctor |
| `--help` | Show help message |

> **Note:** The script automatically validates that you're running it from a Flutter project root (checks for `pubspec.yaml`). Platform-specific tasks also verify that the required directories (`android/` or `ios/`) exist.

---

## 🤝 Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

Please read our [Contributing Guidelines](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests.

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

---

<div align="center">
  <sub>Built with ❤️ for the Flutter Community</sub>
</div>
