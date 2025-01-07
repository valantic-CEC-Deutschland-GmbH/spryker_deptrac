# Spryker Deptrac Configuration for Architectural Enforcement

This repository provides a `deptrac.yaml` configuration file designed to enforce architectural rules within Spryker projects using [Deptrac](https://github.com/qossmic/deptrac). Deptrac is a static code analysis tool that helps maintain a clean and manageable codebase by detecting violations of predefined architectural principles.

## What is Deptrac?

Deptrac analyzes dependencies between different parts of your application (layers) and ensures they adhere to defined rules. This configuration helps enforce Spryker's recommended architectural patterns.

## Benefits of using Deptrac with Spryker:

*   **Enforces Spryker's architectural best practices:** Promotes separation of concerns and well-defined module boundaries.
*   **Prevents architectural drift:** Detects unwanted dependencies, ensuring long-term maintainability.
*   **Improves code understanding:** Highlights potential dependency issues and facilitates better comprehension of code structure.

## Understanding the `deptrac.yaml` Configuration:

The `deptrac.yaml` file defines the architectural rules for your Spryker project:

*   **`paths`:** Specifies the directories containing your Spryker application code:
    *   `./src/Pyz/Zed`: Zed modules (Business Logic)
    *   `./src/Pyz/Client`: Client-side code
    *   `./src/Pyz/Yves`: Yves UI framework code
    *   `./src/Pyz/Glue`: Glue API code
    *   `./src/Pyz/Service`: Standalone services

*   **`layers`:** Defines the architectural layers of your Spryker application:
    *   `Communication`: API endpoints, controllers, etc.
    *   `Business`: Core business logic, domain services, etc.
    *   `Persistence`: Database interaction, repositories, etc.
    *   `Presentation`: UI components, views, templates, etc.
    *   `Client`: Client-side application logic.
    *   `Yves`: Yves UI framework.
    *   `Glue`: Glue API.
    *   `Service`: Standalone services.
    *   `ZedRest`: Legacy REST API within Zed modules.

*   **`ruleset`:** Defines the allowed dependencies between layers. For example:
    *   `Communication` can depend on `Business`, `Client`, `Service`, and `ZedRest`.
    *   `Business` can depend on `Persistence`, `Client`, `Service`, and `ZedRest`.

    This enforces a clear flow of dependencies, preventing unwanted coupling.

*   **`ignore_uncovered_internal_classes: true`:** Prevents Deptrac from reporting dependencies on built-in PHP classes (e.g., `ArrayObject`).
