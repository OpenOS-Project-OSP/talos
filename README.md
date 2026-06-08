[update-readmes]   Mode: rewrite — migrating to template structure...
# talos

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/talos)

<!-- AI:start:what-it-does -->
Talos Linux is a minimal, immutable Linux distribution designed specifically for running Kubernetes clusters. It simplifies Kubernetes operations by providing a secure, consistent, and automated operating system environment. It is used by infrastructure engineers and platform teams to streamline Kubernetes deployments and management.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
Talos Linux is structured as a modular, Go-based project designed to support Kubernetes environments. The architecture consists of several key components:

1. **API**: Defines the core APIs for interacting with Talos.
2. **cmd**: Contains CLI tools for managing and interacting with Talos.
3. **internal**: Houses internal packages and utilities used across the project.
4. **config**: Manages configuration files and schemas.
5. **hack**: Includes development and testing scripts.
6. **api**: Provides the API definitions for Talos services.
7. **Makefile**: Automates build, test, and deployment tasks.

The components interact through well-defined APIs, enabling modularity and extensibility. The workflows in `.github/workflows` automate CI/CD, artifact management, and repository synchronization. The directory structure is as follows:

```plaintext
.
├── api/                # API definitions
├── cmd/                # CLI tools
├── config/             # Configuration schemas and files
├── hack/               # Development and testing scripts
├── internal/           # Internal packages
├── .github/workflows/  # CI/CD workflows
├── Makefile            # Build and automation tasks
├── go.mod              # Go module dependencies
├── README.md           # Project documentation
└── Dockerfile          # Docker build configuration
```
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/talos.git
cd talos
```

## Usage

<!-- Add usage examples here. This section is yours — the AI will not modify it. -->

## Configuration

<!-- Document configuration options here. This section is yours — the AI will not modify it. -->

## CI

<!-- AI:start:ci -->
- **ci.yaml**: Runs unit tests, linting, and static analysis for Go code. No secrets required.
- **integration-*.yaml**: Various workflows for running integration tests across different environments (e.g., AWS, GCP, QEMU, air-gapped setups). Requires `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, and `GCP_CREDENTIALS` secrets for cloud-based tests.
- **grype-scan-cron.yaml**: Periodically scans dependencies for vulnerabilities using Grype. No secrets required.
- **artifacts-cron.yaml**: Manages periodic artifact generation and cleanup. No secrets required.
- **cleanup-branches.yml**: Deletes stale branches in the repository. Requires `GITHUB_TOKEN`.
- **mirror-*.yml**: Synchronizes repositories and artifacts with external mirrors. Requires `GITHUB_TOKEN` and `MIRROR_API_KEY`.
- **notify-poller.yml**: Sends notifications for CI events. Requires `SLACK_WEBHOOK_URL`.
- **update-homebrew.yaml**: Updates Homebrew formulae for Talos releases. Requires `HOMEBREW_GITHUB_API_TOKEN`.
- **validate-config.yml**: Validates project configuration files. No secrets required.
- **stale.yml**: Marks inactive issues and pull requests as stale. Requires `GITHUB_TOKEN`.
- **rotate-token.yml**: Rotates API tokens for external integrations. Requires `ROTATION_SECRET`.
- **sync-*.yml**: Synchronizes forks, upstream changes, and documentation. Requires `GITHUB_TOKEN`.
- **rebase-lts.yml**: Rebases long-term support branches. Requires `GITHUB_TOKEN`.
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/talos`](https://github.com/Interested-Deving-1896/talos) and mirrored through:

```
Interested-Deving-1896/talos  ──►  OpenOS-Project-OSP/talos  ──►  OpenOS-Project-Ecosystem-OOC/talos
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
[@smira](https://github.com/smira) (2734 commits)  
[@andrewrynhard](https://github.com/andrewrynhard) (1105 commits)  
[@frezbo](https://github.com/frezbo) (522 commits)  
[@rsmitty](https://github.com/rsmitty) (243 commits)  
[@Unix4ever](https://github.com/Unix4ever) (175 commits)  
[@bradbeam](https://github.com/bradbeam) (159 commits)  
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896) (134 commits)  
[@AlekSi](https://github.com/AlekSi) (113 commits)  
[@shanduur](https://github.com/shanduur) (96 commits)  
[@utkuozdemir](https://github.com/utkuozdemir) (91 commits)  
[@sergelogvinov](https://github.com/sergelogvinov) (85 commits)  
[@dsseng](https://github.com/dsseng) (74 commits)  
[@Ulexus](https://github.com/Ulexus) (68 commits)  
[@Orzelius](https://github.com/Orzelius) (49 commits)  
[@TimJones](https://github.com/TimJones) (42 commits)  
[@steverfrancis](https://github.com/steverfrancis) (40 commits)  
[@rothgar](https://github.com/rothgar) (23 commits)  
[@tgerla](https://github.com/tgerla) (23 commits)  
[@Iheanacho-ai](https://github.com/Iheanacho-ai) (19 commits)  
[@mcanevet](https://github.com/mcanevet) (15 commits)  
[@nberlee](https://github.com/nberlee) (15 commits)  
[@laurazard](https://github.com/laurazard) (13 commits)  
[@jnohlgard](https://github.com/jnohlgard) (12 commits)  
[@jonkerj](https://github.com/jonkerj) (10 commits)  
[@salkin](https://github.com/salkin) (9 commits)  
[@oscr](https://github.com/oscr) (9 commits)  
[@patatman](https://github.com/patatman) (8 commits)  
[@oguzkilcan](https://github.com/oguzkilcan) (8 commits)  
[@flokli](https://github.com/flokli) (6 commits)  
[@alongwill](https://github.com/alongwill) (5 commits)  

This repository is a mirror. Please refer to the [upstream source](https://github.com/Interested-Deving-1896/talos) for more details.
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
| File | Description |
|---|---|
| [config/gitlab-subgroups.yml](https://github.com/Interested-Deving-1896/talos/blob/main/config/gitlab-subgroups.yml) | GitLab subgroup map |
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
[MPL-2.0](https://github.com/Interested-Deving-1896/talos/blob/main/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
