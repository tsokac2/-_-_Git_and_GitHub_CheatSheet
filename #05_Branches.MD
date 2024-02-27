<h1 align="center">Branches</h1>

### Overview of the Section
* **[Branches Intro](#branches)**
* **[Master Branch](#master)**
* **[HEAD -> master](#head-master)**

#
### <a name="branches">Branches Intro</a>

![branches_2](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/16.JPG)

- Git uses commit hashes to uniquely identify each commit. (These look like long strings of letters and numbers.)
- Each commit references one or more parent commits that came before it.
Branches are separate timelines for your project. They allow you to work on different things in isolation.
- You can create a new branch using the ``git branch`` command (e.g., ``git branch new-color-scheme``).
- You can switch between branches using the ``git checkout`` command (e.g., ``git checkout bug-fix``).
- Merging branches allows you to combine changes from one branch into another branch. (This will be covered in a future video.)

![branches](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/15.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="master">Master Branch</a>

![Master](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/17.JPG)

- We are always on a branch, even if we haven't explicitly created one. The default branch is called master.
- ``git init``: This command initializes a new Git repository.
- ``git status``: This command shows the current branch and the status of your working directory.
- The master branch is **not special** from Git's perspective. You can rename or delete it.
- In 2020, GitHub changed the default branch name from master to main. Git itself still uses master as the default.
- Many people use the **feature branching** workflow:
    - The master branch is the source of truth.
    - Developers create new branches for features or bug fixes.
    - When changes are ready, they are merged back into the master branch.

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="head-master">HEAD -> master</a>

![head](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/18.JPG)

- **HEAD**: This is a pointer that refers to the current location in the Git repository, specifically the currently checked out branch.
- **Branch reference**: This refers to the location of a specific branch in the repository.
- **Branch**: A branch is like a bookmark in a book, allowing you to track different development paths without affecting the main codebase (master branch).
- **Switching branches**: This refers to changing the HEAD pointer to point to a different branch, effectively moving to that branch.
- **Commit**: A commit is a snapshot of the codebase at a specific point in time. Making a new commit updates the relevant branch pointer to reflect this change.

**Important commands (not mentioned in the excerpt but relevant to the concepts)**:

- ``git branch``: This command allows you to list, create, rename, and delete branches.
- ``git checkout``: This command allows you to switch between branches.

**[Back To The Top](#Overview-of-the-Section)**
#


**[Back To The Top](#Overview-of-the-Section)**
#
