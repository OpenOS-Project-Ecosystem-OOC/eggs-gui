[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for managing penguins-eggs, a system customization and deployment tool. It includes a Go-based daemon, a terminal user interface (TUI) built with BubbleTea, a desktop application using NodeGUI, and a web frontend powered by NiceGUI. It is designed for developers and system administrators who need a centralized interface to interact with penguins-eggs across different environments.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four main components: a Go-based daemon, a BubbleTea-based TUI, a NodeGUI-based desktop application, and a NiceGUI-based web frontend. The daemon provides core functionality and serves as the backend for the other components. The TUI, desktop, and web frontends interact with the daemon to provide different user interfaces. The daemon must be running for the other components to function.

The repository is organized as follows:

```plaintext
.
├── Makefile          # Build and run tasks
├── daemon/           # Go daemon source code
│   ├── cmd/          # Main entry point for the daemon
│   └── internal/     # Internal packages for daemon logic
├── tui/              # BubbleTea TUI source code
│   ├── cmd/          # Main entry point for the TUI
│   └── internal/     # Internal packages for TUI logic
├── desktop/          # NodeGUI desktop application
│   ├── src/          # JavaScript/TypeScript source files
│   └── dist/         # Build output
├── web/              # NiceGUI web frontend
│   ├── main.py       # Entry point for the web server
│   └── requirements.txt # Python dependencies
├── assets/           # Static assets (e.g., icons, desktop entry files)
├── proto/            # Protocol buffer definitions
├── locales/          # Localization files
└── bin/              # Compiled binaries (output directory)
```

Each component has its own build process, as defined in the `Makefile`. The `daemon` and `tui` are compiled using Go, the `desktop` app is built with Node.js, and the `web` frontend runs directly with Python.
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
   Mirrors the repository from the open-source platform (OSP) to an out-of-cloud (OOC) environment.  
   **Required secrets:** `OOC_SSH_KEY`, `OOC_REPO_URL`.

2. **`mirror.yaml`**  
   Mirrors the repository to a secondary Git hosting service.  
   **Required secrets:** `MIRROR_REPO_URL`, `MIRROR_AUTH_TOKEN`.

3. **`trigger-artifact-mirror.yml`**  
   Triggers artifact mirroring to external storage after a successful build.  
   **Required secrets:** `ARTIFACT_STORAGE_KEY`, `ARTIFACT_STORAGE_URL`.

Each workflow is located in `.github/workflows/`. Ensure all required secrets are configured in the repository settings before running workflows.
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
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896): 21 commits
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
