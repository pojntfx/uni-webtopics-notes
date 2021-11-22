-   [<span class="toc-section-number">0.1</span>
    Introduction](#introduction)
    -   [<span class="toc-section-number">0.1.1</span>
        Contributing](#contributing)
    -   [<span class="toc-section-number">0.1.2</span>
        License](#license)
-   [<span class="toc-section-number">0.2</span> Overview](#overview)
-   [<span class="toc-section-number">0.3</span>
    Development](#development)
-   [<span class="toc-section-number">0.4</span>
    Distribution](#distribution)
    -   [<span class="toc-section-number">0.4.1</span> Basic
        Distribution Principles](#basic-distribution-principles)
    -   [<span class="toc-section-number">0.4.2</span>
        Pipelines](#pipelines)
    -   [<span class="toc-section-number">0.4.3</span> Distribution to
        RedHat Linux](#distribution-to-redhat-linux)
    -   [<span class="toc-section-number">0.4.4</span> Distribution to
        Debian GNU/Linux](#distribution-to-debian-gnulinux)
    -   [<span class="toc-section-number">0.4.5</span> Distribution to
        Linux (universal)](#distribution-to-linux-universal)
    -   [<span class="toc-section-number">0.4.6</span> Distribution to
        Android](#distribution-to-android)
    -   [<span class="toc-section-number">0.4.7</span> Distribution to
        Windows](#distribution-to-windows)
    -   [<span class="toc-section-number">0.4.8</span> Distribution to
        macOS](#distribution-to-macos)
    -   [<span class="toc-section-number">0.4.9</span> Distribution to
        Kubernetes/the Cloud](#distribution-to-kubernetesthe-cloud)
    -   [<span class="toc-section-number">0.4.10</span> Distribution to
        WebAssembly](#distribution-to-webassembly)
-   [<span class="toc-section-number">0.5</span> Operation](#operation)

Notes on Cloud Native Development

Felicitas Pojtinger

2021-11-19

## Introduction

### Contributing

These study materials are heavily based on [professor Heuzeroth’s
“Spezielle Themen für Web-Anwendungen” lecture at HdM
Stuttgart](https://www.hdm-stuttgart.de/vorlesung_detail?vorlid=5212237).

**Found an error or have a suggestion?** Please open an issue on GitHub
([github.com/pojntfx/uni-webtopics-notes](https://github.com/pojntfx/uni-webtopics-notes)):

<figure>
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAZoAAAGaAQAAAAAefbjOAAADB0lEQVR4nO2czW3jMBCF3ywF5EgBKWBLoTpwSalpOxBLcQEByKMBCm8P/BHt5JJ1Vnak4cGAZX4wCY8eH4cjC/Hl5n99nQEUUkghhRRSSKF9QlLaUK76sV0bFwFi7TA9ZHgKbQ85kmQA4MdFZIoinC0JxBcCMCRJXkPbDU+h7aFYBEDezi/kbEmZosjasVOQnzInhb4JWgTuPACOCXABkOk/fZNCTwgNHy+ZBH+6CL0Ywo8QIj5qeAptDtWIsATyD28TxIUFAgDiCIj7A/SZrCefk0LfAPm8rwCAOCD7SRfaWyx5q/Go4Sm0tUb0AmATiLjktYL+dwKvOzz9nBS6B0LeVWY9gCEZDHNYzJa1rZ+S5Pzkc1LoHgg1z1AzDi4gpydKlNgEMgCcYZjzFhoRe4ZQbvv8xpCzTSDzxrNFSQ0Q1Yj9Q92qwdkmoCwdKHnMGSYryNpZI+IAUAmGdYdhEzjHAYC9CGd7ESDHyyOGp9ADVg1LwjFlu1Cs5CfX1EfsHmqrhmExDgEALKujCIYlIph01TgAVPMRcanrgiXgpyGJOw8Q2IsQWATNTDz9nBS6B6q7T3sjFCUpsdqKuoioRuwcajnLZcj5ST+afJBRmk0DEQfQT0O1lk8+J4XugaqPaKnJnHtgE4VguJ6Lq4/YP9RlqFYrmeMAQEtK1Karxu6h3kcAqPV1q1DANMnQvcYRoBYR5WgLWHeawdxuQVUj9g+h04MuXQk0R1HjhUF9xBGgzll2ptKtGgGgvqhGHAGqVXXxNRFxBAFD+PEd8KcEuDC2+rpFa6gOAIHXDdlK1nx2PgJz7AsnVCN2DWWNqDe/SfSndykV2DBJYAEgvubkFLcenkKbQ9cZqlILkY1DkQwUjWidVSMOAcX2UGctmwHao35eJJ+DlS4/ZE4KfQuU7UJYRCZLyttZpOav9OzzCNCHZ7q8mAQ/mQQ/vg9ENAmIAvqT+ogjQLc+Yq3J7yr2W7Gl+oj9Q72BbGcY3UMbpaQq1XMwjYi9Q6L/TKaQQgoppJBCCv0j9Bdy9rE3fYGmKgAAAABJRU5ErkJggg==" width="150" alt="QR code to source repository" /><figcaption aria-hidden="true">QR code to source repository</figcaption>
</figure>

If you like the study materials, a GitHub star is always appreciated :)

### License

<figure>
<img src="data:image/png;base64,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" width="128" alt="AGPL-3.0 license badge" /><figcaption aria-hidden="true">AGPL-3.0 license badge</figcaption>
</figure>

Uni Web Topics Themes (c) 2021 Felicitas Pojtinger and contributors

SPDX-License-Identifier: AGPL-3.0

## Overview

-   What is DevOps?
-   Which parts of the software lifecycle does it cover?
    -   Development
    -   Distribution (I will focus on this today)
    -   Operation

## Development

-   GitPod
-   Codespaces
-   Coder
-   pojde
-   Waypipe
-   USB forwarding
-   Port forwarding

## Distribution

### Basic Distribution Principles

-   Binaries
-   GPG signing and Gridge
-   Cosign
-   Portability
-   Reproducibility
-   Why we need more than “just binaries”

### Pipelines

-   Bagop
-   Hydrun
-   GitHub Actions
-   Semantic Release

### Distribution to RedHat Linux

-   RPM packages

### Distribution to Debian GNU/Linux

-   DEB package
-   APT repository
-   Yum repository

### Distribution to Linux (universal)

-   Flatpak
-   Flatpak repository

### Distribution to Android

-   APK
-   F-Droid repository

### Distribution to Windows

-   MSI package with auto-updates

### Distribution to macOS

-   DMG package with auto-updates

### Distribution to Kubernetes/the Cloud

-   Docker
-   Kubernetes
-   Helm
-   Skaffold

### Distribution to WebAssembly

-   WASM-Binary
-   WASI/wasm\_exec equivalents

## Operation

-   Sentry
-   OpenTelemetry
-   Prometheus
-   Grafana
