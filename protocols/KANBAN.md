# Kanban Board

This board helps us track the progress of our tasks.

| Backlog | To Do | In Progress | Done |
| :--- | :--- | :--- | :--- |
| Ticket #2: Research authentication libraries. | Ticket #3: Set up basic project structure. | Ticket #4: Implement user registration form. | Ticket #1: Create the initial project structure and workflow files. |
| Ticket #5: Design database schema. | | | |

---

## How Tickets Move Through the Board

To keep our Kanban board synchronized with our development process, a ticket's status should reflect its stage in the Git workflow:

*   **To Do** to **In Progress**: A ticket moves to "In Progress" when a new feature branch is created for it (as per `protocols/GIT-WORKFLOW.md`).
*   **In Progress** to **Done**: A ticket moves to "Done" when its corresponding feature branch is successfully merged into the `main` branch.
