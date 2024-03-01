<h1 align="center">GitHub</h1>

### Overview of the Section
* **[What is Github?](#github)**
* **[git clone: Cloning Github Repos](#git-clone)**
* **[Github Setup: SSH Config](#ssh)**
* **[Creating Our First Github Repo!](#git-repo)**
* **[Git Remote](#git-remote)**
* **[Git Push](#git-push)**
* **["git push -u"](#git-push-u)**


#
### <a name="github">What is Github?</a>

![github](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/44.JPG)

![Comparison](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/45.JPG)

#### Why Use GitHub:
- **Collaboration**: Work on projects with others. (No specific commands mentioned)
Open Source Contribution: Contribute to projects, gain experience, and build your resume. (No specific commands mentioned)
- **Exposure and Networking**: Meet other developers and potential mentors. (No specific commands mentioned)
- **Staying Up-to-Date**: Follow projects and receive updates. (No specific commands mentioned)

#### Additional Information:
- GitHub is a popular platform for hosting code and collaborating on projects. (No specific commands mentioned)
- Employers often look at GitHub profiles when hiring developers. (No specific commands mentioned)
- A GitHub profile can showcase your coding skills and experience. (No specific commands mentioned)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="git-clone">git clone: Cloning Github Repos</a>

![git-clone](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/46.JPG)

- **Command**: ``git clone``
- **Purpose**: Creates a local copy of a remote repository.
- **Arguments**: The URL of the remote repository.
- **Example**: ``git clone https://github.com/username/repository.git``
- **Important notes**:
    - Run ``git clone`` outside of an existing Git repository.
    - The command creates a new directory for the cloned repository.
    - ``git clone`` downloads the entire history of the repository.

#### git clone: Cloning Non-Github Repos

**Command**: ``git clone``
- This command is used to create a copy (clone) of an existing Git repository.
- It can be used with repositories hosted on various platforms, not just GitHub.

**Permissions**:
- Public repositories on platforms like GitHub can be freely cloned by anyone.
- Cloning a private repository requires permission from the owner.

**Important**:
- Cloning a repository allows you to work with the code locally, but does not grant permission to push changes back to the original repository without following the proper contribution workflow.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="ssh">Github Setup: SSH Config</a>

#### SSH: Which stands for Secure Shell

![SSH](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/47.JPG)

**[Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)**

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="git-repo">Creating Our First Github Repo!</a>

![Git-Repo_01](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/48.JPG)

![Git-Repo_02](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/49.JPG)

![Git-Repo_03](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/50.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="git-remote">Git Remote</a>
**Commands**:
- ``git remote``: Lists existing remotes in a repository.
- ``git remote -v``: Lists existing remotes with their corresponding URLs.
- ``git remote add <name> <url>``: Adds a new remote named ``<name>`` for the URL ``<url>``.
- (Optional) ``git remote rename <old_name> <new_name>``: Renames an existing remote from <old_name> to <new_name>.
- (Optional) ``git remote remove <name>``: Removes the named remote ``<name>``.

![Remote](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/51.JPG)

```
git remote add origin https://github.com/tsokac2/git-tut.git
git branch -M main
git push -u origin main
```
**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="git-push">``git push``</a>

![git-push](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/52.JPG)

**Pushing Different Branches**:
- You can push any branch, not just ``master``.
- The command syntax remains the same, but replace ``master`` with the name of the branch you want to push.
- Example for pushing to ``empty`` branch: ``git push origin empty``

**Commands**:
- ``git remote add origin <URL>``: Adds a remote repository named "origin" with the provided URL.
- ``git push origin master``: Pushes the local "master" branch to the remote "origin" repository's "master" branch. (This is the most common scenario.)
- ``git push origin <local_branch>:<remote_branch>``: Pushes the local branch "<local_branch>" to the remote branch "<remote_branch>". This allows pushing to branches with different names on the local and remote repository.

![git-push](https://github.com/tsokac2/-_-_Git_and_GitHub_CheatSheet/blob/main/src/53.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#

### <a name="git-push-u">"git push -u"</a>



**[Back To The Top](#Overview-of-the-Section)**
#