<h1 align="center">The Power of Reflogs - Retrieving "Lost" Work</h1>

### Overview of the Section
* **[Git Reflogs](#git-reflogs)**
* **[The Git Reflog Show Command](#git-show)**

#
### <a name="git-reflogs">Git Reflogs</a>

![Reflogs_01](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/91.JPG)

- ``git reflog`` command is useful for recovering from mistakes in Git.
- This command is helpful in situations like:
    - Losing a commit
    - Performing a rebase that shouldn't have been done
    - Undoing something seemingly undoable
- It's not crucial to memorize the specific command as you can find it online (e.g., Stack Overflow) when needed.

**Important (but not critical)**:
- ``git reflog`` can be used for rescuing lost commits and undoing rebases.

![Reflogs_02](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/92.JPG)

![Limitations Reflogs_02](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/93.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="git-show">The Git Reflog Show Command</a>

**[Git-reflog Docs](https://git-scm.com/docs/git-reflog)**

- Important subcommand: ``git reflog show``
- This command displays the history of changes made to HEAD (or another specified branch).
- Unlike ``git log``, ``git reflog show`` includes actions like checking out branches.
- Information in the Reflog can be helpful for recovering from mistakes like deleted commits.
- The Reflog shows entries with a relative numbering system (e.g., ``head@0`` is the most recent).
- You can also use ``git reflog show`` with other references like branch names (e.g., git reflog show donkey).

**Code to remember**:

- ``git reflog show [reference]`` - This command shows the reflog for the specified reference (HEAD by default).

![Limitations Reflogs_02](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/94.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#