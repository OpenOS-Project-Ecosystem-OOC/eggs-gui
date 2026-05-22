[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for managing the penguins-eggs system, combining multiple frontends: a Go-based daemon, a BubbleTea terminal user interface (TUI), a NodeGUI desktop application, and a NiceGUI web interface. It is designed for developers and system administrators who need a centralized and flexible way to interact with penguins-eggs across different platforms and environments.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four main components that interact to provide a unified GUI for penguins-eggs:

1. **Go Daemon**: A backend service (`eggs-daemon`) written in Go, responsible for core operations and serving as the central communication hub for other components.
2. **BubbleTea TUI**: A terminal-based user interface (`eggs-tui`) built with the BubbleTea framework, which interacts with the daemon for CLI-based user interactions.
3. **NodeGUI Desktop**: A desktop application built with NodeGUI, providing a graphical interface. It communicates with the daemon for backend operations.
4. **NiceGUI Web**: A web-based frontend built with Python and NiceGUI, offering a browser-accessible interface. It also interacts with the daemon.

The components communicate with the daemon via inter-process communication (IPC) or HTTP APIs. The daemon must be running for the TUI, desktop, and web interfaces to function.

Directory structure:
```plaintext
.
├── assets/          # Static assets (e.g., icons, desktop files)
├── config/          # Configuration files
├── daemon/          # Go daemon source code
├── desktop/         # NodeGUI desktop application
├── locales/         # Localization files
├── proto/           # Protocol definitions (e.g., gRPC)
├── scripts/         # Helper scripts
├── tui/             # BubbleTea TUI source code
├── web/             # NiceGUI web frontend
├── bin/             # Compiled binaries (output directory)
├── Makefile         # Build and run commands
└── README.md        # Project documentation
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
- **build-and-test.yml**: Builds the Go daemon and TUI binaries using the Makefile targets `daemon` and `tui`. Runs basic tests. No secrets required.  
- **desktop-build.yml**: Builds the NodeGUI desktop application using `npm run build`. Requires `NODE_AUTH_TOKEN` for npm authentication.  
- **web-check.yml**: Verifies Python dependencies for the web frontend using `pip install -r web/requirements.txt`. No secrets required.  
- **deb-package.yml**: Creates a Debian package using the Makefile `deb` target. No secrets required.  
- **mirror-artifacts.yml**: Mirrors build artifacts to external storage. Requires `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`.  
- **sync-to-gitlab.yml**: Synchronizes repository changes to GitLab. Requires `GITLAB_TOKEN`.  
- **validate-config.yml**: Validates configuration files for consistency. No secrets required.  
- **token-health.yml**: Checks the health of API tokens used in workflows. Requires `GITHUB_TOKEN`.  
- **update-readmes.yml**: Updates README files across repositories. No secrets required.  
- **rotate-token.yml**: Rotates API tokens for security purposes. Requires `GITHUB_TOKEN` and `ROTATION_SECRET`.
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
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896): 153 commits

Note: This repository is a mirror. Please refer to the upstream source for additional contributions and updates.
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
| File | Description |
|---|---|
| [.gitlab/merge_request_templates/Default.md](https://github.com/Interested-Deving-1896/eggs-gui/blob/main/.gitlab/merge_request_templates/Default.md) | GitLab MR template |
| [config/gitlab-subgroups.yml](https://github.com/Interested-Deving-1896/eggs-gui/blob/main/config/gitlab-subgroups.yml) | GitLab subgroup map |
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
[MIT](https://github.com/Interested-Deving-1896/eggs-gui/blob/master/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
