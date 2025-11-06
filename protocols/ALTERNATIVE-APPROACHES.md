# Alternative Integration Approaches

The primary recommended method for integrating this workflow is detailed in the main `README.md` file, using `git archive`. However, there are other valid Git workflows that might better suit your specific needs or preferences. This document outlines those alternatives.

---

## Method 1: Using a Git Submodule

A Git submodule is a way to embed another repository within your main project repository. It keeps the commit histories completely separate but linked.

### How It Works

Your main project will contain a reference to a specific commit in this workflow repository. The workflow files will reside in a dedicated subdirectory.

### Implementation Steps

1.  **Navigate to your project's root directory.**
2.  **Add the submodule:** This command clones the workflow repository into a new directory (e.g., `ai-workflow`) and creates a `.gitmodules` file to track it.
    ```bash
    git submodule add https://github.com/Alexei-AI-Workflow/alexei-ai-workflow.git ai-workflow
    ```
3.  **Commit the change:**
    ```bash
    git commit -m "feat: Add AI workflow as a submodule"
    ```

### Pros and Cons

*   **Pros:**
    *   **Clean History:** The workflow's history and your project's history are never mixed.
    *   **Easy Updates:** You can easily pull the latest changes into the submodule.
    *   **Version Pinning:** Your project is tied to a specific version of the workflow, providing stability.

*   **Cons:**
    *   **Increased Complexity:** Cloning requires an extra flag (`git clone --recurse-submodules`). Other developers need to be aware of the submodule workflow.
    *   **Files in Subdirectory:** All workflow files are nested in a subdirectory (e.g., `ai-workflow/protocols/PLANNING.md`), which may not be ideal if you want them at the root.

---

## Method 2: Using a Git Remote and Merge

This method involves adding the workflow repository as a temporary "remote" and merging its files into your project.

### How It Works

You are telling Git about another repository, pulling its files, and merging them into your own. The `--allow-unrelated-histories` flag is necessary because your project and this template do not share a common starting point.

### Implementation Steps

1.  **Navigate to your existing project's directory.**
2.  **Add the workflow repository as a remote:**
    ```bash
    git remote add workflow-template https://github.com/Alexei-AI-Workflow/alexei-ai-workflow.git
    ```
3.  **Fetch the files** from the remote:
    ```bash
    git fetch workflow-template
    ```
4.  **Merge the files** into your project:
    ```bash
    git merge workflow-template/main --allow-unrelated-histories
    ```
5.  **Clean up** by removing the temporary remote (optional but recommended):
    ```bash
    git remote remove workflow-template
    ```

### Pros and Cons

*   **Pros:**
    *   **Files at Root:** The workflow files are integrated directly into your project's root directory structure.
    *   **Allows for Updates:** If you don't remove the remote, you can pull future updates from the workflow template.

*   **Cons:**
    *   **One-Time Complexity:** The initial merge command is slightly more complex than a simple copy.
    *   **History is Merged:** The commit history of the template will be visible in your project's history, which may be undesirable for some.
