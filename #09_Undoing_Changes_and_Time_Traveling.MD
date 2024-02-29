<h1 align="center">Undoing Changes & Time Traveling</h1>

### Overview of the Section
* **[Checking Out Old Commits](#check-old-commits)**
* **[Re-Attaching Our Detached HEAD!](#re-attaching)**
* **[Referencing Commits Relative to HEAD](#rel-to-head)**

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

**[Back To The Top](#Overview-of-the-Section)**
#

