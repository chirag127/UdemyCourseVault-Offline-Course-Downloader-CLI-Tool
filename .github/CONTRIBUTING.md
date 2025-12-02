# Contributing to UdemyCourseVault-Offline-Course-Downloader-CLI-Tool

We welcome contributions to the **UdemyCourseVault-Offline-Course-Downloader-CLI-Tool** project! This project adheres to rigorous standards, ensuring high-velocity development and zero-defect software through the **Apex Technical Authority** framework.

## 1. Code of Conduct

This project adheres to the Contributor Covenant Code of Conduct. Please read the full [CODE_OF_CONDUCT.md](https://github.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool/blob/main/CODE_OF_CONDUCT.md) to understand our community guidelines.

## 2. Prerequisites

Before contributing, ensure you have the following installed and configured:

*   **Python 3.10+**: Essential for running the project.
*   **uv**: The recommended package manager for managing dependencies.
*   **Ruff**: For linting and formatting code to maintain consistency.
*   **Pytest**: For running tests and ensuring code quality.
*   **Git**: For version control.

Refer to the `README.md` for detailed setup instructions.

## 3. Contribution Workflow

Follow these steps to contribute:

1.  **Fork the Repository**: Create your own fork of `chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool`.
2.  **Clone Your Fork**: Clone your forked repository to your local machine:
    bash
    git clone https://github.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool.git
    cd UdemyCourseVault-Offline-Course-Downloader-CLI-Tool
    
3.  **Set Up Development Environment**: Create a virtual environment and install dependencies:
    bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
    uv pip install -r requirements-dev.txt
    
4.  **Create a New Branch**: Branch out from the `main` branch for your new feature or bug fix. Use a descriptive name:
    bash
    git checkout -b feature/your-feature-name
    # or
    git checkout -b fix/your-bug-fix
    
5.  **Make Your Changes**: Implement your changes, adhering to the project's coding standards and architectural patterns.
6.  **Test Your Changes**: Run the test suite to ensure your changes haven't introduced regressions:
    bash
    pytest
    
7.  **Lint and Format**: Ensure your code is clean and formatted correctly:
    bash
    ruff check .
    ruff format .
    
8.  **Commit Your Changes**: Commit your changes with clear, concise messages. Follow conventional commits if applicable.
    bash
    git add .
    git commit -m "feat: Add new feature for X"
    # or
    git commit -m "fix: Resolve issue Y"
    
9.  **Push to Your Fork**: Push your branch to your fork on GitHub:
    bash
    git push origin feature/your-feature-name
    
10. **Create a Pull Request**: Open a Pull Request from your fork to the `main` branch of the `chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool` repository.
    *   Provide a clear description of your changes.
    *   Reference any relevant issues.
    *   Ensure all checks pass.

## 4. Development Standards & Principles

*   **Apex Technical Authority**: All contributions must align with the **Apex Technical Authority** standards, emphasizing Zero-Defect, High-Velocity, and Future-Proof development.
*   **DRY (Don't Repeat Yourself)**: Avoid redundant code. Use abstractions and helper functions.
*   **SOLID Principles**: Strive for Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion where applicable.
*   **Modularity**: Maintain a modular monolith architecture as defined in `AGENTS.md`.
*   **Testing**: All new code must be accompanied by relevant unit and integration tests.
*   **Documentation**: Update relevant documentation (e.g., README, docstrings) for any significant changes.

## 5. Submitting Issues

If you encounter a bug or have a feature request, please use the provided issue templates in the `.github/ISSUE_TEMPLATE/` directory. Provide as much detail as possible, including steps to reproduce the issue and environment information.

## 6. Architectural Alignment

Contributions should respect the established architecture. Refer to the `AGENTS.md` file for the specific tech stack, architectural patterns, and verification commands that define the project's operating parameters. Any proposed deviation must be well-justified and discussed.

Thank you for contributing to **UdemyCourseVault-Offline-Course-Downloader-CLI-Tool**!