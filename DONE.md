# Done

Use this file for work that has passed Testing and has been explicitly approved by the user as Done.

Each completed item should keep enough detail to understand what was delivered, why it fit the product vision, what was intentionally excluded, how it was tested, and what checks were completed before commit.

## [FEATURE-ID] [Feature Name]

Source backlog item: `[Original backlog item name]`

Vision fit: [Briefly explain why this feature supports `PRODUCT_VISION.md`.]

Implementation slice:

- [Delivered behavior or change]
- [Delivered behavior or change]
- [Delivered behavior or change]

Non-goals:

- [Out-of-scope behavior or change]
- [Out-of-scope behavior or change]
- [Out-of-scope behavior or change]

Acceptance criteria:

- [Acceptance criterion]
- [Acceptance criterion]
- [Acceptance criterion]

Lightweight UAT test cases completed:

- [Completed UAT test case]
- [Completed UAT test case]
- [Completed UAT test case]

Developer checks completed before Done:

- [Validation check]
- [Validation check]
- [Validation check]

Defects and fixes:

- [Defect or refinement] - [Fix]
- [Defect or refinement] - [Fix]

Commit notes:

- User approved as Done: [Yes/No]
- Commit completed: [Yes/No]
- Commit message: `[Commit message]`

Technical follow-ups:

Capture technical, quality, maintainability, accessibility, performance, test coverage, or implementation follow-ups discovered during build or testing.

Do not invent new product feature ideas here. User-facing feature ideas should come from the user. If a technical follow-up would noticeably affect UX, it may still be captured here as long as it is framed as a technical or quality improvement.

Do not silently add technical follow-ups to `BACKLOG.md`. Alert the user to the proposed follow-up and ask for approval before adding it to the `Technical Enhancement Backlog`.

- [Technical or quality follow-up, if applicable]
- User approved adding to backlog: [Yes/No]
- Added to `BACKLOG.md`: [Yes/No]

**EXAMPLE ONLY:**

## FEAT-001 Restore from backup

Source backlog item: `Restore from backup`

Vision fit: Supports user trust and data ownership by letting users recover their saved content from a backup they control.

Implementation slice:

- Add a simple restore flow for a user-selected backup file.
- Validate the selected file before restore.
- Show a preview before replacing current data.
- Require explicit confirmation before restore runs.

Non-goals:

- Cloud sync.
- Account creation.
- Automatic scheduled backups.
- Full file-management behavior.

Acceptance criteria:

- User can select a valid backup file.
- Unsupported files are rejected with a clear message.
- User sees a preview before restore.
- Restore does not run until the user explicitly confirms.
- Existing export behavior still works.

Lightweight UAT test cases completed:

- Selected a valid backup file and confirmed the preview appeared.
- Canceled restore and confirmed no data changed.
- Confirmed restore and verified expected data appeared.
- Selected an invalid file and confirmed a clear error message appeared.

Developer checks completed before Done:

- `npx tsc --noEmit`
- `npm run lint`
- `git diff --check`

Defects and fixes:

- Invalid file message was too technical - Replaced with clearer user-facing copy.
- Restore preview did not show item count - Added count to preview screen.

Commit notes:

- User approved as Done: Yes
- Commit completed: Yes
- Commit message: `Add backup restore flow`

Technical follow-ups:

- Add test coverage for invalid backup file handling.
- User approved adding to backlog: Yes
- Added to `BACKLOG.md`: Yes

- Consider extracting restore validation into a dedicated utility for easier maintenance.
- User approved adding to backlog: No
- Added to `BACKLOG.md`: No
