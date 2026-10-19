# Expressivegram

**Telegram Desktop, reimagined with Material 3 Expressive.**

Expressivegram is an unofficial community fork of [Telegram Desktop](https://github.com/telegramdesktop/tdesktop) exploring a more expressive desktop messaging experience inspired by Google's [Material 3 design system](https://m3.material.io/).

The goal is to bring expressive shapes, a coherent color system, clearer visual hierarchy, and carefully designed interaction states to Telegram Desktop while preserving its messaging functionality.

> [!NOTE]
> Expressivegram is an unofficial third-party project. It is not affiliated with, endorsed by, or sponsored by Telegram or Google.

[![Linux CI](https://github.com/timched/Expressivegram-Desktop/actions/workflows/build-linux.yml/badge.svg?branch=dev)](https://github.com/timched/Expressivegram-Desktop/actions/workflows/build-linux.yml)
[![Windows CI](https://github.com/timched/Expressivegram-Desktop/actions/workflows/build-windows.yml/badge.svg?branch=dev)](https://github.com/timched/Expressivegram-Desktop/actions/workflows/build-windows.yml)
[![macOS CI](https://github.com/timched/Expressivegram-Desktop/actions/workflows/build-macos.yml/badge.svg?branch=dev)](https://github.com/timched/Expressivegram-Desktop/actions/workflows/build-macos.yml)
[![Upstream Telegram Desktop](https://img.shields.io/badge/based%20on-Telegram%20Desktop-26A5E4)](https://github.com/telegramdesktop/tdesktop)
[![License](https://img.shields.io/badge/license-GPL--3.0%20with%20OpenSSL%20exception-blue)](LICENSE)

## Project status

**Work in progress.** Expressivegram is based on the Telegram Desktop C++/Qt codebase. The Material 3 Expressive redesign is being developed incrementally; not every screen or component has been redesigned yet.

## Design goals

- **Material 3 Expressive** — intentional shape, color, typography, and motion rather than a simple recolor.
- **Consistent components** — shared visual language for navigation, buttons, menus, dialogs, settings, and chat surfaces.
- **Desktop-first usability** — expressive styling without sacrificing keyboard navigation, density, or familiar desktop behavior.
- **Theme support** — coordinated light and dark palettes, with room for user customization.
- **Preserve Telegram functionality** — keep messaging and platform features working as the interface evolves.

## Building

The project uses the upstream Telegram Desktop build system and its Git submodules. Start with the [Linux build instructions](docs/building-linux.md), [Windows build instructions](docs/building-win.md), or [macOS build instructions](docs/building-mac.md).

Clone the repository and its submodules:

```bash
git clone --recursive https://github.com/timched/Expressivegram-Desktop.git
cd Expressivegram-Desktop
```

For a Linux build, prepare the upstream build environment:

```bash
Telegram/build/prepare/linux.sh
```

Then follow the platform-specific build guide. The build may require your own Telegram API credentials; see the relevant documentation and the [upstream build guide](https://github.com/telegramdesktop/tdesktop/blob/dev/docs/building-linux.md).

## GitHub Actions

The workflows run on pushes to `dev`, pull requests targeting `dev`, and manual dispatches:

- **Linux** — prepares the upstream build container, compiles the application, and uploads the executable as a workflow artifact.
- **Windows x64** — prepares third-party libraries, configures CMake, compiles the application, and uploads the executable and optional updater.
- **macOS** — prepares dependencies, builds the application bundle, and uploads a ZIP artifact.

Builds can take a while because Telegram Desktop has many dependencies. Workflow artifacts are temporary CI outputs, not official signed releases.

## License

Expressivegram is based on [Telegram Desktop](https://github.com/telegramdesktop/tdesktop). The upstream project is licensed under GPLv3 with an OpenSSL exception. See [LICENSE](LICENSE), [LEGAL](LEGAL), and the applicable third-party license notices for the exact terms.

## Credits

- [Telegram Desktop](https://github.com/telegramdesktop/tdesktop) — upstream application and codebase.
- [Telegram API](https://core.telegram.org/) — platform documentation.
- [Material Design](https://m3.material.io/) — design inspiration.

Expressivegram is an independent community project; Telegram and Google names are used only to identify the upstream project and design inspiration.
