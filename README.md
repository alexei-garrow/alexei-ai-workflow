# Alexei's Ai workflow

A first draft for AI workflows.

The main idea / concept being guardrails of sorts. I want to minimise problems early on by giving a clear outline with guidelines.

The idea is that this repo will be cloned into other repo's and used as the 'Ai workflow'. 

Ideally this not only prevents oversights, but also cuts down on some of the repititive prompts.

As the technology evolves, this could be a very good way to go moving forward!

## Getting Started

To start using this workflow in your project, follow these steps:

1.  **Clone this repository:** Clone or copy the files from this repository into the root of your project.
2.  **Review `protocols/PLANNING.md`:**
    *   **For new projects:** Fill out the `PLANNING.md` document to define your project's goals, scope, and technology stack.
    *   **For existing projects:** Follow the "Adapting for Existing Projects" guide in `PLANNING.md` to document your existing project.
3.  **Create your first ticket:** Add a new task to the `TICKETS.md` file.
4.  **Start the workflow:** Begin the process of planning, executing, and reviewing your tasks with your AI assistant.

## The Workflow Files

This repository provides a set of templates to guide our development process. Here's a breakdown of each file and its purpose:

### Project Planning & Tracking

*   **`protocols/PLANNING.md`**: Defines the project's goals, scope, and technology stack.
*   **`protocols/TICKETS.md`**: A list of all the tasks that need to be done.
*   **`protocols/KANBAN.md`**: A Kanban board to visualize the status of each task (To Do, In Progress, Done).

### Task Execution

*   **`workflows/TASK-EXECUTION.md`**: A template for breaking down and executing a single task.
*   **`protocols/QA.md`**: Outlines our two-stage Quality Assurance process for both individual tasks and the project as a whole.

### Automation & Improvement

*   **`protocols/GIT-WORKFLOW.md`**: Outlines our Git workflow for branching, committing, and merging code.
*   **`protocols/CI-CD.md`**: Our strategy for Continuous Integration and Continuous Deployment, which is about automating our build, test, and deployment processes.
*   **`protocols/RETROSPECTIVES.md`**: A place to hold retrospectives to discuss what went well, what didn't, and how we can improve our workflow.
*   **`notes/NOTES.md`**: For logging our decisions, providing explanations, and asking questions.

## Kanban vs. CI/CD

It's worth clarifying the difference between Kanban and CI/CD, as they are both key parts of our workflow:

*   **Kanban (`protocols/KANBAN.md`)** is for **Project Management**. It's a visual tool to manage the flow of work. It helps us track the status of tasks and manage our priorities. It's about the **"what"** and **"when"** of our work.

*   **CI/CD (`protocols/CI-CD.md`)** is for **Automation and Quality**. It's a plan for automating the process of building, testing, and deploying our code. It improves the quality of our code and makes our deployment process faster and more reliable. It's about the **"how"** of our work.

In short, Kanban manages the tasks, and CI/CD manages the code.