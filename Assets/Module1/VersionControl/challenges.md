# Module 1 – Version Control Challenges (GitHub Desktop)

These challenges reinforce Git basics using GitHub Desktop only (no terminal). Keep Unity edits minimal; prefer text changes in this folder to avoid merge issues with scenes.

## Prerequisites

- You have cloned your fork of the course repository via GitHub Desktop (this is your `origin`).
- You added the instructor repository as `upstream`.
- You fetched and merged `upstream/Module1-GitRepo` into `main`.

Folder you’ll use: `Assets/Module1/VersionControl/`

---

## Challenge A – First Sync and Feature Branch

1. Confirm you’re on `main` in GitHub Desktop.
2. Repository → Fetch origin (and upstream if enabled) to ensure you’re up to date.
3. Branch → New Branch… → name: `Module1` → Create from `main` → Publish branch.

Deliverable: A new branch named `Module1` published to your fork.

---

## Challenge B – Add a Script (Minimal Change)

1. In `Assets/Module1/VersionControl/`, create a file named `playermovement.cs`.
2. Add this stub content and save:

```csharp
using UnityEngine;

public class playermovement : MonoBehaviour
{
    void Update()
    {
        // TODO: movement will be added later
    }
}
```

3. In GitHub Desktop, stage (it’s automatic), write message: `Add playermovement stub`, and Commit to `Module1`.
4. Push the `Module1` branch.

Deliverable: Commit visible on your fork’s `Module1` branch with the new file.

---

## Challenge C – Merge to Main

Option 1 (Recommended): Pull Request

- In GitHub Desktop, click `Create Pull Request` (or `Open in GitHub` and create PR targeting `main`).
- Merge the PR on GitHub, then in Desktop fetch/pull to update local `main`.

Option 2 (Local merge)

- Switch to `main` in Desktop.
- Branch → Merge into current branch… → choose `Module1`.
- Push `main`.

Deliverable: `playermovement.cs` now exists on `main`.

---

## Challenge D – Branch Cleanup

1. Delete the remote feature branch (after PR merge, use the Delete Branch button in GitHub).
2. In GitHub Desktop: Branch → Delete… → select `Module1` (local).

Deliverable: `Module1` branch removed locally and remotely.

---

## Challenge E – Revert the Feature (Practice Removal)

1. On `main`, delete `Assets/Module1/VersionControl/playermovement.cs`.
2. Commit with message: `Remove playermovement stub`.
3. Push `main`.

Deliverable: Commit removing the file appears on `main`.

---

## Extra Practice (Unity-Safe)

- Stage vs Unstage: Edit `README.md` in this folder; stage and unstage to see differences.
- Discard changes: Edit `NOTES.md`, then discard in GitHub Desktop.
- Text conflict practice: On `main`, add a line to `NOTES.md` and commit. Create a new branch `conflict-practice`, edit the same line differently and commit. Merge back to `main` and resolve the conflict.
- Revert a commit: Use GitHub Desktop to revert your last commit on `main`.
- Tags (conceptual): Note how releases/tags work on GitHub (no need to create via CLI).
- Stash: Start a change, use Desktop’s `Stash changes` (if available), switch branches, then re-apply.

---

## Submission

- Ensure your `main` has the merge and the later removal commit.
- Share your repository URL with the instructor.
