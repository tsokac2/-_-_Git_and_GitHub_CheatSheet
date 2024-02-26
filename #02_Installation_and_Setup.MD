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



**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="cmd-files">Terminal Course - Files and Folders</a>


**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="cmd-delete">Terminal Course - Delete Files and Folders</a>


**[Back To The Top](#Overview-of-the-Section)**