# Building

Use this file for work currently in the `Building` column of `KANBAN.md`.

## [FEATURE-ID] [Feature Name]

### Scope

- [In-scope behavior or change]
- [In-scope behavior or change]
- [In-scope behavior or change]

**EXAMPLE ONLY:**

- Add a basic restore flow for a user-selected backup file.
- Validate that the selected file matches the supported backup format.
- Preview what will be restored before replacing current data.
- Keep the existing export behavior unchanged.

### Non-Goals

- [Out-of-scope behavior or change]
- [Out-of-scope behavior or change]
- [Out-of-scope behavior or change]

**EXAMPLE ONLY:**

- No cloud sync in this slice.
- No account creation or login.
- No full file-management system.
- No automatic scheduled backups.

### Acceptance Criteria

- [Expected result]
- [Expected result]
- [Expected result]

**EXAMPLE ONLY:**

- A user can select a valid backup file.
- The product rejects unsupported files with a clear, user-friendly message.
- The user sees a preview before confirming restore.
- The restore does not run until the user explicitly confirms.
- Existing export behavior continues to work normally.

### Lightweight UAT Test Cases

- [User test step and expected result]
- [User test step and expected result]
- [User test step and expected result]

**EXAMPLE ONLY:**

- Launch the app and confirm the existing main screen still loads normally.
- Open the restore flow and select a valid backup file; confirm the preview appears.
- Cancel the restore and confirm no data changes.
- Confirm the restore and verify the expected data appears.
- Select an invalid file and confirm a clear error message appears.
