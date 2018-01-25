# Table of contents
1. [Vocabulary](#vocabulary)
2. [Configure Git for terminal](#configure)
3. [Configure Git for atom](#configure2)
4. [Commands](#commands)
4. [Best practice](#practice)

## Git vocabulary <a name="vocabulary"></a>
Some introduction text, formatted in heading 2 style

## Terminal installation <a name="configure"></a>
1. Download udacity-terminal-config from udacity to your home directory and name it .udacity-terminal-config
2. copy paste whats in .bash_profile to your .bash_profile
3. Run this code:

  `git config --global user.name "<Your-Full-Name>"`

  `git config --global user.email "<your-email-address>"`

  `git config --global color.ui auto`

  `git config --global merge.conflictstyle diff3`

  `git config --list`


## Atom installation <a name="configure2"></a>

`git config --global core.editor "atom --wait"`



## Commands <a name="commands"></a>

`git init` - Create brand new repositories on your computer

`git clone <path-to-repository-to-clone> <alt:rename-dir>` - Copy existing repos from somewhere else to your local computer

`git status` - Check the status of the repo



*  `On branch master` - This tells us that Git is on the master branch.

*   ` Your branch is up-to-date with 'origin/master'` - This tells us that our project is in sync with the one we copied from

* ` nothing to commit, working directory is clean` - This is saying that there are no pending changes

`git log` - Display information about the existing commits

* `q`- quit/get out of the log
* `git log --oneline` - displays the information in a more organized way.
* `git log --oneline --decorate` - Shows tags, branch etc
* `git log --oneline --decorate --graph --all` - Shows all branches and therefor all commits in the repo
* `git log --stat`- display the files that have been changes in the commit
* `git log -p <alt:SHA code>` - display exactly what has been changed. If alt: you get to see exactly the one commit with the SHA code

`git show <alt:SHA>` - Display information about the given commit. Default = latest commit. Alt = commit with that SHA code

`git add <alt:file1> <alt:file2> <alt:fileN>`- Add files from the working directory to the staging index
* `git add .` - Add ALL the files in the working directory to the staging index

`git commit` - Take files from the staging index and save them in the repository
* `git commit -m "initial commit"` - A shorthand method that bypasses the text editor. Is used for short commit messages

`git diff`  - Displays the difference between two versions of a file. Used to see changes that have been made but havnt been committed, yet.

`git tag` - Add tags to specific commits
* `git tag -a v1.0` - added a tag to most recent commit
* `git tag -d v1.0` - deleted a tag
* `git tag -a v1.0 <alt:SHA>` - Add tag to an older commit

`git branch` - Allows multiple lines of development
* `git branch` - lists out all branch names in repository. Also shows the active branch.
* `git branch <name-of-branch>` - Creates a new branch with name passed in
* `git branch -d <branch-name>` - Deletes a branch

`git checkout` - Switch between different branches and tags
* `git checkout <name-of-branch>` - Swith to nameofbranch



`git merge`- Combines changes on different branches
* `git reset --hard HEAD^` - Use this if you merge on the wrong branch
* `git merge <name-of-branch-to-merge-in>`

### Undoing changes

`git commit --amend` - Alter the most-recent commit

`git revert <SHA-of-commit-to-revert>` - Reverses given commit

`git reset` - Erases commits (dangerous)
Flags: `--mixed` - move them to working directory. `--soft` - move to staging index `--hard` - move to trash

### Working with remotes

`git remote` - Manage remote repository

`git push` - Send changes up to the remote
* `git push <remote shortname> <branch>`


`git pull` - Retrieve update from the remote repo

## Best practice <a name="practice"></a>

1. The goal is that each commit has a single focus. Each commit should record a single-unit change. Each commit should change one aspect of the project.
2. Keep the message short
3. explain WHAT the commit does (not how or why)
4. do not use the word "and" -> break the commit up in parts
5. Your message should finish this phrase "This commit will..." but not include it!
6. Be consistent with how you write commit messages
7. Always use annotated tags when creating tags
8. When you are collaborating with other developers make sure to create a new branch that has descriptive name that describes what changes it contains (Always use topic branches to isolate unrelated changes from eachother)
9.
