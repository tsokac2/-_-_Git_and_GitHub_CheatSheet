<h1 align="center">Comparing Changes With Git Diff</h1>

### Overview of the Section
* **[Intro Git Diff](#diff)**
* **[Guide To Reading Diffs](#reading-diffs)**

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


**[Back To The Top](#Overview-of-the-Section)**
#