# Zoho Docs: version history and restore points

## Problem

A document can change substantially over time, and users may notice a mistake only after several edits or after collaborators have made further changes. The current recovery path is unclear when a user needs to compare an earlier version or restore part of a document.

## Proposal

Add a user-visible version history to Zoho Docs. Each saved version should show:

- the timestamp and author;
- a short description of the change;
- a preview of the differences;
- actions to open, download, or restore that version.

Restoring a version should create a new current version rather than deleting the later history. This keeps the audit trail intact and lets users undo an accidental restore.

## Suggested workflow

1. Open **File → Version history**.
2. Select a version from the timeline.
3. Review the side-by-side or inline comparison.
4. Choose **Restore this version** and confirm.
5. Show a notice that the restore created a new version.

## Initial scope

The first release could retain named versions and automatic versions created at meaningful save intervals. It should respect existing document permissions and clearly distinguish versions created by the user from versions created by collaborators.

## Acceptance criteria

- A user can view the version history for a document they can edit.
- The history identifies the author and timestamp of each version.
- A restore does not remove later versions.
- Users without edit permission cannot restore a version.
- The feature works for shared documents and records permission changes in the audit trail.
