# Git Workflow

This document outlines the Git workflow we will use for this project. This workflow is designed to ensure that our code is well-organized, that we can work on multiple features simultaneously without conflicts, and that our main branch is always stable.

## Core Principles

*   **Main Branch is Sacred:** The `main` branch should always be in a deployable state. All changes to the `main` branch must be made through pull/merge requests.
*   **Branch for Everything:** Every new feature, bug fix, or experiment should be developed in its own branch.
*   **Commit Frequently:** Make small, atomic commits with clear and descriptive messages.

## The Workflow

1.  **Create a Branch:** For each new task (as defined in `TICKETS.md`), create a new branch from the `main` branch.
    *   **Branch Naming Convention:** Use a descriptive name for your branch, such as `feature/new-auth-flow` or `fix/login-bug`.

2.  **Make Commits:** As you work on the task, make regular commits.
    *   **Commit Message Style:** We will follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification. Each commit message should have a type (e.g., `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`) and a clear description of the change.
    *   **Example Commit Messages:**
        *   `feat: add user authentication endpoint`
        *   `fix: correct spelling in README.md`
        *   `docs: update installation instructions`

3.  **Open a Pull/Merge Request:** When the task is complete and all tests are passing, open a pull/merge request to merge the feature branch back into the `main` branch.
    *   **Pull Request Template:** The pull request description should clearly explain the changes that were made and link to the corresponding ticket in `TICKETS.md`.

4.  **Code Review:** The user will review the pull request. The AI can also be asked to review the code for potential issues.

5.  **Merge:** Once the pull request is approved, it can be merged into the `main` branch.

6.  **Delete the Branch:** After the branch is merged, it should be deleted.

## AI's Role

The AI agent will follow this workflow for all code changes it makes. The AI will:

*   **Branching:** Ask the user to create a new branch for a new task, following the naming convention (`feature/new-auth-flow`, `fix/login-bug`, etc.).
*   **Committing:** Propose clear and concise commit messages for the changes it makes, adhering to the Conventional Commits specification.
*   **Pull Requests:** Ask the user to open a pull/merge request when a task is complete, ensuring the pull request template is filled out correctly.
*   **Merge Conflicts:** If a merge conflict occurs, the AI will not attempt to resolve it automatically. It will inform the user of the conflict and ask for guidance on how to proceed.
