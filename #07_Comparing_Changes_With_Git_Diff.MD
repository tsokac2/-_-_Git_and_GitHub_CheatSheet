<h1 align="center">Comparing Changes With Git Diff</h1>

### Overview of the Section
* **[Intro Git Diff](#diff)**
* **[Guide To Reading Diffs](#reading-diffs)**
* **[Viewing Unstaged Changes](#changes)**

#
### <a name="diff">Intro Git Diff</a>

![diff](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/24.JPG)

- The ``git diff`` command shows changes in a Git repository.
- It can be used to compare various aspects of a repository, including:
    - Working directory vs. staging area: ``git diff`` (without arguments)
    - Working directory vs. last commit: ``git diff HEAD``
    - Two branches: ``git diff <branch1> <branch2>``
    - Two specific commits: ``git diff <commit1> <commit2>``
- The output of ``git diff`` can be complex at first, but it includes information about:
    - Added lines (+ signs)
    - Removed lines (- signs)
    - Modified lines (combination of + and - signs)

![git-diff](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/25.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="reading-diffs">Guide To Reading Diffs</a>

**Understanding Git Diff Output**:

- **File comparison**: The output shows the differences between two versions of a file, typically the old version ``(A)`` and the new version ``(B)``.
- **Chunk headers**: These lines identify different sections of the file that have been changed. They are denoted by ``@@`` symbols and contain information about the line numbers involved.
- **Lines with symbols**: Lines starting with ``-`` represent lines removed from the old version ``(A)``. Lines starting with ``+`` represent lines added to the new version ``(B)``. Lines without symbols are unchanged.
- **Color coding (optional)**: Some tools use color coding to visually distinguish added, removed, and unchanged lines.
- **Multiple chunks**: A single file can have multiple chunks if there are changes in different sections.

**Important Commands (not mentioned in the text, but implied)**:
- ``git diff``: This command is used to view the differences between versions of files in a Git repository.

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="changes">Viewing Unstaged Changes</a>
**Git Diff Commands**:
- ``git diff``: Shows all changes in the working directory that are not staged.
- ``git diff HEAD``: Compares the working directory with the latest commit (HEAD).
- ``git diff staged <file_name> (or git diff --cached <file_name>)``: Shows the changes in a specific file that are staged for the next commit.
- ``git diff HEAD <file_name>``: Compares a specific file in the working directory with the latest commit (HEAD).
- ``git diff``: Shows all unstaged changes in the working directory.
- ``git diff HEAD``: Shows all changes (staged and unstaged) in the working directory since the last commit (pointed to by HEAD).

**Explanation of ``git diff`` output**:
- ``A``: Represents the version of the file in the staging area.
- ``B``: Represents the version of the file in the working directory.
- ``-``: Indicates a line that was removed in the working directory version (compared to the staging area version).
- ``+``: Indicates a line that was added in the working directory version (compared to the staging area version).

![git_diff_stage](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/26.JPG)

- To see **staged changes only**, use the ``git diff --staged`` command (or equivalently, ``git diff --cached``).
- ``git diff`` by itself shows **unstaged changes**.
- ``git diff HEAD`` shows **all changes**, staged and unstaged.
- ``--staged`` and ``--cached`` are aliases for the same functionality.

**[Back To The Top](#Overview-of-the-Section)**
#