% Uni Web Topics Themes
% Felicitas Pojtinger
% \today
\tableofcontents
\newpage

# Uni Web Topics Themes

## Introduction

### Contributing

These study materials are heavily based on [professor Heuzeroth's "Spezielle Themen für Web-Anwendungen" lecture at HdM Stuttgart](https://www.hdm-stuttgart.de/vorlesung_detail?vorlid=5212237).

**Found an error or have a suggestion?** Please open an issue on GitHub ([github.com/pojntfx/uni-webtopics-notes](https://github.com/pojntfx/uni-webtopics-notes)):

![QR code to source repository](./static/qr.png){ width=150px }

If you like the study materials, a GitHub star is always appreciated :)

### License

![AGPL-3.0 license badge](https://www.gnu.org/graphics/agplv3-155x51.png){ width=128px }

Uni Web Topics Themes (c) 2021 Felicitas Pojtinger and contributors

SPDX-License-Identifier: AGPL-3.0
\newpage

## Overview

- What is DevOps?
- Which parts of the software lifecycle does it cover?
  - Development
  - Distribution (I will focus on this today)
  - Operation

## Development

- GitPod
- Codespaces
- Coder
- pojde
- Waypipe
- USB forwarding
- Port forwarding

## Distribution

### Basic Distribution Principles

- Binaries
- GPG signing and Gridge
- Cosign
- Portability
- Reproducibility
- Why we need more than "just binaries"

### Pipelines

- Bagop
- Hydrun
- GitHub Actions
- Semantic Release

### Distribution to RedHat Linux

- RPM packages
- Yum repository

### Distribution to Linux (universal)

- Flatpak
- Flatpak repository

### Distribution to Debian GNU/Linux

- DEB package
- APT repository

### Distribution to Android

- APK
- F-Droid repository

### Distribution to Windows

- MSI package with auto-updates

### Distribution to macOS

- DMG package with auto-updates

### Distribution to Kubernetes/the Cloud

- Docker
- Kubernetes
- Helm
- Skaffold

### Distribution to WebAssembly

- WASM-Binary
- WASI/wasm_exec equivalents

## Operation

- Sentry
- OpenTelemetry
- Prometheus
- Grafana
