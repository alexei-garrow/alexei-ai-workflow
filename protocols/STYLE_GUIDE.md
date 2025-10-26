# Code Style Guide

This document outlines the coding style and conventions for this project. A consistent style makes the code easier to read, understand, and maintain.

---

### Core Principle

Our codebase should look like it was written by a single person, even though it is a collaboration between a human and an AI. Consistency is the key to readability.

---

### For a Small Project / Prototype

For a small project, the focus should be on automation and consistency without a lot of configuration overhead.

*   **Automated Formatting:**
    *   **What:** Use an automated code formatter to handle all stylistic decisions.
    *   **How:**
        *   Choose a standard, widely-used formatter for the project's language (e.g., `Prettier` for JavaScript/TypeScript, `Black` for Python, `gofmt` for Go).
        *   Use the default configuration for the formatter.
    *   **Goal:** To eliminate all arguments about style and ensure that all code is formatted consistently with zero manual effort.
*   **Linting:**
    *   **What:** Use a linter to catch common errors and potential bugs.
    *   **How:** Use a standard linter with its recommended set of rules.
    *   **Goal:** To automatically catch potential issues before they become bugs.

---

### For a Production Application

For a production application, we build upon the foundation of automated formatting and add more specific conventions.

*   **Automated Formatting & Linting:** This remains the foundation. The rules may be more customized, and the linter may be configured to be more strict.

*   **Naming Conventions:**
    *   **What:** A clear and consistent strategy for naming variables, functions, classes, etc.
    *   **How:** (To be decided based on language/framework conventions, e.g., `camelCase` for variables in JavaScript, `PascalCase` for classes, `snake_case` for Python functions).
    *   **Goal:** To make the code more self-documenting.

*   **Architectural Patterns:**
    *   **What:** A consistent approach to structuring the code and organizing files.
    *   **How:** (To be decided based on the project's needs, e.g., Model-View-Controller, layered architecture, feature-based folders).
    *   **Goal:** To ensure that the project is organized logically and that developers can easily find the code they are looking for.

*   **Comments:**
    *   **What:** Comments should explain the *why*, not the *what*. The code itself should explain what it is doing.
    *   **How:** Use comments to explain complex logic, business rules, or the reasoning behind a particular implementation choice.
    *   **Goal:** To provide context that cannot be inferred from the code itself.
