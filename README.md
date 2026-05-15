# Lightweight SDLC Agent Workflow

This template provides a small, repo-based SDLC workflow for agent-assisted software projects.

It is designed for lightweight product work where a user wants the agent to help manage feature ideas, active build work, UAT, completion records, and small UI tweaks without turning the project into a heavy process.

## Files Included

| File                | Purpose                                                      |
| ------------------- | ------------------------------------------------------------ |
| `AGENTS.md`         | Gives the agent the operating rules for the workflow.        |
| `PRODUCT_VISION.md` | Defines the product north star, trust promise, principles, and decision filter. |
| `BACKLOG.md`        | Captures candidate product ideas, parking lot items, and technical enhancements. |
| `KANBAN.md`         | Shows active work status using `Building`, `Testing`, and `Done`. |
| `BUILDING.md`       | Captures scope, non-goals, acceptance criteria, and lightweight UAT cases for active build work. |
| `TESTING.md`        | Captures UAT results, defects, fixes, developer checks, and approval to move to Done. |
| `DONE.md`           | Records completed work after user approval, including what was delivered, tested, fixed, and committed. |
| `UI_TWEAKS.md`      | Tracks small user-requested or user-approved UI/copy polish outside the full feature workflow. |

## Quick Start

1. Copy these files into the root of your project repo.
2. Update `PRODUCT_VISION.md` for your project.
3. Review `AGENTS.md` and adjust any project-specific rules.
4. Add candidate ideas to `BACKLOG.md`.
5. When ready to build, move one selected backlog item into `KANBAN.md` under `Building`.
6. Assign the item a stable feature ID, such as `FEAT-001`.
7. Fill out the matching entry in `BUILDING.md`.
8. Build the feature.
9. Ask the user for approval before moving the item to `Testing`.
10. Track UAT in `TESTING.md`.
11. Ask the user for approval before moving the item to `Done`.
12. Record the completed work in `DONE.md`.
13. Commit only after the user has explicitly approved the work as Done.

## Core Workflow

### 1. Product Vision

Start with `PRODUCT_VISION.md`.

This file is the decision filter. Before adding or prioritizing work, the agent should check whether the idea supports the product north star and preserves the intended user experience.

### 2. Backlog

Use `BACKLOG.md` for candidate ideas.

Backlog items normally do not have feature IDs. Feature IDs are assigned only when an item moves into active work.

The backlog has three sections:

- Feature Backlog
- Parking Lot
- Technical Enhancement Backlog

User-facing feature ideas should come from the user or be explicitly approved by the user before being added.

### 3. Kanban

Use `KANBAN.md` only as a lightweight visual board.

The only statuses are:

- `Building`
- `Testing`
- `Done`

The board should show only the feature ID and feature name. Details belong in the matching status file.

### 4. Building

Use `BUILDING.md` for the active work definition.

Each feature should include:

- scope
- non-goals
- acceptance criteria
- lightweight UAT test cases

Do not move work from `Building` to `Testing` until the user explicitly approves.

### 5. Testing

Use `TESTING.md` for UAT and fixes.

Track:

- lightweight UAT test cases
- UAT results
- defects and fixes
- developer checks
- user approval to move to Done

Do not move work from `Testing` to `Done` until the user explicitly approves.

### 6. Done

Use `DONE.md` as the final record of completed work.

Record what was delivered, what was excluded, what was tested, what defects were fixed, what checks passed, and whether the user approved the work as Done.

The agent may identify technical follow-ups, but must ask the user before adding them to `BACKLOG.md`.

### 7. UI Tweaks

Use `UI_TWEAKS.md` for small visual, layout, accessibility, and copy refinements.

UI tweaks must be requested or explicitly approved by the user. The agent may suggest a tweak in chat, but must not apply it or add it to `UI_TWEAKS.md` without user approval.

If a tweak grows into behavior, data, navigation, permissions, persistence, backup/restore, or larger workflow changes, move it into `BACKLOG.md` and the Kanban flow.

## Template Rules

- Replace bracketed placeholders with project-specific language.
- Treat `**EXAMPLE ONLY:**` content as illustrative, not as requirements.
- Remove or replace example content once real project content exists.
- Keep the process lightweight.
- Do not add new workflow sections unless needed to keep the process clear, complete, or functional.

## Recommended File Names

For direct use in a project repo, use these names:

```text
AGENTS.md
PRODUCT_VISION.md
BACKLOG.md
KANBAN.md
BUILDING.md
TESTING.md
DONE.md
UI_TWEAKS.md
README.md
```

## Recommended First Prompt to the Agent

After copying these files into a repo, a user can start with:

```text
Review AGENTS.md and the SDLC workflow files. Then help me adapt PRODUCT_VISION.md for this project. Do not add feature ideas or UI tweaks unless I explicitly approve them.
```

## Philosophy

This workflow is intentionally small.

It gives the agent enough structure to behave consistently, preserve user approval gates, and keep work traceable without creating unnecessary ceremony.
