# Testing

Use this file for work currently in the `Testing` column of `KANBAN.md`.

If no features are currently in Testing, write:

`No features are currently in Testing.`

## [FEATURE-ID] [Feature Name]

### Lightweight UAT Test Cases

- [User test step and expected result]
- [User test step and expected result]
- [User test step and expected result]

**EXAMPLE ONLY:**

- Launch the app and confirm the existing main screen still loads normally.
- Open the new feature and confirm the expected starting state appears.
- Complete the primary user flow and confirm the expected result.
- Try an invalid or edge-case input and confirm the product responds clearly.

### UAT Results

- [Pass/Fail] [Test case or result notes]
- [Pass/Fail] [Test case or result notes]
- [Pass/Fail] [Test case or result notes]

**EXAMPLE ONLY:**

- Pass - Valid backup file showed preview before restore.
- Pass - Canceling restore did not change existing data.
- Fail - Invalid file message was too technical for a normal user.

### Defects and Fixes

- [Defect found] - [Fix made or planned]
- [Defect found] - [Fix made or planned]

**EXAMPLE ONLY:**

- Invalid file message was too technical - Replaced with clearer user-facing copy.
- Restore preview did not show item count - Added count to preview screen.

### Developer Checks

- [Check completed]
- [Check completed]
- [Check completed]

**EXAMPLE ONLY:**

- `npx tsc --noEmit`
- `npm run lint`
- `git diff --check`

### Approval

Do not move this feature to `Done` until the user explicitly approves it.

- User approved moving to Done: [Yes/No]
- Approval notes: [Notes]
