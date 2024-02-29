<h1 align="center">Undoing Changes & Time Traveling</h1>

### Overview of the Section
* **[Checking Out Old Commits](#check-old-commits)**
* **[Re-Attaching Our Detached HEAD!](#re-attaching)**
* **[Referencing Commits Relative to HEAD](#rel-to-head)**
* **[Git Restore](#git-restore)**

#
### <a name="check-old-commits">Checking Out Old Commits</a>

![Checking](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/35.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="re-attaching">Re-Attaching Our Detached HEAD!</a>

1. **Switching back to a branch**:
- **Command**: ``git checkout <branch_name>`` (e.g., git checkout master)

2. **Creating a new branch based on a commit**:

- **Command**: ``git checkout -b <new_branch_name> <commit_hash>`` (e.g., ``git checkout -b chapter_two_redo 4f1234``)

3. Checking out a commit (detached HEAD):

- **Command**: ``git checkout <commit_hash>`` (e.g., ``git checkout 4f1234``)

**Important Notes**:

- Detached HEAD means you're not currently on any branch.
- Use ``git checkout <branch_name>`` to switch back to an existing branch.
- Use ``git checkout -b <new_branch_name> <commit_hash>`` to create a new branch based on a specific commit.
- Use ``git checkout <commit_hash>`` to check out a specific commit (detached HEAD).

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="rel-to-head">Referencing Commits Relative to HEAD</a>
![Relative to HEAD](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/36.JPG)

- You can reference commits relative to the current HEAD using HEAD~ (tilde) followed by a number.
- ``HEAD~1`` refers to the **previous commit** (one step back from HEAD).
- ``HEAD~2`` refers to the **grandparent commit** (two steps back from HEAD), and so on.

**Important Commands**:

- ``git checkout HEAD~<number>``: Checks out the commit that is ``<number>`` commits before the current HEAD.
- ``git switch`` -: Switches back to the branch you were previously on (useful when in detached HEAD).

![Relative to HEAD](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/37.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="git-restore">Git Restore</a>

![Relative to HEAD](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/38.JPG)

![Relative to HEAD](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/39.JPG)


**New command**: git restore is a new and experimental command in Git. It helps with undoing operations within your repository.

**Discarding Uncommitted Changes**:

- Use ``git restore <file>`` to discard uncommitted changes in a file and restore it to the state at the last commit (similar to ``git checkout HEAD <file>``).

**Restoring from a Specific Commit**:

Use ``git restore --source <commit> <file>`` to restore a file to the state at a specific commit.
- Replace ``<commit>`` with a commit hash or ``HEAD~<n>`` (where n is the number of commits back).

**Caution**: This discards any uncommitted changes in the file.

![Relative to HEAD](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/40.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#

