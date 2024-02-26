<h1 align="center">Installation & Setup</h1>

### Overview of the Section
* **[Git: Command line & GUIs](#cmd)**
* **[Installing Git!](#install-git)**
* **[Git Name and Email Configuration](#name-email)**
* **[Terminal Course - Intro](#cmd-intro)**
* **[Terminal Course - Navigation](#cmd-navigation)**
* **[Terminal Course - Files and Folders](#cmd-files)**
* **[Terminal Course - Delete Files and Folders](#cmd-delete)**

#
### <a name="cmd">Git: Command line & GUIs</a>

#### Two ways to interact with Git:
- **Command-Line Interface (CLI)**: Powerful, efficient, but less user-friendly.
- **Graphical User Interface (GUI)**: Easier to learn, more visual, but can be less flexible.

#### Pros of CLI:
- Faster for experienced users.
- More powerful and feature-rich.
- Consistent across different platforms.
- Documentation and resources are geared towards CLI.

#### Cons of CLI:
Steeper learning curve.
Less user-friendly interface.

#### Pros of GUI:
- Lower barrier to entry.
- More intuitive and visual.
- Can be a better fit for some users.

#### Cons of GUI:
- May not fully explain what's happening behind the scenes.
- Can lead to dependence on specific software.
- Features and interfaces can vary between different GUIs.

### GitKraken
GitKraken is a cross-platform Git client that provides a graphical interface for managing Git repositories. 

It offers features like visual commit history, drag-and-drop Git branching, real-time collaboration, and integrations with platforms like GitHub, GitLab, and Bitbucket.

[GitKraken Link](https://www.gitkraken.com/)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="install-git">Installing Git!</a>

#### Windows

**Key Points of Installing Git on Windows**:
- Windows installation is trickier than Mac due to Git being designed for Unix.
- Download and install Git Bash, which emulates a Unix experience.
- Consider switching the default text editor from Vim to a more user-friendly option like VS Code.
- Git installer offers options for customizing settings like branch name and line endings (not covered in detail in this summary).
- Verify successful installation by running ``git --version`` in the Git Bash terminal.
- Git Bash is the primary interface for using Git on Windows.

**[git Link](https://git-scm.com/)**

#### Mac
- Most Macs come with git pre-installed, but this course requires version 2.23 or above.
- Check your version with ``git --version`` in the terminal.
- If you need to upgrade, download the latest version from the git website (link provided) and choose the "release" for Mac, not the source release.
- Click on ``"binary installer"`` and download the latest version (greater than 2.23).
- Double-click the downloaded package and follow the installation steps, including granting security permissions.
- Open a new terminal window or tab to verify the updated version with ``git --version``.
- Minor differences exist between versions, but most users won't be affected.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="name-email">Git Name and Email Configuration</a>

**Configuring Git Name and Email**:
- **Purpose**: Identifies you as the author of your commits.
- **Not tied to an account**: It's independent of any online accounts.
- **Benefits**:
    - Tracks individual contributions in collaborative projects.
    - Maintains consistency when publishing work.
**Recommended Settings**:
- **Name**: Use the name you want to be known as a developer.
- **Email**: Use the email you plan to use for your GitHub account (if applicable).
**Configuration Steps**:
- **Global**: Applies to all Git repositories on your machine.
    - Command: ``git config --global user.name "Your Name"``
    - Command: ``git config --global user.email "your_email@example.com"``
- **Local**: Applies to the current repository only.
    - Command: ``git config user.name "Your Name"``
    - Command: ``git config user.email "your_email@example.com"``
**Verification**:
- Command: ``git config user.name`` (to check your username)
- Command: ``git config user.email`` (to check your email)


**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="cmd-intro">Terminal Course - Intro</a>

Basic Unix commands like ``ls``, ``pwd``, ``cd``, ``touch``,``mkdir`` are crucial for navigating the terminal and working with Git.
#
### <a name="cmd-navigation">Terminal Course - Navigation</a>

**Essential Commands**:

- ``ls`` (list): Lists contents of the current directory.
- ``pwd`` (print working directory): Shows the current location.
- ``cd`` (change directory): Allows moving into different folders.
- ``cd..``: Moves back one folder.
- ``open`` (on Mac) / ``start`` (on Windows): Opens the current directory in Finder or File Explorer.

**Navigation on Mac**:

- ``ls`` displays contents of the current directory.
- ``pwd`` reveals the current location.
- ``cd`` allows changing into different folders.
- ``open`` opens the current directory in Finder.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="cmd-files">Terminal Course - Files and Folders</a>

**File Creation with Touch Command**:
- ``touch`` is a command used to create new files.
- Unlike traditional methods through text editors, you can use touch in the terminal.
- Syntax: ``touch <filename>`` creates a file in the current directory.
- Multiple files can be created simultaneously by separating names with spaces.
- Example: ``touch purple.js red.txt orange.py yellow.pdf``.

**Creating Files in Different Directories**:
- You can create files in the current directory or specify a path for a different location.
- Example: ``touch pets/horses/rocky.png`` creates a PNG file in the specified path.
- The location is crucial; if in the home directory, use touch filename, else use the full path.

**Directory Creation with Make Directory Command**:
- ``mkdir`` (make directory) is used to create new directories.
- Syntax: ``mkdir <dirname>`` creates a directory in the current location.
- Multiple directories can be created simultaneously by separating names with spaces.
- Example: ``mkdir turtles sea_turtles land_turtles``.

**Avoiding Spaces in File or Directory Names**:
- Spaces in names can cause issues; it's recommended to use underscores or dashes.
- Example: ``mkdir sea_turtles`` instead of ``mkdir sea turtles``.

**Viewing Files and Directories**:
- ``ls`` is used to list files and directories in the current location.
- Example: ``ls`` shows the current files in the directory.
- Use ``ls <path>`` to view files in a specific location.

**Creating Folders on Windows**:
- The same commands (mkdir and touch) work on Windows in the Command Prompt.
- Example: ``mkdir cars bikes creates`` two folders on the desktop.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="cmd-delete">Terminal Course - Delete Files and Folders</a>

**Deleting Files**:
- Command: ``rm``
- Syntax: ``rm [filename]``
- Be cautious, as it permanently deletes the file.

**Creating Files for Deletion**:
- Use commands like ``touch [filename]`` to create files for practice.

**Deleting Multiple Files**:
- Syntax: ``rm [file1] [file2]``

**Deleting Folders**:
- Normal ``rm`` doesn't work for folders.
- Use ``rm -rf [folder]`` to delete a folder recursively and forcefully.

**Flags and Options**:
- Flags modify command behavior.
- Examples: ``ls -a (list all, including hidden)``, ``rm -rf`` (recursive and force).

**Example Commands**:
- ``touch delete_me``
- ``rm delete_me``
- ``rm delete.txt remove.xls``
- ``rm -rf folder_to_delete``

**[Back To The Top](#Overview-of-the-Section)**