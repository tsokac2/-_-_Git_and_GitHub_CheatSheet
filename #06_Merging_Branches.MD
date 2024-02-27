<h1 align="center">Merging Branches</h1>

### Overview of the Section
* **[Merging](#merging)**
* **[Performing A Fast Forward Merge](#fast-forward)**
* **[Generating Merge Commits](#merge-commits)**

#
### Merging

![Merging](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/21.JPG)

- **Merging branches**: Combines work from one branch into another using the ``git merge`` command.
**Common workflow**: Treat ``master`` branch (or similar) as the source of truth and merge approved features into it from feature branches.
- **Important concepts**:
We merge branches, not individual commits.
We merge based on the current head branch (where ``HEAD`` points).
- **Simple merge example**:
    - Use ``git switch`` to switch to the branch receiving the merge (e.g., ``git switch master``).
    - Use ``git merge branch_name`` to merge the specified branch (e.g., git merge bugfix).
    - This is called a **fast-forward merge** when the receiving branch can simply be moved forward to encompass the other branch's commits.

![master_merge](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/22.JPG)

**[git-merge Docs Link](https://git-scm.com/docs/git-merge)**

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="fast-forward">Performing A Fast Forward Merge</a>

- **Fast-forward merge**: A special, simpler type of merge where Git only needs to move a pointer to catch up on commits.
- **Command**: ``git merge <branch_name>`` (replace ``<branch_name>`` with the actual branch you want to merge).

- **Steps**:
1. Switch to the destination branch (where you want the changes to be merged). Example: ``git switch master``
2. Run ``git merge <branch_name>`` to merge the specified branch into the current branch.

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="merge-commits">Generating Merge Commits</a>
**Concepts**:
- **Fast-forward merge**: When merging a branch with no new commits on the target branch, Git simply moves the branch pointer forward.
- **Non-fast-forward merge (merge commit)**: When the target branch has new commits since the branch to be merged was created, Git creates a new commit to merge the changes. This commit has two parents, one from the target branch and one from the branch being merged.

**Commands**:
- ``git branch <branch_name>``: Creates a new branch.
- ``git checkout <branch_name>``: Switches to a different branch.
- ``git add <file_name>``: Adds a file to the staging area for the next commit.
- ``git commit -m "<message>"``: Commits changes with a message.
- ``git merge <branch_name>``: Merges changes from another branch into the current branch.

**[Back To The Top](#Overview-of-the-Section)**
#

### Resolving Merge Conflicts

![Merge_Conflict](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/23.JPG)

**Deleting a Branch**:
- Command: ``git branch -d <branch_name>``
- Make sure you are not on the branch you want to delete.

**Creating Branches**:
- Command: ``git switch -c <branch_name>``

**Merging Branches**:
- Command: ``git merge <branch_name>``
- This may lead to merge conflicts if changes were made to the same file in both branches.

**Resolving Merge Conflicts**:
- Manually edit the file and remove conflict markers (``<<<<<<<, =======, >>>>>>>``).
- Decide which changes to keep from each branch.
- Save the file.
- Stage the changes: ``git add <file_name>``
- Commit the changes: ``git commit -m "<message>"``

**[Back To The Top](#Overview-of-the-Section)**
#
