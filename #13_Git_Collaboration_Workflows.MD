<h1 align="center">Git Collaboration Workflows</h1>

### Overview of the Section
* **[The Pitfalls Of A Centralized Workflow](#c-workflow)**
* **[](#)**


#
### <a name="c-workflow">The Pitfalls Of A Centralized Workflow</a>
![Pitfalls](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/65.JPG)

- **Single branch**: Everyone works on the same branch, typically called master or main.
- **Cloning**: Developers clone the repository from a remote server (e.g., GitHub) to their local machines.
- **Pushing**: Uploads local commits to the remote repository.
- **Pulling**: Downloads the latest commits from the remote repository to the local machine.
- **Merging**: Combines different versions of code from different branches.

#### Drawbacks:
- **Frequent merging**: Every developer needs to pull and merge frequently, which can be time-consuming and error-prone, especially for large teams.
- **Difficult collaboration**: It's challenging to work on incomplete features or experiments without affecting the main codebase.
- **Risk of breaking the codebase**: Pushing incomplete or broken code can disrupt everyone's work

#### When to use:
- **Very small teams**: Only recommended for tiny teams with minimal collaboration and experimentation needs.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="merging">Merging Feature Branches</a>

![Merging](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/66.JPG)

- **Merging branches**: This is the process of integrating the changes from a feature branch into the main branch.
- **Risks of merging at will**: This can lead to conflicts and problems, especially on large teams.
- **Option 1**: Merge after discussion: This involves discussing the changes with the team before merging.
- **Option 2**: Pull Requests (covered in next video): This is a more common way to merge branches, which involves a formal request and review process.

#### Commands:
- ``git switch``: This command is used to switch between branches.
- ``git pull``: This command is used to download the latest changes from a remote branch.
- ``git merge``: This command is used to merge the changes from one branch into another.
- ``git push``: This command is used to upload local changes to a remote branch.

**[Back To The Top](#Overview-of-the-Section)**
#