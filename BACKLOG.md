# [PROJECT_NAME] Backlog

This backlog captures product ideas and technical improvements without letting the product drift away from the core vision in `PRODUCT_VISION.md`.

Backlog items are candidate ideas. They normally do **not** receive feature IDs. Assign a stable feature ID, such as `FEAT-001`, only when an item moves from `BACKLOG.md` into `Building`.

## Rating Method

Feature score is calculated from usefulness and complexity:

`score = usefulness - complexity + 3`

- Usefulness: 1 low, 5 high.
- Complexity: 1 easy, 5 hard.
- Score: 1 low priority, 7 highest priority.

## Feature Backlog

| Feature Idea | Usefulness | Complexity | Score | Notes |
| --- | ---: | ---: | ---: | --- |
| [Feature idea] | [1-5] | [1-5] | [1-7] | [Briefly describe user value, expected behavior, and constraints from `PRODUCT_VISION.md`.] |
| [Feature idea] | [1-5] | [1-5] | [1-7] | [Describe the smallest useful version and what should be avoided.] |

**EXAMPLE ONLY:**

| Feature Idea | Usefulness | Complexity | Score | Notes |
| --- | ---: | ---: | ---: | --- |
| Restore from backup | 5 | 3 | 5 | Let users choose a backup file, validate it, preview what will be restored, and confirm before replacing current data. Keep this protective and simple, not a full file-management system. |
| Search all saved content | 4 | 2 | 5 | Expand search beyond item titles to include notes, details, and related history. This makes the library more useful without adding much UI weight. |
| Direct item sharing | 4 | 3 | 4 | Let users intentionally share one saved item through the system share sheet. Avoid accounts, follower graphs, feeds, recommendations, or background sharing unless the product vision changes. |

## Parking Lot

These ideas are not aligned enough for active backlog grooming right now.

| Idea | Reason |
| --- | --- |
| [Idea] | [Reason this does not currently align, or what would need to change before reconsidering it.] |
| [Idea] | [Reason this does not currently align, or what would need to change before reconsidering it.] |

**EXAMPLE ONLY:**

| Idea | Reason |
| --- | --- |
| Social community features | Not aligned with a private, user-controlled product direction because it implies accounts, a social graph, moderation, and ongoing relationship management. Prefer direct, user-initiated sharing unless the product vision changes. |
| Built-in task management | Useful in some products, but likely to pull this product away from its core promise. Prefer lightweight export or integration options first. |
| Advanced analytics dashboard | Potentially valuable later, but too heavy for the current product experience unless a future slice clearly supports the north star. |

## Technical Enhancement Backlog

| Priority | Enhancement | Why It Matters |
| ---: | --- | --- |
| 1 | [Technical enhancement] | [Explain how this makes the product safer, easier to maintain, easier to extend, or more reliable.] |
| 2 | [Technical enhancement] | [Explain the risk of not doing this.] |
| 3 | [Technical enhancement] | [Explain what future work this enables.] |

**EXAMPLE ONLY:**

| Priority | Enhancement | Why It Matters |
| ---: | --- | --- |
| 1 | Split a large screen or module into focused components and hooks | Large files that own data, forms, modals, styling, and view logic become risky to change. Splitting them makes future changes safer. |
| 2 | Introduce typed storage and schema migrations | A small storage layer and explicit migrations protect user data as schemas evolve. |
| 3 | Move palette, spacing, and type styles into design tokens | Centralized design tokens keep the visual system consistent and make future theme changes easier. |
| 4 | Accessibility pass for labels, touch targets, contrast, and dynamic type | Clean interfaces should remain usable with assistive technology, larger text, and varied vision needs. |
| 5 | Add lightweight test coverage for transforms and storage behavior | Storage, import, export, and data-shape logic should be protected before data model changes. |
