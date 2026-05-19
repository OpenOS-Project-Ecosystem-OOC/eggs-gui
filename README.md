[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface for managing penguins-eggs, a system provisioning tool. It integrates multiple components, including a Go-based daemon, a terminal user interface (TUI) built with BubbleTea, a desktop application using NodeGUI, and a web frontend powered by NiceGUI. It is designed for developers and system administrators who need a centralized interface to interact with penguins-eggs across different environments.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four main components: a Go-based daemon, a BubbleTea-based TUI, a NodeGUI-based desktop application, and a NiceGUI-based web frontend. The daemon provides core functionality and serves as the backend for the other interfaces. The TUI, desktop, and web frontends interact with the daemon to provide user interfaces for different environments. The directory structure is as follows:

```plaintext
.
├── daemon/       # Go daemon source code
│   └── cmd/      # Entry point for eggs-daemon
├── tui/          # BubbleTea TUI source code
│   └── cmd/      # Entry point for eggs-tui
├── desktop/      # NodeGUI desktop application
│   ├── src/      # Source code for the desktop app
│   └── dist/     # Build output (ignored in clean)
├── web/          # NiceGUI web frontend
│   ├── main.py   # Entry point for the web app
│   └── requirements.txt # Python dependencies
├── assets/       # Shared assets (e.g., icons, desktop files)
├── bin/          # Compiled binaries (created during build)
├── locales/      # Localization files
├── proto/        # Protocol buffer definitions
└── Makefile      # Build and run tasks
```

The daemon must be running for the TUI, desktop, and web interfaces to function. The `Makefile` provides commands for building and running each component.
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
The repository uses GitHub Actions for continuous integration. The following workflows are defined:

1. **`mirror-osp-to-ooc.yaml`**  
   Mirrors the repository from the open-source project (OSP) to an out-of-core (OOC) repository.  
   - **Triggers:** Push to the default branch.  
   - **Required Secrets:** `OOC_REPO_URL`, `OOC_REPO_TOKEN`.

2. **`mirror.yaml`**  
   Mirrors the repository to a secondary location for backup or distribution purposes.  
   - **Triggers:** Push to the default branch.  
   - **Required Secrets:** `MIRROR_REPO_URL`, `MIRROR_REPO_TOKEN`.

3. **`trigger-artifact-mirror.yml`**  
   Triggers artifact mirroring to external storage after a successful build.  
   - **Triggers:** Workflow dispatch or successful completion of specific workflows.  
   - **Required Secrets:** `ARTIFACT_STORAGE_URL`, `ARTIFACT_STORAGE_TOKEN`.
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
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896) - 21 commits
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
[MIT](https://github.com/Interested-Deving-1896/eggs-gui/blob/master/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
