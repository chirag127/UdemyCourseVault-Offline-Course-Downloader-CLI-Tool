# Security Policy

## Supported Versions

We actively support and patch security vulnerabilities in the latest stable version of `UdemyCourseVault-Offline-Course-Downloader-CLI-Tool`.

| Version | Supported          |
|---------|--------------------|
| Latest  | :white_check_mark: |

## Reporting a Vulnerability

We take security vulnerabilities very seriously. If you discover a security issue, please report it via one of the following channels:

*   **GitHub Security Advisory:** [https://github.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool/security/advisories](https://github.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool/security/advisories)
*   **Email:** Please email security@your-domain.com (replace with a real security contact if applicable, otherwise direct to GitHub).

Please do not disclose the vulnerability publicly until it has been addressed. We appreciate your responsible disclosure.

## Vulnerability Disclosure Policy

When you report a vulnerability, we will:

1.  Acknowledge receipt of your report within **48 hours**.
2.  Investigate the reported vulnerability thoroughly.
3.  Provide regular updates on the status of the fix.
4.  Once a fix is available and deployed, we will disclose the vulnerability details publicly, crediting the reporter.

## Security Best Practices

*   **Dependency Management:** We use `uv` for dependency management and aim to keep all dependencies up-to-date to mitigate known vulnerabilities. Regularly run `uv sync` and `uv pip check`.
*   **Code Review:** All code changes undergo rigorous review processes, including security considerations.
*   **Static Analysis:** Tools like `Ruff` are employed to detect potential security flaws and code quality issues.
*   **Testing:** Comprehensive test suites using `Pytest` are run to ensure code integrity and prevent regressions.
*   **Input Validation:** All user inputs and external data are validated to prevent injection attacks or other vulnerabilities.
*   **Secure API Usage:** When interacting with external services (like Udemy's backend, if applicable), we follow best practices for API key management and secure communication.

## Python Security Considerations

As a Python project, we are mindful of common Python security risks:

*   **Dependency Confusion:** Mitigated by using pinned versions and potentially private package indexes if needed.
*   **Deserialization Vulnerabilities:** Careful use of libraries like `pickle` or `json` with untrusted input.
*   **Insecure `eval()` Usage:** Avoided in favor of safer alternatives.

We are committed to maintaining a secure and reliable tool for our users.