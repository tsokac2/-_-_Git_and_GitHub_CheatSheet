<h1 align="center">The Power of Reflogs - Retrieving "Lost" Work</h1>

### Overview of the Section
* **[Git Reflogs](#git-reflogs)**
* **[The Git Reflog Show Command](#git-show)**
* **[Reflog References Around](#r-references)**
* **[Time-Based References](#t-references)**

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
### <a name="r-references">Reflog References Around</a>

![Limitations Reflogs_02](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/95.JPG)

**Referencing entries in a reflog**: 
- Use ``name@{number}`` syntax.
- name is the reference name (e.g., head, master).
- @ symbol separates the name from the qualifier.
- number specifies the position in the reflog history.

- ``git reflog show`` command: Shows the reflog for a specific reference (defaults to HEAD).

- ``git checkout head@{number}``: Checks out the commit that HEAD pointed to number moves ago in the reflog.

- ``git checkout head~{number}`` **(tilde notation)**: Checks out the parent commit of HEAD ``number`` generations back (e.g., tilde2 is the grandparent commit).

- **Using reflogs with other commands**: You can use the same syntax (``name@{number}``) with other Git commands like ``diff`` to compare commits at different points in the reflog history.

**Important to Remember**:

- ``head@{number}`` might not refer to a different commit if the reflog entries involve branch switching or detached HEAD.
- Tilde notation ``(~)`` is a shorthand for referencing parents in the commit history.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="t-references">Time-Based References</a>

![Limitations Reflogs_02](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/96.JPG)

- Git reflogs record timestamps associated with every update to branch tips and other references in your local repository.
- You can use these timestamps to revisit specific points in your Git history with timed qualifiers.

**Important commands and syntax**:
- ``git reflog show``: This command displays the reflog for the HEAD reference by default. You can also specify a different reference like ``git reflog show master``.

- Timed qualifiers: These qualifiers allow you to specify a point in time relative to the present. Examples include:
    - ``HEAD@{yesterday}``: Refers to the state of HEAD one day ago.
    - ``master@{two.days.ago}``: Refers to the state of the master branch two days ago.
    - Other supported qualifiers include "hours ago", "weeks ago", and "months ago".

- Using timed qualifiers with ``git checkout``: You can use timed qualifiers with ``git checkout`` to checkout a specific point in your Git history. For example:
    - ``git checkout master@{one.week.ago}``: Checks out the master branch to the state it was in one week ago.

**[Back To The Top](#Overview-of-the-Section)**