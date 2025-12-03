# UdemyCourseVault-Offline-Video-Downloader-CLI-Tool

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool/assets/12345678/d0b0c0d0-0000-4000-8000-000000000000">
  <img alt="UdemyCourseVault" src="https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool/assets/12345678/d0b0c0d0-0000-4000-8000-000000000000">
</picture>

![Build Status](https://img.shields.io/github/actions/workflow/user/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool/ci.yml?style=flat-square)
![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool?style=flat-square)
![Python Version](https://img.shields.io/badge/python-3.10%2B-blue?style=flat-square&logo=python)
![Uvicorn](https://img.shields.io/badge/uv-0.1.16-green?style=flat-square&logo=uv)
![Ruff](https://img.shields.io/badge/ruff-latest-orange?style=flat-square&logo=ruff)
![Pytest](https://img.shields.io/badge/pytest-latest-purple?style=flat-square&logo=pytest)
![License](https://img.shields.io/github/license/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool?style=flat-square&color=success)
![GitHub Stars](https://img.shields.io/github/stars/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool?style=flat-square&logo=github)

**UdemyCourseVault** is a robust, cross-platform Python CLI tool engineered for efficiently downloading Udemy courses in high-quality formats for seamless offline access. It intelligently handles HLS streams and supports resumable downloads to ensure a reliable course acquisition experience.

[![Star ⭐ this Repo](https://img.shields.io/github/stars/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool?style=social&label=Star)](https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool)

---

## Table of Contents

*   [Overview](#overview)
*   [Features](#features)
*   [Architecture](#architecture)
*   [Getting Started](#getting-started)
*   [Usage](#usage)
*   [Development](#development)
*   [Contributing](#contributing)
*   [License](#license)
*   [AI Agent Directives](#ai-agent-directives)

---

## Overview

UdemyCourseVault aims to provide students with the ultimate flexibility in accessing their purchased Udemy courses. By leveraging modern Python practices and robust networking capabilities, it offers a reliable solution for downloading video content, including those delivered via HLS (HTTP Live Streaming), and ensures that interrupted downloads can be resumed without data loss.

---

## Features

*   **Cross-Platform Compatibility:** Works seamlessly on Windows, macOS, and Linux.
*   **Udemy Course Download:** Specifically designed to download lectures from Udemy courses.
*   **HLS Stream Support:** Capable of downloading and merging HLS segmented video streams.
*   **Resumable Downloads:** Automatically resumes interrupted downloads, saving bandwidth and time.
*   **High-Quality Video:** Prioritizes downloading the best available video quality.
*   **Fast & Efficient:** Utilizes `uv` for optimized package management and `Ruff` for rapid linting/formatting.
*   **Comprehensive Testing:** Extensive test suite powered by `Pytest`.

---

## Architecture

The project follows a **Modular Monolith** architecture. This pattern promotes a clear separation of concerns within a single deployable unit, making it easier to manage, test, and scale.

mermaid
graph TD
    CLI[CLI Interface] --> Auth[Authentication Service]
    CLI --> CourseList[Course Listing Service]
    CLI --> Downloader[Download Manager]
    Auth --> UdemyAPI[Udemy API]
    CourseList --> UdemyAPI
    Downloader --> HLSHandler[HLS Stream Handler]
    Downloader --> Resumable[Resumable Download Module]
    HLSHandler --> VideoSegments[Video Segments]
    Resumable --> DownloadState[Download State Management]
    Downloader --> FileIntegrity[File Integrity Checks]
    CLI --> Config[Configuration Management]
    CLI --> Logging[Logging Module]


---

## Getting Started

### Prerequisites

*   **Python:** Version 3.10 or higher.
*   **pip / uv:** `uv` is recommended for dependency management. Install it with `curl -LsSf https://astral.sh/uv/install.sh | sh`.

### Installation

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool.git
    cd UdemyCourseVault-Offline-Video-Downloader-CLI-Tool
    

2.  **Install dependencies using uv:**
    bash
    uv install
    

---

## Usage

*   **Basic Download Command:**
    bash
    udemy-course-vault download <course_url> --email <your_email> --password <your_password>
    

*   **Other commands and options:**
    bash
    udemy-course-vault --help
    udemy-course-vault download --help
    

---

## Development

### Setup

1.  **Create a virtual environment (if not using uv globally):**
    bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
    

2.  **Install development dependencies:**
    bash
    uv install --with dev
    

### Running Tests

Execute the test suite using Pytest:

bash
pytest


### Linting and Formatting

Ensure code quality and consistency with Ruff:

bash
ruff check .
ruff format .


### Scripts

| Script Name      | Description                                        |
| :--------------- | :------------------------------------------------- |
| `dev:install`    | Installs all development dependencies.             |
| `dev:lint`       | Runs Ruff checks for linting and formatting.       |
| `dev:test`       | Executes the full Pytest test suite.               |
| `dev:coverage`   | Runs tests with coverage reporting.                |
| `prod:install`   | Installs production dependencies.                  |
| `prod:build`     | Builds the production distributable (if applicable). |

---

## Contributing

Contributions are welcome! Please read our [CONTRIBUTING.md](./.github/CONTRIBUTING.md) file for details on how to submit pull requests and report issues.

---

## License

This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0) - see the [LICENSE](./LICENSE) file for full details.

---

## AI Agent Directives

<details>
<summary>Click to expand AI Agent Directives</summary>

### System: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

*   **Role:** Senior Principal Software Architect, Master Technical Copywriter, DevOps Strategist with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
*   **Context:** Current Date is **December 2025**. You are building for the 2026 standard.
*   **Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
*   **Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

### Input Processing & Cognition

*   **Speech-to-Text Interpretation Protocol:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **Mandatory MCP Instrumentation:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

### Context-Aware Apex Tech Stacks (Late 2025 Standards)

*   **PRIMARY SCENARIO: DATA / SCRIPTS / AI (Python)**
    *   **Stack:** This project leverages **Python 3.10+**. Key tools include **uv** (for package management and dependency resolution), **Ruff** (for ultra-fast linting and formatting), and **Pytest** (for robust unit and integration testing).
    *   **Architecture:** Adheres to a **Modular Monolith** pattern, ensuring clear separation of concerns for features like Udemy API interaction, video downloading, and CLI interface, while maintaining a unified deployment.
    *   **CLI Framework:** Uses `Click` (or similar) for a powerful and intuitive command-line interface.

### Development, Testing, and Linting Commands

*   **Install Dependencies:** `uv install`
*   **Lint & Format:** `ruff check .` and `ruff format .`
*   **Run Tests:** `pytest`
*   **Run Tests with Coverage:** `pytest --cov=udemy_course_vault` (adjust `udemy_course_vault` to the actual package name)

### Security Mandates

*   **Dependency Auditing:** Regularly audit dependencies using `uv audit` or similar tools to identify and mitigate vulnerabilities.
*   **Secure API Handling:** Ensure Udemy API credentials are handled securely (e.g., via environment variables or a secure secrets manager), never hardcoded.
*   **Input Validation:** Rigorously validate all user inputs and external data to prevent injection attacks or unexpected behavior.

### Deployment Strategy

*   **Packaging:** Package the CLI tool for distribution (e.g., using `setuptools` or `poetry`) for easy installation via `pip`.
*   **CI/CD:** Utilize GitHub Actions for automated testing, linting, and packaging upon code commits and pull requests.

</details>
