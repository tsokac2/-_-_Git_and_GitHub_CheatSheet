<h1 align="center">Git Behind The Scenes - Hashing & Objects</h1>

### Overview of the Section
* **[Working With The Local Config File](#config-file)**
* **[The Refs Directory](#refs)**
* **[The Objects Directory](#objects)**
* **[Git As A Key-Value Datastore](#git-key)**
* **[Hashing With Git Hash-Object](#hashing)**
* **[Retrieving Data With Git Cat-File](#cat-file)**
* **[Deep Dive Into Git Objects: Blobs](#blobs)**
* **[Deep Dive Into Git Objects: Trees](#trees)**

#
### <a name="config-file">Working With The Local Config File</a>

**[Git Config Docs](https://git-scm.com/docs/git-config)**

**Git config file**:
-Located in every ``.git`` folder of a repository.
-Used for additional configuration of Git for that specific repository.
- Settings are local to the repository unless specified otherwise.

**Changing configurations**:
- Use ``git config`` command followed by the setting and value.
- Use ``--local`` flag with the command to set a local configuration.
- Can be manually edited in the .git/config file.

**Color configuration**:

- Set colors for different parts of Git output using color section in the config file.
- Examples:
    - ``color.branch.current = yellow bold`` (current branch yellow and bold)
    - ``color.diff.old = magenta bold`` (old lines in diff magenta and bold)
- Refer to Git documentation for a list of available colors and attributes.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="refs">The Refs Directory</a>

![Git Tags Versoning](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/82.JPG)

- **Location**: The .git/refs directory stores all references in Git.
- **Subdirectories**: It contains subdirectories for different types of references:
    - ``heads``: Stores references to local branches, each branch having a file named after the branch containing the commit hash it points to.
    - ``tags``: Stores references to tags, similar to branches.
    - ``remotes``: Stores references to remote branches (on other repositories), typically grouped by remote name (e.g., ``origin``).

**Exploring Branch References**:
- You can use ``git log --oneline`` to see the commit hash a branch points to.
- Commands to create a new branch: ``git branch <branch_name>``

**Key takeaway**:
The refs directory stores references (branch names, tag names, etc.) which point to commit hashes. These files contain the commit hash the reference points to.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="objects">The Objects Directory</a>

![Git Tags Versoning](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/83.JPG)

- The ``.git/objects`` folder stores all the important data in a Git repository.
- This includes backups of files, content of commits, and history.
- The contents are stored in a special format and not meant to be viewed directly.
- There are four main types of objects stored here:
    - **Blobs**: Store the actual content of files.
    - **Trees**: Organize blobs into a hierarchical structure like folders and files.
    - **Commits**: Reference trees and contain metadata like author and commit message.
    - **Annotated Tags**: Similar to commits but can store additional information like tag names.
- These objects are identified using unique hashes (those long, crazy strings).
- We will explore hashing and the details of these objects in future videos.

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="git-key">Git As A Key-Value Datastore</a>

![Git Database](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/84.JPG)

**Git is a key-value data store**:
- You can store data (files, folders, text) in Git.
- Git gives you a unique key (SHA-1 hash) to retrieve that data later.

**Example**: Imagine a coat check at a venue.
- You give them your coat, they give you a unique claim check (key).
- Later, you give them the claim check to get your coat back (data).

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="hashing">Hashing With Git Hash-Object</a>

**[Git-hash-object Docs](https://git-scm.com/docs/git-hash-object)**

![Git Database Object Hash](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/85.JPG)

- Git stores information as key-value pairs.
- ``git hash-object`` command calculates the SHA-1 hash of a given file or data provided through standard input (``--stdin``).
- By default, it only outputs the hash and doesn't store the data.
- To store the data in the Git object database, use the ``-w`` flag with ``git hash-object``.
- The data is stored in a folder named after the first two characters of the SHA-1 hash, and the remaining digits are used as the filename within that folder.
- The stored data is compressed and encrypted.

Important Commands:

- ``git hash-object``: This command calculates the SHA-1 hash of a file or data.
- ``--stdin``: This flag tells ``git hash-object`` to read data from standard input.
- ``-w``: This flag tells ``git hash-object`` to write the object to the Git object databas

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="cat-file">Retrieving Data With Git Cat-File</a>
- Git stores information as objects (blobs, trees, commits, tags).
- We can manually store content in Git using the ``git hash-object`` command.
- ``git hash-object <file>``: Calculates the SHA-1 hash of the content in the specified file and prints the hash to the standard output. Optionally stores the object in the database with ``-w`` flag.
- ``git cat-file -p <hash>``: Retrieves an object from the Git database based on the provided hash and pretty-prints the content based on the object type. Use the ``-p`` flag for pretty printing.
- We can use these commands to store and retrieve different versions of a file by hashing the content.
- This is not the same as creating a commit in Git. We will explore blobs in more detail in the next video.

![Retrieving Git Database Object Hash](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/86.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="blobs">Deep Dive Into Git Objects: Blobs</a>

![Blobs](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/87.JPG)

- Git stores content of files in objects called Blobs (Binary Large Objects).
- Blobs are identified by a unique 40 character SHA-1 hash, generated from the content.
- The ``git hash-object`` command can be used to create a blob from a file's content. (Important command to know)
- Blobs themselves don't store filenames, they only store the raw content.
- Blobs are building blocks for other Git objects like Trees and Commits.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="trees">Deep Dive Into Git Objects: Trees</a>

![Trees_01](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/88.JPG)

**Important concepts**:
- Git stores blobs (content of files) and trees (directory structure) as objects.
- Blobs store the contents of a file and do not store the file name.
- Trees store pointers to blobs and other trees.
- Each entry in a tree has a type (blob or tree) and a hash.
- The hash is used to reference the blob or tree object.

**Important commands**:
- ``git cat-file -P <hash>``: This command is used to view the contents of a blob or tree object.
    - ``<hash>`` is the hash of the blob or tree object.
- ``git cat-file -T <hash>``: This command is used to get the type of a Git object (blob or tree).

![Trees_02](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/89.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#

