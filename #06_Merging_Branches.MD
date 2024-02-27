<h1 align="center">Merging Branches</h1>

### Overview of the Section
* **[Merging](#merging)**
* **[Performing A Fast Forward Merge](#fast-forward)**


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


**[Back To The Top](#Overview-of-the-Section)**
#
