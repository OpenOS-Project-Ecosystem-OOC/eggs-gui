[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/OpenOS-Project-OSP/eggs-gui) [![KDE Eco](https://img.shields.io/badge/KDE%20Eco-certified-brightgreen?logo=kde&logoColor=white&style=flat-square)](https://eco.kde.org/) [![Blue Angel](https://img.shields.io/badge/Blue%20Angel-DE--UZ%20215-0055a4?style=flat-square)](https://www.blauer-engel.de/en/certification/criteria)



<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for the Penguins-Eggs toolset, combining a Go-based daemon, a BubbleTea terminal UI (TUI), a NodeGUI desktop application, and a NiceGUI web frontend. It is designed for users managing Linux live system remastering, ISO creation, diagnostics, and configuration tasks, offering multiple interface options to interact with Penguins-Eggs.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four main components: a Go-based daemon, a BubbleTea-based TUI, a NodeGUI desktop application, and a NiceGUI web frontend. These components interact with each other through the Go daemon, which serves as the backend service. The TUI, desktop, and web interfaces communicate with the daemon to provide a unified user experience for managing penguins-eggs functionalities such as diagnostics, ISO building, and configuration.

The repository is organized as follows:

```plaintext
.
├── bin/                # Compiled binaries for the daemon and TUI
├── daemon/             # Go-based backend service
├── tui/                # BubbleTea-based terminal user interface
├── desktop/            # NodeGUI-based desktop application
├── web/                # NiceGUI-based web frontend
├── proto/              # Protocol buffer definitions
├── config/             # Configuration files
├── assets/             # Static assets (e.g., icons, desktop files)
├── doc/                # Documentation
├── Makefile            # Build and run tasks
├── package.json        # Node.js project metadata and scripts
├── Dockerfile          # Docker configuration
└── README.md           # Project documentation
```

The `Makefile` defines tasks for building and running the components. The daemon must be running for the TUI, desktop, and web interfaces to function.
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/eggs-gui.git
cd eggs-gui
```

## Usage

<!-- Add usage examples here. This section is yours — the AI will not modify it. -->

## Configuration

<!-- Document configuration options here. This section is yours — the AI will not modify it. -->

## CI

<!-- AI:start:ci -->
The repository uses GitHub Actions for continuous integration and automation. Below are the relevant workflows:

- **build.yml**: Builds the project for all supported platforms. No secrets required.
- **build-x86.yml**: Builds the project for x86 architecture. No secrets required.
- **build-arm64.yml**: Builds the project for ARM64 architecture. No secrets required.
- **ci.yaml**: Runs linting, tests, and static analysis. No secrets required.
- **deploy-book.yml**: Deploys documentation to the project website. Requires `DOCS_DEPLOY_KEY`.
- **mirror-artifacts.yml**: Syncs build artifacts to external storage. Requires `ARTIFACT_STORAGE_KEY`.
- **sync-to-gitlab.yml**: Mirrors the repository to GitLab. Requires `GITLAB_TOKEN`.
- **release.yaml**: Handles version tagging and release creation. Requires `GITHUB_TOKEN`.

Secrets must be configured in the repository settings for workflows requiring them.
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/eggs-gui`](https://github.com/Interested-Deving-1896/eggs-gui) and mirrored through:

```
Interested-Deving-1896/eggs-gui  ──►  OpenOS-Project-OSP/eggs-gui  ──►  OpenOS-Project-Ecosystem-OOC/eggs-gui
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896): 879 commits

*Note: This repository is a mirror. Please refer to the upstream source for additional contributions.*
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

<!-- AI:start:accessibility -->
This repo uses automated accessibility auditing via `check-accessibility.yml`.

Checks include: CODEOWNERS ownership coverage, README screen-reader compatibility,
WCAG 2.1 AA HTML compliance, audio overview (espeak-ng), and Braille output (liblouis).




Run the [Check Accessibility](https://github.com/Interested-Deving-1896/eggs-gui/actions/workflows/check-accessibility.yml)
workflow to generate the first report and accessibility artifacts.
See [DOCS/accessibility.md](https://github.com/Interested-Deving-1896/eggs-gui/blob/main/DOCS/accessibility.md) for the full reference.
<!-- AI:end:accessibility -->

## License

<!-- AI:start:license -->
[MIT](https://github.com/Interested-Deving-1896/eggs-gui/blob/master/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
