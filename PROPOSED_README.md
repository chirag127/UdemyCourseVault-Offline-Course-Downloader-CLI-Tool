# 🎓 UdemyCourseVault-Offline-Course-Downloader-CLI-Tool

[![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool/ci.yml?label=Build&style=flat-square)](https://github.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool?style=flat-square)](https://codecov.io/github/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool)
[![Language](https://img.shields.io/github/languages/top/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool?style=flat-square&logo=python)](https://www.python.org/)
[![License](https://img.shields.io/github/license/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool?style=flat-square)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool?style=flat-square)](https://github.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool/stargazers)

--- 

**Star ⭐ this Repo** if you find this utility valuable for managing your educational assets.

This repository contains a cross-platform Python CLI utility engineered to securely download Udemy course materials for personal archival and offline consumption. It robustly handles complex HLS streaming formats and integrates download resumption capabilities for uninterrupted access.

## 🚀 Architecture Overview

The project adheres to a **Modular Monolith** pattern, ensuring high cohesion within functional domains (Authentication, Download Management, HLS Processing) while remaining easily maintainable as a single deployable unit. The CLI utilizes the `Click` framework for superior user experience.

text
UdemyCourseVault-Offline-Course-Downloader-CLI-Tool/
├── src/
│   ├── core/           # Core logic, configuration management
│   ├── cli.py          # Main Click interface entry point
│   ├── downloader/
│   │   ├── session.py  # Authentication & session handling
│   │   └── streams.py  # HLS/M3U8 parsing and segment download
│   └── utils/
│       └── filesystem.py # Resumption and file management
├── tests/
│   └── ...
├── pyproject.toml      # Dependency management (uv)
└── README.md


## 📋 Table of Contents
1. [Prerequisites & Setup](#prerequisites--setup)
2. [Core Features](#core-features)
3. [Usage Examples](#usage-examples)
4. [Development & Contribution](#development--contribution)
5. [🤖 AI Agent Directives (Apex Protocol)](#-ai-agent-directives-apex-protocol)

## 🛠️ Prerequisites & Setup

This project requires Python 3.10+ and leverages **uv** for efficient dependency management.

bash
# 1. Clone the repository
git clone https://github.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool.git
cd UdemyCourseVault-Offline-Course-Downloader-CLI-Tool

# 2. Create and activate a virtual environment using uv (Recommended 2025 Standard)
uv venv
source .venv/bin/activate  # On Windows use: .\.venv\Scripts\activate

# 3. Install dependencies
uv install

# 4. Initialize configuration (e.g., settings file)
# (Follow CLI prompts or generate config file here)


## ✨ Core Features

*   **Cross-Platform CLI:** Native execution on Linux, macOS, and Windows.
*   **HLS Stream Mastery:** Capable of parsing and reconstructing segmented HLS (`.m3u8`) content.
*   **Resumable Downloads:** Tracks partial downloads via manifest, allowing scripts to resume failed transfers seamlessly.
*   **Security Focus:** Employs secure session handling for authentication tokens.

## 💡 Usage Examples

**Basic Download Command:**
bash
python src/cli.py download --url "<COURSE_URL>" --output "./MyNewCourse"


**Resuming a Failed Download:**
(If `session.manifest` exists, the tool automatically detects and resumes)
bash
python src/cli.py download --url "<COURSE_URL>" --resume


## 🤝 Development & Contribution

We enforce strict adherence to Apex architectural principles. All code must pass **Ruff** linting and achieve 90%+ coverage via **Pytest**.

| Command | Description |
| :--- | :--- |
| `uv run format` | Apply standard formatting using Ruff. |
| `uv run lint` | Check code against established style and error rules. |
| `uv run test` | Run unit and integration tests with Pytest. |
| `uv run check` | Run format, lint, and test in sequence. |

### Principles Enforced
*   **SOLID:** Design modular components with clear interfaces.
*   **DRY:** Avoid redundancy, especially in network I/O wrappers.
*   **YAGNI:** Only build features required by current requirements.

## 🤖 AI Agent Directives (Apex Protocol)

<details><summary>Apex Technical Directives for Autonomous Agent Execution</summary>

### 1. Identity & Mandate
**Role:** Senior Principal Software Architect / Elite DevOps Strategist.
**Objective:** Maintain, enhance, and verify the integrity of the `UdemyCourseVault-Offline-Course-Downloader-CLI-Tool` against 2026 standards.

### 2. Tech Stack Definition (Python 3.10+ Environment)
*   **Language Core:** Python 3.10+.
*   **Package Management:** **uv** (Dependency resolution, environment creation).
*   **Linting/Formatting:** **Ruff** (Mandatory compliance for all commits).
*   **Testing Framework:** **Pytest** (Unit and Integration testing).
*   **CLI Library:** `Click` (or equivalent high-standard CLI generator).
*   **Architectural Pattern:** Modular Monolith.

### 3. Verification & Testing Commands
Agents **MUST** verify operational integrity using the following sequence before proposing changes:

1.  **Environment Validation:** `uv venv` followed by environment activation.
2.  **Style Enforcement:** `uv run format` (Failure blocks PR merge).
3.  **Static Analysis:** `uv run lint` (Must pass 100% compliance).
4.  **Functional Test Suite:** `uv run test` (Target coverage must exceed 90% for new feature code).

### 4. Architectural Constraints
*   **API Interaction:** All network calls must use asynchronous clients where possible (e.g., `httpx` asyncio support) to optimize I/O blocking during segment fetching.
*   **State Management:** The download manifest/resume file must use an immutable, versioned schema (JSON or TOML) for persistence.
*   **Error Handling:** Implement specific `try...except` blocks for network failures, HLS parsing errors, and authentication failures, logging detailed context using Python's standard `logging` module.

</details>


[⬆️ Back to Top](#-udemycoursevault-offline-course-downloader-cli-tool)