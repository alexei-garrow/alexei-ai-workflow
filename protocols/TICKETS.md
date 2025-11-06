#  Ai Workflow Tickets

This document serves as the central place to manage all project tasks. Below, you will find a template for creating new tickets and a suggestion for your first task.

## The Core Principle: Consult Before Acting

**The AI must not take any action without consulting the user and getting their approval.**

This means that for any task, the AI must:

1.  **Understand the task:** The AI must first understand the task at hand. This may involve asking clarifying questions.
2.  **Propose a plan:** The AI must then propose a plan of action. This plan should be detailed enough for the user to understand what the AI is going to do.
3.  **Get approval:** The AI must then get the user's approval for the proposed plan.

Only after the user has approved the plan can the AI take action.

## The Workflow

The workflow is as follows:

1.  **The user creates a ticket:** The user will create a ticket in this document for each task that needs to be done.
2.  **The AI analyzes the ticket:** The AI will analyze the ticket and propose a plan of action.
3.  **The user approves the plan:** The user will review the plan and approve it.
4.  **The AI executes the plan:** The AI will execute the plan.
5.  **The user reviews the work:** The user will review the work and provide feedback.

## Ticket Template

> **Note:** For each new ticket, create a new `TASK-EXECUTION.md` file in the `workflows` directory. You can use the `workflows/TASK-EXECUTION-TEMPLATE.md` as a starting point. The new file can be named `workflows/TASK-[Ticket-Number].md`.

### Ticket #[Ticket Number]: [Ticket Title]

*   **Status:** (Backlog | To Do | In Progress | Done)
*   **Description:** (A brief description of the task)
*   **Link to Task Execution File:** `workflows/TASK-[Ticket-Number].md` (Create this file from `workflows/TASK-EXECUTION-TEMPLATE.md` for your new ticket.)

## Suggested First Ticket

*   **Ticket #1:** Fill out the `PLANNING.md` document to define the project's goals and scope.
    *   **Status:** To Do
    *   **Description:** Define the project's goals, scope, and technology stack in `protocols/PLANNING.md`.
    *   **Link to Task Execution File:** `workflows/TASK-1.md` (Create this file from `workflows/TASK-EXECUTION-TEMPLATE.md`)
