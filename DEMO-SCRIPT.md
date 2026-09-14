# Ash’s Agentic Development Demo

## What I’m Going to Show You

1. Design for the Design
2. Iterative Agentic Design
3. Supervised Agentic Development

## Let Me Show You

### Part 1: Product & UX Design

1. **Think, Ideate, and Research with ChatGPT and Codex**
2. **Set the Scope**
3. **Snap Some Screenshots**
    - Pairs of existing mockups vs. reality (`*.PNG` files)
    - One-off bugs (`*.PNG` files)
4. **Use Claude Design**
    - *Note: Try to kick this off before lunch or dinner!*
    - Inputs:
        - Screenshot `*.PNG` files
        - The `designtheidea.md` prompt using Fable 5.1 (yes, Fable!)
            - Usually under one hour, but not always
    - Outputs:
        - New critique diagrams illustrating every mismatch and bug

### Part 2: Agentic Software Design

5. **Software Design (Measure Twice, Cut Once!)**
    - *Note: Try to kick this off before signing off for the day!*
    - Inputs—the context harness for software design:
        - Custom Claude Code subagents with shared project memory
            - `opus-engineer` and `sonnet-engineer`
        - Custom Claude Code slash commands
            - `/ideatoplan` as the hardened orchestration counterpart
        - Existing codebase superrepo
            - Git submodules for all code repositories
            - Metarepo with project-level Docker Compose
        - Step 4 output via the Claude Design MCP
        - Step 5 meta prompt outlining the task using Opus
        - Step 5 prompt with multi-subagent orchestration
            - 1–10+ hours depending on the inputs
    - Outputs, in order:
        - **5a: `current-design.md`**
            - A detailed design of the current state of the entire codebase, kept in a separate file to avoid cluttering subagent context when unnecessary.
        - **5b: `design-delta.md`**
            - A detailed design of how we will update the code across all impacted repositories and perform any corresponding administrative, infrastructure, or manual tasks.
        - **5c: `plan.md`**
            - A detailed, ordered plan of the steps necessary to implement `design-delta.md` based on `current-design.md`.

### Part 3: Supervised Agentic Development

6. **Time to Code (Careful: It’s Just an LLM!)**
    - *Note: Grab some coffee and lock-in before starting!*
    - Inputs—the context harness for coding:
        - Custom Claude Code subagents with shared project memory
        - Custom Claude Code slash commands
            - `/plantocode`, `/release-web`, `/release-dbos`, `/release-root`, etc.
        - Existing codebase superrepo
        - Step 4 output via the Claude Design MCP
        - Step 5 design outputs
            - `current-design.md`, `design-delta.md`, `plan.md`, and the vision brief
        - Selected tasks and design URLs passed to the Step 6 prompt
        - Step 6 prompt with multi-subagent orchestration
            - Don’t set it and forget it—supervise the coding!
    - Outputs:
        - **Updated `plan.md`**
            - Completed, verified tasks marked “Done” at the end of the run
        - Updated TDD code with tests
7. **Test It Manually & Repeat**
    - *Note: Grab some more coffee!*
    - Kick the tires on the changes.
    - If applicable, deploy the changes.
    - Return to Step 1.

## What I Showed You

1. Use Claude Design and Codex to prepare artifacts for the software design.
2. Use Claude Code with iterative subagents to create the design and implementation plan.
3. Use Claude Code with the plan-to-code workflow to implement, test, and—if approved—release selected work.
