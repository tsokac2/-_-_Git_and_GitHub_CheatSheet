<h1 align="center">Rebasing</h1>

### Overview of the Section
* **[Why Rebasing?](#rebasing)**
* **[The Golden Rule: When NOT to Rebase](#not-rebasing)**
* **[Interactive Rebase](#i-rebase)**

#
### <a name="rebasing">Why Rebasing?</a>
![Rebasing](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/70.JPG)

- ``git rebase`` is a command used for rebase operations in Git.
- There are two main use cases for git rebase:
    - As an alternative to git merge for combining branches.
    - To clean up your Git history by editing or squashing commits.

- Rebasing is an alternative to merging for combining changes from two branches.
- Merging creates merge commits, which can clutter the branch history.
- Rebasing rewrites history by creating new commits on top of the target branch.
- This results in a cleaner and more linear branch history.

****Important commands**:

- ``git rebase``: Rebases the current branch onto another branch.
- ``git rebase -i``: Starts an interactive rebase session, which allows you to edit individual commits before applying them.

**[Git rebase Docs](https://git-scm.com/docs/git-rebase)**

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="not-rebasing">The Golden Rule: When NOT to Rebase</a>
**Rebasing**:
- Rebases commits onto a new base branch, rewriting the commit history.
- This can be useful for keeping the commit history clean and linear, especially in collaborative projects.

**Important to know**:
- Do not rebase commits that have already been shared with others. This can cause problems for collaborators who have already pulled down those commits.
- Only rebase commits that are on your local machine and have not been shared with others.
- You can rebase your feature branches onto the master branch or another branch.
- The command to rebase is git rebase <branch>.

**Additional notes**:
- Rebasing can be a powerful tool, but it is important to use it carefully to avoid causing problems for others.
- If you are working on a team project, it is important to follow the team's workflow for rebasing and merging.

![Rebasing Add](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/71.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="i-rebase">Interactive Rebase</a>
**Rewriting history with Git Rebase**:

- This is an alternative way to use ``git rebase`` beyond merging branches.
- Important: It's not recommended to rewrite history on shared work.
- Use this for cleaning up your branch before sharing:
    - Combine commits.
    - Rename commits.
    - Delete commits.
    - Reorder commits.

**Command**:
``git rebase -i <number of commits to go back>``

- ``<number of commits to go back>`` specifies how far back in your branch history you want to start rewriting.
- The ``-i`` flag enables interactive mode, allowing you to edit commits during the rebase process.

![Interactive Rebasing](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/72.JPG)

**[Back To The Top](#Overview-of-the-Section)**