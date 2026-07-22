# Global Agent Rules

These rules apply to all tasks in this workspace.

## Routing and Workflow Integration

Before executing any request or starting any task, you **MUST** read and adhere
to the project's official AI rules defined in the `.ai/` directory:

1. **Routing Framework:** Read `.ai/routing.md` to understand how to classify
   user intent, select the appropriate workflow, and route the task to the
   correct agent role. Do not skip the routing and classification step.
2. **AI Constitution:** Read `.ai/constitution.md` (and any other relevant rule
   files in `.ai/`) to ensure all actions strictly comply with the project's AI
   principles and documentation-first methodology.

Always prioritize the workflows and guidelines defined in the `.ai/` directory
over default behaviors.

## Communication & Language Policy

- **Default Response Language:** You **MUST ALWAYS** communicate and respond to the user in **Vietnamese (Tiếng Việt)** by default.
- **Language Switch:** If the user explicitly requests responses in another language (e.g. English, Japanese), switch to the user's requested language for that conversation.

## Git & Branching Policy for AI Agents

- **Automatic Feature/Module Branching:** Whenever the user requests to create, design, or write code for a new module or feature (e.g. `modules/<module-name>`), you **MUST AUTOMATICALLY** create a new dedicated Git branch (e.g. `git checkout -b feature/<module-name>`) before creating or modifying any documentation or source code files.
- **Branch Naming Conventions:**
  - `feature/<name>` or `module/<name>`: New feature or module development.
  - `bugfix/<name>` or `fix/<name>`: Bug fixes and patches.
  - `docs/<name>`: Pure documentation updates.
  - `refactor/<name>`: Code or architecture refactoring.
- **Conventional Commits:** Commit messages **MUST** follow Conventional Commits format (`feat(...)`, `fix(...)`, `docs(...)`, `chore(...)`, `refactor(...)`).
- **Push & Pull Request Proposal:** Once the task or module is complete and verified, push the branch to remote repository (`git push -u origin <branch-name>`) and inform the user to review or open a Pull Request into `main`.
