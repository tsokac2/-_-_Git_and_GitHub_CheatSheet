<h1 align="center">Git Diff Stash</h1>

### Overview of the Section
* **[Git Stash](#stash)**
* **[Stashing Basics: Git Stash Save & Pop](#git-stash)**
* **[Git Stash Apply](#apply)**

#
### <a name="stash">Git Stash</a>

**Problem**: Switching branches with uncommitted changes can lead to:

- **Losing changes**: They might come along if there's no conflict, but not guaranteed.
- **Conflicts**: If changes conflict with the destination branch, switching is blocked.

**Solution**: Use git stash to temporarily store uncommitted changes and switch branches freely.

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="git-stash">Stashing Basics: Git Stash Save & Pop</a>

![Stash](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/29.JPG)

![Stashing](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/30.JPG)

![Stashing_pop](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/31.JPG)

**Command**: git stash (or git stash save) - Saves uncommitted changes (staged and unstaged) for later use.

**Purpose**: Temporarily stores changes without cluttering the commit history.

- **Benefits**:
    - Allows switching branches without losing work.
    - Useful for incomplete or temporary changes.

- **Effect**:
    - Reverts changes in the working directory.
    - Stores changes in a "stash" for later retrieval.

- **Retrieval**:
    - ``git stash pop`` - Applies the most recent stashed changes back to the working directory.
    - Can be used on any branch, not just the one where it was stashed.

**Remember**:
- ``git stash`` and ``git stash pop`` are the key commands for stashing and retrieving changes.
- Stashing is a temporary storage, not a replacement for proper commits.

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="apply">Git Stash Apply</a>
**Most common commands**:
- ``git stash``: Stores uncommitted changes in a stash.
- ``git stash pop``: Applies the latest stashed changes and removes them from the stash.

**Alternative command**:
- ``git stash apply``: Applies the latest stashed changes but **keeps them in the stash**.

This is useful if you need to apply the same changes to multiple branches or locations.

**Important notes**:
- ``git stash apply`` can lead to conflicts, which need to be resolved manually.
- Using ``pop`` removes the changes from the stash, while ``apply`` keeps them available for future use.

![Stash Apply]()

**[Back To The Top](#Overview-of-the-Section)**
#