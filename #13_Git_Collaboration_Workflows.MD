<h1 align="center">Git Collaboration Workflows</h1>

### Overview of the Section
* **[The Pitfalls Of A Centralized Workflow](#c-workflow)**

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