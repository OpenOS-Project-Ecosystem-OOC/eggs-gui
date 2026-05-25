[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for managing penguins-eggs, a tool for creating and managing Linux system images. It integrates multiple components, including a Go-based daemon, a BubbleTea terminal user interface (TUI), a NodeGUI desktop application, and a NiceGUI web frontend. It is designed for developers and system administrators who need a consolidated interface for interacting with penguins-eggs across different platforms.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four main components: a Go-based daemon, a BubbleTea-based TUI, a NodeGUI desktop application, and a NiceGUI web frontend. The daemon provides core functionality and must be running for the other components to operate. The TUI, desktop, and web interfaces interact with the daemon to provide user-facing functionality. The directory structure reflects this modular design:

```plaintext
.
├── Makefile          # Build and run commands
├── daemon            # Go daemon source code
│   └── cmd           # Entry point for eggs-daemon
├── tui               # BubbleTea TUI source code
│   └── cmd           # Entry point for eggs-tui
├── desktop           # NodeGUI desktop application
│   ├── src           # Source files
│   └── dist          # Build output
├── web               # NiceGUI web frontend
│   └── main.py       # Entry point for the web server
├── bin               # Compiled binaries
├── assets            # Shared assets (e.g., icons, desktop files)
├── config            # Configuration files
└── scripts           # Utility scripts
```

Each component is built independently using the `Makefile`. The `run` targets allow running the daemon and other components together or individually.
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
The repository uses GitHub Actions for continuous integration and automation. Below are the workflows and their purposes:

- **add-mirror-repo.yml**: Adds new repositories to the mirror configuration.
- **cleanup-branches.yml**: Deletes stale branches from the repository.
- **generate-dep-graph.yml**: Generates a dependency graph for the project.
- **mirror-artifacts.yml**: Synchronizes build artifacts to external storage.
- **mirror-orgs-full.yml**: Mirrors all repositories in an organization to another platform.
- **mirror-releases.yml**: Mirrors release artifacts to external repositories.
- **pr-automation.yml**: Automates tasks related to pull requests, such as labeling or assigning reviewers.
- **rate-limit-status.yml**: Monitors and reports GitHub API rate limits.
- **sync-eggs-docs-to-book.yml**: Syncs documentation to an external book format.
- **update-infra-deps.yml**: Updates infrastructure dependencies in the repository.

Some workflows may require the following secrets:
- `GITHUB_TOKEN`: Default token for accessing the repository.
- `MIRROR_REPO_TOKEN`: Token for mirroring repositories.
- `ARTIFACT_STORAGE_KEY`: Key for external artifact storage.
- `DOCS_SYNC_TOKEN`: Token for syncing documentation.

Refer to `.github/workflows/` for full workflow definitions.
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
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896): 182 commits
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
