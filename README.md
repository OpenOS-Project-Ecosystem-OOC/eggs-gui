[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for managing the penguins-eggs system, combining multiple frontends: a Go-based daemon, a BubbleTea terminal UI (TUI), a NodeGUI desktop application, and a NiceGUI web interface. It is designed for developers and system administrators who need a centralized and flexible way to interact with penguins-eggs across different environments.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four main components that interact to provide a unified GUI for penguins-eggs:

1. **Go Daemon (`daemon`)**: A backend service written in Go that handles core operations and communicates with other components.
2. **BubbleTea TUI (`tui`)**: A terminal-based user interface built with the BubbleTea framework, which interacts with the daemon.
3. **NodeGUI Desktop (`desktop`)**: A desktop application built with NodeGUI, providing a graphical interface that communicates with the daemon.
4. **NiceGUI Web Frontend (`web`)**: A web-based interface built with Python and NiceGUI, also interacting with the daemon.

The daemon serves as the central component, managing the application's state and providing APIs for the TUI, desktop, and web interfaces. Each frontend communicates with the daemon to perform operations and display data.

The repository structure is as follows:

```plaintext
.
├── Makefile          # Build and run commands
├── README.md         # Project documentation
├── LICENSE           # License information
├── daemon/           # Go daemon source code
├── tui/              # BubbleTea TUI source code
├── desktop/          # NodeGUI desktop app source code
├── web/              # NiceGUI web frontend source code
├── assets/           # Static assets (e.g., icons, desktop files)
├── config/           # Configuration files
├── proto/            # Protocol buffer definitions
├── scripts/          # Helper scripts
├── locales/          # Localization files
└── .github/          # GitHub workflows and CI/CD configurations
```
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

- **check-gitlab-sync.yml**: Verifies synchronization between GitHub and GitLab repositories.
- **cleanup-branches.yml**: Removes stale branches from the repository.
- **cleanup-pollution.yml**: Cleans up temporary or unnecessary files.
- **mirror.yaml**: Mirrors the repository to other platforms.
- **pr-automation.yml**: Automates pull request labeling and merging.
- **rate-limit-status.yml**: Monitors API rate limits and logs status.
- **rotate-token.yml**: Rotates authentication tokens for security.
- **sync-forks.yml**: Synchronizes forks with their upstream repositories.
- **update-readmes.yml**: Updates README files across the repository.

Required secrets:
- `GITHUB_TOKEN`: Automatically provided by GitHub for repository-related actions.
- `GL_ACCESS_TOKEN`: Required for GitLab synchronization workflows.
- `MIRROR_API_KEY`: Needed for mirroring workflows to external platforms.
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
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896): 267 commits
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
| File | Description |
|---|---|
| [config/gitlab-subgroups.yml](https://github.com/Interested-Deving-1896/eggs-gui/blob/main/config/gitlab-subgroups.yml) | GitLab subgroup map |
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
[MIT](https://github.com/Interested-Deving-1896/eggs-gui/blob/master/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
