<h1 align="center">Branches</h1>

### Overview of the Section
* **[Branches Intro](#branches)**
* **[Master Branch](#master)**
* **[HEAD -> master](#head-master)**
* **[Viewing and Creating Branches](#view-branches)**
* **[``git checkout <branch name>``](#checkout)**

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

### <a name="view-branches">Viewing and Creating Branches</a>

- The ``git branch`` command is used to **list** existing branches in a Git repository.
- It does not create or switch branches, just displays them.
- The currently active branch will have an asterisk (*) next to it in the output.
- To exit the branch listing, type q.

![create_branche](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/19.JPG)

**Creating a branch**:
- Use the command: ``git branch <branch_name>``
- Replace ``<branch_name>`` with your desired name (avoid spaces).

**Listing branches**:
- Use the command: ``git branch``

**Switching branches**:
- Use the command: ``git switch <branch_name>``
- Replace ``<branch_name>`` with the branch you want to switch to.

**Important notes**:
- Creating a branch does not switch you to it.
- You can use ``git log`` to see which commit each branch is pointing to.
- Switching branches changes your working directory to the content of the selected branch.


- **Creating a new branch**:
    - Use ``git branch <branch-name>`` to create a new branch based on the current **HEAD**.
    - The current branch you're on when creating a new branch matters.
- **Switching branches**:
    - Use git switch <branch-name> to switch to a different branch.
    - HEAD will point to the new branch after switching.
- **Checking branch history**:
    - Use ``git log`` to view the commit history of the current branch.
- **Adding and committing changes (one-line shortcut)**:
    - Use ``git commit -a -m "<message>"`` to add all staged changes and commit them with a message.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="checkout">``git checkout <branch name>``</a>

![checkout](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/20.JPG)

**Switching Branches**:
- Use ``git checkout <branch_name>`` to switch to an existing branch.
- This is the older way of switching branches compared to ``git switch``.
- Both commands achieve the same outcome.

**Creating and Switching to a Branch (One Step)**:
- Use ``git switch -c <branch_name>`` to create a new branch and switch to it simultaneously.
- This is a shortcut for creating a branch and then switching to it separately.

**Equivalent Command (Less Common)**:
- Use ``git checkout -b <branch_name>`` (not recommended) to create a new branch and switch to it in one step.

**[Back To The Top](#Overview-of-the-Section)**
#



**[Back To The Top](#Overview-of-the-Section)**
#
