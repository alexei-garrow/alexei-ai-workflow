# Alexei's Ai workflow

A first draft for AI workflows.

The main idea / concept being guardrails of sorts. I want to minimise problems early on by giving a clear outline with guidelines.

The idea is that this repo will be cloned into other repo's and used as the 'Ai workflow'. 

Ideally this not only prevents oversights, but also cuts down on some of the repititive prompts.

As the technology evolves, this could be a very good way to go moving forward!

## Getting Started

To integrate this workflow, you should copy its files into your project's repository without bringing along this template's Git history. Here are the best methods to do that.

### Method 1: For New or Existing Projects (Recommended)

This method uses `git archive` to copy the files from the template repository directly into your project folder. It's clean, fast, and avoids creating temporary clones.

1.  **Navigate to your project's root directory** (either a new, empty one or an existing one).
2.  **Run the `git archive` command:** This will fetch the latest version of the workflow files and extract them into your current directory.
    ```bash
    git archive --format=tar --remote=https://github.com/Alexei-AI-Workflow/alexei-ai-workflow.git main | tar -x
    ```

#### Breaking Down the Command

It might look complex, but this command is doing something simple. Let's break it down:

*   `git archive --format=tar --remote=... main`
    *   This part of the command tells Git to connect to the remote repository, find the `main` branch, and create a `tar` archive of all its files, as if you were creating a `.tar` (like a `.zip`) file.
*   `|`
    *   This is the "pipe" operator. It takes the output of the command on its left (the `tar` archive that `git archive` created in memory) and sends it as the input to the command on its right.
*   `tar -x`
    *   This is the standard `tar` utility. The `-x` flag tells it to **e**xtract the contents of the archive it receives from the pipe. The result is that all the files from the template are placed in your current directory.

3.  **Commit the files** to your project:
    ```bash
    git add .
    git commit -m "feat: Integrate AI workflow protocols"
    git push
    ```

### Method 2: For New Projects (GitHub-Specific)

If this repository is used as a GitHub Template, the easiest way to start a new project is by using the "Use this template" feature on the GitHub UI. This creates a new repository with a clean Git history for you.

### Cleanup: If You Cloned Directly by Mistake

If you accidentally cloned this repository directly, here’s how to fix it by removing the template's Git history.

**This should only be done in a new, empty project folder.**

1.  **Clone the repository** (this is the step you might have already done):
    ```bash
    git clone https://github.com/Alexei-AI-Workflow/alexei-ai-workflow.git .
    ```
2.  **Remove the template's .git directory:**
    ```bash
    rm -rf .git
    ```
3.  **Initialize a new Git repository** for your project:
    ```bash
    git init
    ```
4.  **Add and commit the files** to your new, clean project history:
    ```bash
    git add .
    git commit -m "Initial commit with AI workflow structure"
    ```

### Next Steps

Once the files are integrated, you can proceed with the workflow:

1.  **Review `protocols/PLANNING.md`:**
    *   **For new projects:** Fill out the `PLANNING.md` document to define your project's goals, scope, and technology stack.
    *   **For existing projects:** Follow the "Adapting for Existing Projects" guide in `PLANNING.md` to document your existing project.
2.  **Create your first ticket:** Add a new task to the `protocols/TICKETS.md` file.
3.  **Start the workflow:** Begin the process of planning, executing, and reviewing your tasks with your AI assistant.

### Exploring Other Integration Methods

For alternative or more advanced ways to integrate this workflow into your project, including using Git submodules or remote merges, please refer to [Alternative Integration Approaches](protocols/ALTERNATIVE-APPROACHES.md).

## An Evolving Workflow

This workflow is designed to be adaptable. It can scale with your project from a small prototype to a full production application.

Many of the protocol documents (like `TESTING.md` and `SECURITY.md`) contain different levels of implementation: one for small projects and another for production applications. You can start with a "Minimal" approach and graduate to a "Comprehensive" one when the project's needs change.

This evolution is a conscious choice that we can make during our planning and review cycles, particularly during retrospectives (see `RETROSPECTIVES.md`).

## The Workflow Files

This repository provides a set of templates to guide our development process. Here's a breakdown of each file and its purpose:

### Project Planning & Tracking

*   **`protocols/BRAINSTORMING.md`**: A guide to help brainstorm and define new project ideas.
*   **`protocols/PLANNING.md`**: Defines the project's goals, scope, and technology stack.
*   **`protocols/TICKETS.md`**: A list of all the tasks that need to be done.
*   **`protocols/KANBAN.md`**: A Kanban board to visualize the status of each task (To Do, In Progress, Done).

### Task Execution

*   **`workflows/TASK-EXECUTION.md`**: A template for breaking down and executing a single task.
*   **`protocols/QA.md`**: Outlines our two-stage Quality Assurance process for both individual tasks and the project as a whole.

### Automation & Improvement

*   **`protocols/project-structure.md`**: An overview of the project's directory structure.
*   **`protocols/GIT-WORKFLOW.md`**: Outlines our Git workflow for branching, committing, and merging code.
*   **`protocols/CI-CD.md`**: Our strategy for Continuous Integration and Continuous Deployment, which is about automating our build, test, and deployment processes.
*   **`protocols/RETROSPECTIVES.md`**: A place to hold retrospectives to discuss what went well, what didn't, and how we can improve our workflow.
*   **`notes/NOTES.md`**: For logging our decisions, providing explanations, and asking questions.

## Kanban vs. CI/CD

It's worth clarifying the difference between Kanban and CI/CD, as they are both key parts of our workflow:

*   **Kanban (`protocols/KANBAN.md`)** is for **Project Management**. It's a visual tool to manage the flow of work. It helps us track the status of tasks and manage our priorities. It's about the **"what"** and **"when"** of our work.

*   **CI/CD (`protocols/CI-CD.md`)** is for **Automation and Quality**. It's a plan for automating the process of building, testing, and deploying our code. It improves the quality of our code and makes our deployment process faster and more reliable. It's about the **"how"** of our work.

In short, Kanban manages the tasks, and CI/CD manages the code.