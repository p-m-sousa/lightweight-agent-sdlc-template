# [PROJECT_NAME] Kanban

Use this lightweight board for work that has moved out of `BACKLOG.md`.

## Workflow Rules

1. Review `PRODUCT_VISION.md`.
2. Confirm the feature passes the north-star decision filter.
3. Assign a stable feature ID, remove the item from `BACKLOG.md`, and pull one small slice into `Building`.
4. Define scope, non-goals, acceptance criteria, and lightweight UAT test cases before or during implementation.
5. Keep the feature in `Building` while implementation, refactoring, unit testing, smoke testing, and UAT test-case preparation are in progress.
6. Do not move a feature from `Building` to `Testing` until the user explicitly approves.
7. Keep the feature in `Testing` while the user performs E2E UAT. If UAT fails, document defects and fixes in the matching status detail file.
8. Do not move a feature from `Testing` to `Done` until the user explicitly approves.
9. Commit only after the user has explicitly approved the feature as `Done`.

## Board

The board shows only the stable feature ID and short feature name. Details belong in the matching status detail file.

<table>
  <thead>
    <tr>
      <th>Building</th>
      <th>Testing</th>
      <th>Done</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        None.
      </td>
      <td>
        None.
      </td>
      <td>
        None.
      </td>
    </tr>
  </tbody>
</table>

**EXAMPLE ONLY:**

```html
<strong>FEAT-001 Restore from backup</strong>
```

## Status Details

- Building details: [BUILDING.md](BUILDING.md)
- Testing details: [TESTING.md](TESTING.md)
- Done details: [DONE.md](DONE.md)
