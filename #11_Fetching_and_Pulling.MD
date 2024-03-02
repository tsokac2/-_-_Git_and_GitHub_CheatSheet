<h1 align="center">GitHub: Fetching & Pulling</h1>

### Overview of the Section
* **[Remote Tracking Branches](#remote-branche)**
* **[Checking Out Remote Tracking Branches](#checking-remote-branche)**
* **[Git Fetch](#git-fetch)**
* **[Git Pull](#git-pull)**
* **[Git Pull & Merge Conflicts](#pull-conflicts)**
#
### <a name="remote-branches">Remote Tracking Branches</a>

![Remote Branche](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/55.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="checking-remote-branche">Checking Out Remote Tracking Branches</a>

**Commands**:
- ``git status``: This command shows the status of the working directory and the staging area. It tells you which files have been modified, staged, or untracked.
- ``git add <file>``: This command adds a file to the staging area, which tells Git that you want to include those changes in the next commit.
- ``git commit -m "<message>"``: This command creates a new commit with the specified message.
- ``git log``: This command shows the commit history of the repository.
- ``git checkout <branch>``: This command switches to the specified branch.
- ``git push origin main``: This command pushes your local commits to the remote repository on GitHub.

**Concepts**:

- **Remote tracking branch:** This is a special branch in your local repository that tracks a branch on a remote repository (like GitHub). It tells you how far ahead or behind you are from the remote branch.
- **Detached HEAD**: This is a state where your HEAD is not pointing to any commit in your local repository. You can be in detached HEAD by checking out a specific commit or a remote tracking branch.
- **Pushing commits**: This is the process of sending your local commits to the remote repository.

![git-swithc-branch](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/56.JPG)

![git-swithc-branch](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/57.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="git-fetch">Git Fetch</a>

- **Fetching**: Used to download changes from a remote repository (e.g., GitHub) to your local repository **without** integrating them into your working directory.
- **Command**: ``git fetch [remote]`` (default remote is ``origin``)
- **Optionally fetch specific branch**: ``git fetch origin master`` (fetches only the ``master`` branch from remote ``origin``)
- **Benefits**:
    - Review changes before integrating them.
    - Maintain a clean working directory.
    - Access downloaded changes even without internet connection.

![Fetching](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/58.JPG)

![git-fetching](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/59.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="git-pull">Git Pull</a>

![git pull](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/60.JPG)

**Command**: ``git pull``

**Purpose**: Downloads changes from a remote repository and merges them into your current branch and working directory.

**Syntax**: ``git pull <remote> <branch>``

- ``<remote>``: The name of the remote repository (e.g., ``origin``).
- ``<branch>``: The branch on the remote repository to pull from (e.g., ``master``).

**Example 1 (movies branch)**:

1. Run git pull origin movies to pull changes from the remote origin/movies branch and merge them into your local movies branch.

**Example 2 (fantasy branch)**:

1. Switch to the fantasy branch.
2. Run git pull origin fantasy to pull changes from the remote origin/fantasy branch and merge them into your local fantasy branch.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="pull-conflicts">Git Pull & Merge Conflicts</a>
- **Pull command**: git pull origin master (or any branch name)
- **Checking for conflicts**: git pull (without origin master) will show conflicts if any exist.
- **Resolving conflicts**:
    - Edit conflicted files and manually combine desired changes.
    - Use visual tools like VS Code to accept both changes.
- **Adding and committing resolved conflicts**:
    - ``git add <file>``
    - ``git commit -m "<message>"``
- **Pushing after resolving conflicts**:
    - ``git push origin master`` (or any branch name)

**[Back To The Top](#Overview-of-the-Section)**