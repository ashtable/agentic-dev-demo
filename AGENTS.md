# Repository Guidelines

## Project Structure & Module Organization

This repository contains the prompts, inputs, outputs, and narration used by the Agentic Development Demo; it is not a deployable application.

- `prompts/step-4/` through `prompts/step-6/` hold the reusable Markdown prompts for each demo stage.
- `step-4-input/` contains reference screenshots. Corresponding `step-*-output/` directories hold generated artifacts and may be empty until that step is run.
- `DEMO-SCRIPT.md/` contains the presentation script.
- `.claude/agents/` defines custom agent profiles; `.claude/commands/` contains reusable workflow and release commands.
- `README.md` is the repository overview.

Keep new material with the step that produces or consumes it. Do not place generated artifacts beside reusable prompts.

## Build, Test, and Development Commands

There is no package manifest, build system, or automated test suite. Changes are reviewed as Markdown and image assets. Useful checks are:

```sh
git status --short              # Show changed and untracked files
git diff --check                # Detect whitespace errors
rg '^#' prompts .claude         # Review heading structure
git diff --word-diff -- '*.md'  # Inspect prose changes closely
```

Preview changed Markdown in a renderer and open added PNGs to confirm readability at their native resolution.

## Coding Style & Naming Conventions

Use concise Markdown with ATX headings (`#`, `##`) and blank lines around headings, lists, and code fences. Preserve YAML front matter in `.claude` definitions. Match existing lower-case command names such as `ideatoplan.md` and lower-kebab-case agent names such as `sonnet-engineer.md`.

Name step directories `step-N-input` or `step-N-output`. Screenshot names use an uppercase purpose prefix and descriptive kebab-case, for example `BUG-Trace-View-Overlaps-In-Wide-Resolution.png` or `FUTURE-Graph-View.png`.

## Validation Guidelines

For prompt edits, read the entire workflow to verify numbering, referenced paths, terminology, and expected outputs remain consistent. For command or agent changes, verify the YAML delimiters and required metadata (`name`, `description`, or command `description`). Run `git diff --check` before submitting.

## Commit & Pull Request Guidelines

Recent history uses short, single-purpose subjects with capitalized past-tense verbs, for example `Added Custom Claude Slash-Commands` and `Replaced PDF with HTML for step 4 output`. Follow that established style and avoid mixing unrelated demo steps.

Pull requests should explain the purpose, identify the affected step, list manual validation, and link any relevant issue. Include before/after screenshots when visual assets or demonstrated UI behavior change.
