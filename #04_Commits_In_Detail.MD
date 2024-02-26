<h1 align="center">Commits In Detail</h1>

### Overview of the Section
* **[Keeping Your Commits Atomic](#atomic)**
* **[Escaping VIM & Configuring Git's Default Editor](#configuring)**

#
### <a name="Atomic">Keeping Your Commits Atomic</a>

![Atomic](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/11.JPG)

**Important commands**:

- ``git status``
- ``git add [file]``
- ``git commit -m "[message]"``

**Key points**:

- Keep your commits atomic, which means they should focus on a single change.
- This is important for tracking changes and making it easier to undo mistakes.
- When making a commit, you can specify which files to include using ``git add``.
- Use a clear and concise message when committing changes using ``git commit -m "[message]"``.

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="configuring"> Escaping VIM & Configuring Git's Default Editor </a>

``git config core.editor commands``
Accompanying the configuration instructions in Your Editor, many editors can be set as follows:

**Visual Studio Code**:

``git config --global core.editor "code --wait"``

**[Git Docs for more info](https://git-scm.com/book/en/v2/Appendix-C%3A-Git-Commands-Setup-and-Config)**

**[Back To The Top](#Overview-of-the-Section)**
#