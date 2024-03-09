<h1 align="center">Git Tags: Marking Important Moments in History</h1>

### Overview of the Section
* **[Git Tags](#git-tags)**
* **[Semantic Versioning](#semantic-versioning)**
* **[Viewing & Searching Tags](#s-tags)**
* **[Creating Annotated Tags](#c-annotated)**
* **[Tagging Previous Commits](#tagging-commits)**
* **[Replacing Tags With Force](#replacing-tags)**
* **[Deleting Tags](#d-tags)**
* **[Pushing Tags](#pushing-tags)**

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

### <a name="c-lightweight">Creating Lightweight Tags</a>

![Create Tags](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/76.JPG)

- There are two types of tags: lightweight and annotated.
- Lightweight tags are simpler and only store a reference to a commit.
- To create a lightweight tag, use the following command:

``git tag <tag_name>``

- The ``<tag_name>`` can be any name you choose to identify the commit.
- By default, the tag will reference the commit that the HEAD is currently pointing to.
- Annotated tags (covered in the next video) store additional information like author name, date, and a tagging message.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="c-annotated">Creating Annotated Tags</a>

![Create Tags Annotated](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/77.JPG)

**Creating an Annotated Tag**:
- Command: ``git tag -a <tag_name> [message]``
- ``-a`` flag: This flag indicates you want to create an annotated tag.
- ``<tag_name>``: The name you want to give to your tag.
- ``[message]``: (Optional) A message you can include with the tag. If omitted, your default text editor will open for you to write a message.

**Alternative way to create an annotated tag (skip editor)**:
- Command: ``git tag -a -m "<message>" <tag_name>``
- ``-m`` flag: This flag lets you pass the tag message directly in the command line.
- ``<message>``: The message you want to include with the tag (in quotes).

**Viewing Tag Information**:
- Command: ``git show <tag_name>``
- ``<tag_name>``: The name of the tag you want to see information about.
- This command will display details like:
    - Tagger name (who created the tag)
    - Date the tag was created
    - Tag message (if provided)
    - Reference to the commit the tag points to

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="tagging-commits">Tagging Previous Commits</a>
![Tagging Previous Commits](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/78.JPG)

- You can tag earlier commits using the commit hash, not just the current HEAD commit.
- Use git log (or git log --oneline) to find the commit hash of the commit you want to tag.
- Tag a specific commit with:

``git tag <tag_name> <commit_hash>``

- ``tag_name`` can be anything descriptive (e.g., mytag).
- You can use the ``-a`` flag for an annotated tag with a message. This example uses a lightweight tag for simplicity.
- After tagging, you can verify the tag with ``git tag`` or ``git log``.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="replacing-tags">Replacing Tags With Force</a>

![Replacing Tags With Force](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/79.JPG)

**Moving Tags in Git**
Git tags are typically immutable (unchanging). However, in specific situations, you can move a tag to point to a different commit using the -f flag with the git tag command.

**Important Command**:
- ``git tag -f <tag_name> <commit_hash>``

**Steps**:
1. Identify the commit hash you want the tag to point to.
2. Use the command ``git tag -f <tag_name> <commit_hash>``, replacing ``<tag_name>`` with the desired tag name and <commit_hash> with the actual commit hash.

**Important Note**:
Using the ``-f`` flag is generally discouraged as it rewrites history. It's recommended only when absolutely necessary.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="d-tags">Deleting Tags</a>

![Tagging Previous Commits](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/80.JPG)

- Use the ``git tag -d`` command followed by the tag name you want to delete.
- This is similar to deleting a branch using ``-d`` flag.
- Example: ``git tag -d deleteme``  (This deletes the tag "deleteme")

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="pushing-tags">Pushing Tags</a>

![Tagging Previous Commits](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/81.JPG)

**Two ways to Push Tags**:

1. Push all new tags:

``git push <remote_name> --tags``
- ``<remote_name>``: The name of the remote repository (e.g., origin).

2. Push a single specific tag:

``git push <remote_name> <tag_name>``

- ``<remote_name>``: The name of the remote repository.
- ``<tag_name>``: The name of the specific tag you want to push.

**[Back To The Top](#Overview-of-the-Section)**