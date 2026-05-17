[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface for managing penguins-eggs, a system provisioning tool. It integrates multiple components, including a Go-based daemon, a terminal user interface (TUI) built with BubbleTea, a desktop application using NodeGUI, and a web frontend powered by NiceGUI. It is used by developers and system administrators to streamline provisioning workflows across different interfaces.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four main components that interact to provide a unified GUI for penguins-eggs:

1. **Go Daemon (`daemon`)**: A backend service written in Go that handles core operations. It communicates with the other components via APIs.
2. **BubbleTea TUI (`tui`)**: A terminal-based user interface built with the BubbleTea framework. It interacts with the daemon for real-time updates and operations.
3. **NodeGUI Desktop (`desktop`)**: A desktop application built with NodeGUI. It provides a graphical interface and communicates with the daemon via HTTP or WebSocket.
4. **NiceGUI Web Frontend (`web`)**: A web-based interface built with NiceGUI (Python). It also interacts with the daemon for backend operations.

The directory structure is organized as follows:

```plaintext
.
├── Makefile          # Build and run tasks
├── daemon            # Go daemon source code
│   └── cmd           # Main entry point for the daemon
├── tui               # BubbleTea TUI source code
│   └── cmd           # Main entry point for the TUI
├── desktop           # NodeGUI desktop app source code
│   ├── src           # Application logic
│   └── dist          # Build output
├── web               # NiceGUI web frontend source code
│   ├── static        # Static assets
│   └── templates     # HTML templates
├── assets            # Shared assets (e.g., icons, desktop files)
├── proto             # Protocol buffer definitions
├── locales           # Localization files
└── .github           # GitHub workflows and CI/CD configurations
```

Components are built and run independently but require the daemon to be running for full functionality.
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
The repository uses GitHub Actions for continuous integration and automation. The following workflows are defined:

1. **`mirror-osp-to-ooc.yaml`**  
   Mirrors the repository to an external organization.  
   **Required secrets**: `OOC_REPO_TOKEN`.

2. **`mirror.yaml`**  
   Mirrors the repository to a secondary Git hosting service.  
   **Required secrets**: `MIRROR_REPO_TOKEN`.

3. **`trigger-artifact-mirror.yml`**  
   Triggers artifact mirroring to external storage after a successful build.  
   **Required secrets**: `ARTIFACT_STORAGE_KEY`, `ARTIFACT_STORAGE_SECRET`.

Each workflow is located in the `.github/workflows/` directory. Ensure the required secrets are configured in the repository settings for successful execution.
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
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896) - 16 commits

Note: This repository is a mirror. Please refer to the upstream source for additional details.
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_No dependency graph found. Run `generate-dep-graph.yml` to generate `dep-graph/origins.md`._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
<!-- License not detected — add a LICENSE file to this repo. -->
<!-- AI:end:license -->
