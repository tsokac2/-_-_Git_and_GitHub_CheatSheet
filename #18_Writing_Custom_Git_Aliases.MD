<h1 align="center">Writing Custom Git Aliases</h1>

### Overview of the Section
* **[The Global Git Config File](#global-git)**
* **[Git Alias](#git-alias)**

#
### <a name="global-git">The Global Git Config File</a>

![The Global Git Config File](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/97.JPG)

- There are 3 Git config files:
    - Local: ``.git/config`` inside each Git repository
    - Global: ``~/.gitconfig`` (tilde refers to home directory)
    - System-wide: ``/etc/gitconfig`` (not commonly used)
- This video focuses on the Global config file.
- You can view the global config file using: ``git config --global --list`` or ``~/.gitconfig`` (open in text editor)
- Common configurations include:
    - User name: ``user.name``
    - User email: ``user.email``
    - Default editor: (e.g. VS Code) ``core.editor``
- Commands:
    - Set global config: ``git config --global <key> <value>`` (e.g. ``git config --global user.name "John Doe"``)
- Important Note:
    - The syntax for setting configs in the file is different from the command line syntax.
    - File syntax: ``<group>.<property> = <value>`` (e.g. ``user.name = John Doe``)
    - Command line syntax: ``git config --global <group>.<property> <value>``

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="git-alias">Git Alias</a>

![The Global Git Config File](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/98.JPG)

**Git aliases explained**:
- Git aliases are shortcuts for existing git commands.
- You can define custom names (e.g. s or st) for frequently used commands (e.g. git status).
- Aliases are configured using the git config command.

**Setting a basic alias**:

1. Open your git config file (usually ~/.gitconfig).
2. Add a line following this format: ``alias <alias_name> = <git_command>``.

``alias s = status``

3. Save the file.
4. Now you can use your alias (e.g. git s) instead of the full command (e.g. git status).

**Additional points**:
- You can set aliases from the command line using ``git config --global alias.<alias_name> <git_command>``.
- Aliases can be used for combining commands or adding frequently used options.
- Some resources share pre-defined useful aliases.

**[Back To The Top](#Overview-of-the-Section)**
#
