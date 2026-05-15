# AGENTS.md

## Template Usage Rules

These SDLC files are designed to be copied into a project repo and adapted by the agent for that project.

- Replace bracketed placeholders with project-specific language.
- Treat all `**EXAMPLE ONLY:**` content as illustrative, not as project requirements.
- Remove or replace example content once real project content exists.
- Do not add new workflow sections unless needed to keep the SDLC process clear, complete, or functional.
- Keep the workflow lightweight.

## Agent Autonomy Rules

- The agent may suggest user-facing feature ideas in chat when they seem relevant, but must not add user-facing feature ideas to `BACKLOG.md` unless the user explicitly approves.
- The agent may identify technical, quality, accessibility, maintainability, performance, test coverage, or UX-polish follow-ups discovered during work, but must ask the user before adding them to the Technical Enhancement Backlog.
- The agent must not autonomously make UI tweaks. UI tweaks must be requested or explicitly approved by the user before implementation.
- The agent may mention possible UI tweaks in chat, but must ask for approval before applying them or adding them to `UI_TWEAKS.md`.

## Product Vision Gate

Before adding, changing, or prioritizing any feature, review `PRODUCT_VISION.md`.

Feature suggestions must be evaluated against the product north star:

- Does this support the product's core purpose?
- Does this make the product more useful without making it feel unnecessarily heavier?
- Does this fit the intended user experience?
- Does this preserve the user's sense of safety, ownership, trust, and control?
- Can this be done simply enough that it preserves the intended feel of the product?

If a suggested feature does not clearly align, push back and explain why. If it may align only with constraints, document those constraints in `BACKLOG.md`.

## Backlog Rules

- Put future product ideas in `BACKLOG.md`, not `PRODUCT_VISION.md`.
- Keep `PRODUCT_VISION.md` focused on the product's north star and decision filter.
- Score backlog items using the existing usefulness/complexity rating method.
- Keep product constraints aligned to `PRODUCT_VISION.md`.
- Direct sharing, sync, accounts, automation, analytics, integrations, or other larger product expansions should only be considered when they clearly align with the product vision or the user explicitly changes the product direction.
- Use `KANBAN.md` for active work that has moved out of the backlog.
- Before coding a backlog item, add or update the board in `KANBAN.md` and the matching status detail file with scope, non-goals, acceptance criteria, and lightweight UAT test cases.
- When a backlog item moves into `Building`, remove it from `BACKLOG.md` and track it in `KANBAN.md` plus `BUILDING.md`.
- The only Kanban statuses are `Building`, `Testing`, and `Done`.
- Assign each active feature a stable feature ID, such as `FEAT-001`, only when it moves into `Building`.
- Keep the visual Kanban board minimal: show only the feature ID and feature name in each status column.
- Keep status details in `BUILDING.md`, `TESTING.md`, and `DONE.md`, not below the board in `KANBAN.md`.

## Kanban Workflow

- `Building`: A feature has been picked from `BACKLOG.md` and is being built into a functional feature for user testing. Keep the feature in `Building` while implementing, refactoring, unit testing, smoke testing, and preparing lightweight UAT test cases. Do not move a feature from `Building` to `Testing` until the user provides explicit approval.
- `Testing`: The user has explicitly approved moving the feature from `Building` to `Testing`. The user performs E2E UAT from the provided test cases. If UAT fails, document defects and fixes in `TESTING.md`, make fixes, and wait for the user to test again. Do not move a feature from `Testing` to `Done` until the user provides explicit approval.
- `Done`: The feature has been built, approved for testing, tested, and explicitly approved by the user for a Git commit.

## UI Tweak Process

- Use `UI_TWEAKS.md` for small visual or copy refinements noticed while using the product.
- UI tweaks are not product features and do not need the full Kanban workflow when they are limited to layout polish, spacing, labels, button presentation, visual hierarchy, or similarly small interface adjustments.
- Track lightweight UI tweak notes in `UI_TWEAKS.md` with `Ideas` and `Completed` sections.
- If a requested UI tweak affects app behavior, data shape, navigation structure, permissions, persistence, sharing, restore/backup behavior, or becomes complex enough to warrant planning and UAT, tell the user it should be handled as a feature before building it.
- Preserve the product vision and intended product tone for UI tweaks.
- Prefer icon-only controls when the screen context and icon are clear, while keeping accessible labels for screen readers. Add visible button text only when it improves clarity.

## Implementation Notes

- Prefer simple behavior unless the backlog item explicitly requires a larger pattern.
- Treat user data and user trust according to the promises in `PRODUCT_VISION.md`.
- Preserve the intended visual direction.
- Consider accessibility for all features and UI tweaks, including labels, touch targets, contrast, readable text, and assistive-technology behavior. Make recommendations when accessibility could improve, while recognizing the user may choose a different tradeoff if the accessible option creates a worse overall experience.
- Keep all user-facing text friendly, clear, non-technical, and consistent with the product tone.
- Treat user backups and exports as durable when the product supports them. Future releases that change user content, settings, or export schemas should include a migration path for older supported backup files when practical.
- Run the project's validation commands before committing code changes.

**EXAMPLE ONLY:**

For a TypeScript / Node project, validation commands might include:

- `npx tsc --noEmit`
- `npm run lint`
