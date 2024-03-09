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

- You can configure Git aliases from the command line using the git config command.
- The syntax is: ``git config --global alias.<alias_name> <command>``. For example, to create an alias named ``showmebranches`` for the ``git branch`` command, you would run: ``git config --global alias.showmebranches git branch``
- You can use the ``--global`` flag to make the alias available for all Git repositories on your system. If you omit the ``--global`` flag, the alias will only be available for the current repository.
- You can check the aliases you have configured by running: ``git config --global -l`` (or ``git config -l`` for local aliases).

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="a-arguments">Aliases With Arguments</a>

- Git aliases can accept arguments.
- When calling an alias with arguments, those arguments are passed through to the original command.
- This allows you to create shortcuts for commands that typically require additional information, like a commit message.

**Here's how to set up an alias with an argument**:

1. Open your ``.gitconfig`` file (usually located in your home directory).
2. Add a line in the ``[alias]`` section with the following format:

``alias_name = command -flag``

- Replace ``alias_name`` with your desired shortcut.
- Replace ``command`` with the actual git command (e.g., commit).
- Replace ``-flag`` with the flag that typically requires an argument (e.g., ``-m`` for commit message).

**Example**:

``CM = commit -m``

This alias allows you to commit changes with a message by running ``git CM "your message"``.

**[Git-aliases Docs](https://www.durdn.com/blog/2012/11/22/must-have-git-aliases-advanced-examples/)**

**[Back To The Top](#Overview-of-the-Section)**