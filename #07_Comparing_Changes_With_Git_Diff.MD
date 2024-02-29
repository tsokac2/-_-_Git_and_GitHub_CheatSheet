<h1 align="center">Comparing Changes With Git Diff</h1>

### Overview of the Section
* **[Intro Git Diff](#diff)**


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
