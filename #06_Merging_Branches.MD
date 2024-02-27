<h1 align="center">Merging Branches</h1>

### Overview of the Section
* **[Merging](#merging)**
* **[Merging](#merging)**


#
### Merging

![Merging]()

- **Merging branches**: Combines work from one branch into another using the ``git merge`` command.
**Common workflow**: Treat ``master`` branch (or similar) as the source of truth and merge approved features into it from feature branches.
- **Important concepts**:
We merge branches, not individual commits.
We merge based on the current head branch (where ``HEAD`` points).
- **Simple merge example**:
    - Use ``git switch`` to switch to the branch receiving the merge (e.g., ``git switch master``).
    - Use ``git merge branch_name`` to merge the specified branch (e.g., git merge bugfix).
    - This is called a fast-forward merge when the receiving branch can simply be moved forward to encompass the other branch's commits.


![master_merge]()

**[git-merge Docs](https://git-scm.com/docs/git-merge)**

**[Back To The Top](#Overview-of-the-Section)**
#


### <a name="branches">Branches Intro</a>


**[Back To The Top](#Overview-of-the-Section)**
#
