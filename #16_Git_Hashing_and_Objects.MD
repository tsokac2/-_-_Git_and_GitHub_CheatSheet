<h1 align="center">Git Behind The Scenes - Hashing & Objects</h1>

### Overview of the Section
* **[Working With The Local Config File](#config-file)**
* **[The Refs Directory](#refs)**

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

![Git Tags Versoning](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/74.JPG)

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