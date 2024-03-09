<h1 align="center">Git Tags: Marking Important Moments in History</h1>

### Overview of the Section
* **[Git Tags](#git-tags)**
* **[Semantic Versioning](#semantic-versioning)**
* **[Viewing & Searching Tags](#s-tags)**

#
### <a name="git-tags">Git Tags</a>

**[Git Tags Docs](https://git-scm.com/docs/git-tag)**

![Git Tags](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/73.JPG)

- Tags are used to mark specific commits (versions) in your Git repository history.
- You can name them anything but typically used for version releases (e.g., v3.1.0.0).
- Tags are like bookmarks pointing to a specific commit unlike branch references which change as you add commits.

**Important command**:

- ``git tag``: This command is used to create, list, delete or manipulate tags.

**There are two types of tags**:

1. **Lightweight tags**:
    - Simpler tags containing just a name and reference to a commit.

2. **Annotated tags** (preferred):
    - Include additional information like tag message, author details and date.

![Git Tags Versoning](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/74.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="semantic-versioning">Semantic Versioning</a>
![Git Tags](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/75.JPG)

Semantic Versioning is a system for assigning version numbers that indicates the severity or the scope of a given release and its changes. Here are the key points:
- The system is three numbers separated by dots: Major.Minor.Patch.
- Major version (X): Incremented for backward incompatible changes.
- Minor version (Y): Incremented for new features that are backward compatible.
- Patch version (Z): Incremented for bug fixes and minor changes.
- Initial public release should be 1.0.0.
- Minor releases reset the patch number to zero (e.g., 1.1.0).
- Patch version shouldn't contain new features or breaking changes.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="s-tags">Viewing & Searching Tags</a>
Here are the key points from the text about viewing tags in Git, including important commands:

**View all tags**:
- Command: ``git tag`` (no arguments)

**List of tags with filtering**:
- Command: ``git tag -l <pattern> ``(use asterisk ``*`` for wildcard)
- ``-l`` (or ``--list``) is required for filtering with a pattern.

**Filtering Example**:
- Find all tags containing "beta": ``git tag -l "*beta*"``

**Additional Notes**:
- Tags are listed by name, which usually corresponds to version numbers.
- Each tag points to a specific commit in the Git history.
- This instructor uses ``-l`` (or ``--list``) even though it's implicit with ``git tag``.

**[Back To The Top](#Overview-of-the-Section)**
#



**[Back To The Top](#Overview-of-the-Section)**
#