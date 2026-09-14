# Ash’s Agentic Development Demo  
  
## What I’m Going to Show You:  
1. Design for the Design  
2. Iterative Agentic Design  
3. Supervised Agentic Development  
  
  
## Let Me Show You:  
  
### Part 1: Product & UX Design  
1. ++Ideate with ChatGPT++  
2. ++Set the Scope++  
3. ++Snap Some Screenshots++  
    - [ ] Pairs of Existing Mockup vs Reality *.PNG files  
    - [ ] One-Off Bug(s) *.PNG file(s)  
4. ++Use Claude Design++  
    - [ ] *Note: Try to kick this off before lunch/dinner!*  
    - [ ] Inputs:  
        - [ ] Screenshot *.PNG Files  
        - [ ] “designtheidea.md” prompt  using Fable 5.1 (Yes, FABLE!)  
            - [ ] Usually under 1 hour, but not always   
    - [ ] Outputs:   
        - [ ] New Mockups  
  
  
### Part 2: Agentic Software Design  
5. ++Software Design (Measure Twice, Cut Once!)++  
    - [ ] *Note: Try to kick this off before signing off for the day!*  
    - [ ] Inputs - “Context Harness for the Software Design”  
        - [ ] Custom, Claude Code Subagents w/ Shared Project Memory  
            - [ ] “Opus-Engineer” & “Sonnet-Engineer”  
        - [ ] Custom, Claude Code Slash Commands
            - [ ] “/release-web", "/release-dbos", "/release-root", etc.
        - [ ] Existing Codebase Super-Repo  
            - [ ] Git Submodules for All Code Repos  
            - [ ] Meta-Repo w/ Project-Level Docker Compose  
        - [ ] Step 4 Output via Claude Design MCP   
        - [ ] Step 5 Meta-Prompt Outlining the Task using Opus  
        - [ ] Step 5 Prompt (multi-subagent, orchestration)  
            - [ ] 1-10+ hours depending on the inputs   
    - [ ] Outputs (in order)  
        - [ ] ++5-a: “current-design.md”++  
            - [ ] A detailed design of the current state of the entire codebase, kept in a separate file to avoid cluttering subagent context when unnecessary.  
        - [ ] ++5-b: “design-delta.md”++  
            - [ ] A detailed design of how we will update the code across all impacted repos, as well as perform any corresponding administrative, infrastructure or manual tasks.  
        - [ ] ++5-c: “plan.md”++  
            - [ ] A detailed and ordered, plan of the steps necessary to implement “design-delta.md” based on “current-design.md.”  
  
### Part 3: Supervised Agentic Development  
6. ++Time to Code (Careful: It’s just an LLM!!)++  
    - [ ] *Note: Grab some coffee and lock-in before starting!*  
    - [ ] Inputs - “Context Harness for the the Coding”  
        - [ ] Custom, Claude Code Subagents w/ Shared Project Memory  
        - [ ] Existing Codebase Super-Repo  
        - [ ] Step 3 Output via Claude Design MCP  
        - [ ] Select Step 4 Outputs  
            - [ ] “design-delta.md” and “plan.md” only  
        - [ ] Step 5 Meta-Prompt Outlining the Task using Sonnett  
        - [ ] Step 5 Prompt (multi-subagent, orchestration)  
            - [ ] Don’t set it and forget it!!!!!   
            - [ ] Supervise the coding!!!!!  
    - [ ] Outputs  
        - [ ] ++Updated “plan.md”++  
            - [ ] Each task marked “Done” along the way  
        - [ ] Updated, TDD Code w/ Tests  
7. Test it Manually & Repeat  
    - [ ] *Note: Grab some more coffee!*  
    - [ ] Kick the tires on the changes.  
    - [ ] If applicable, deploy the changes.  
    - [ ] Return to Step 1.  
  
  
## What I Showed You:  
1. Use Claude Design and Codex to Prepare Artifacts for the Software Design  
2. Use Claude Code with Iterative Subagents to Create the Design and Implementation Plan  
3.  Use Claude Code with the Play  
