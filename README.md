# Spryker Deptrac Configuration for Architectural Enforcement

This repository provides a `deptrac.yaml` configuration file designed to enforce architectural rules within Spryker projects using [Deptrac](https://github.com/qossmic/deptrac). Deptrac is a static code analysis tool that helps maintain a clean and manageable codebase by detecting violations of predefined architectural principles.

## What is Deptrac?

Deptrac analyzes dependencies between different parts of your application (layers) and ensures they adhere to defined rules. This configuration helps enforce Spryker's recommended architectural patterns.

## Benefits of using Deptrac with Spryker:

*   **Enforces Spryker's architectural best practices:** Promotes separation of concerns and well-defined module boundaries.
*   **Prevents architectural drift:** Detects unwanted dependencies, ensuring long-term maintainability.
*   **Improves code understanding:** Highlights potential dependency issues and facilitates better comprehension of code structure.

## How to Use Deptrac with Spryker:
1. Composer install deptrac: `composer require valantic-spryker/spryker_deptrac`
2. Run `deptrac -c vendor/valantic-spryker/deptrac.yaml` to analyze your project.
