# **Git Command**

## Check Git Version 
| Command         | Description       |
| :-------------- | :-----------------|
| `git --version` | Check Git version |


## Generate SSH Key and Set Configurations
| Command                                               | Description                                                           |
| ------------------------------------------------------| --------------------------------------------------------------------- |
|`ssh-keygen`                                           | Generate ssh key                                                      |
|`FILE-PATH`/.ssh/`ADD HERE HOST NAME`                  | Enter the file in which to save the key                               |


##### MacOS
| Command                                               | Description                                                           |
| ----------------------------------------------------- | --------------------------------------------------------------------- |
|cat ~/.ssh/`ADD HERE HOST NAME`.pub                    | show ssh key                                                          |
|`cat ~/.ssh/config`                                    | List of all host and identity files                                   |
|`vi ~/.ssh/config`                                     | Open the SSH client configuration file in the Vi text editor          |
|`touch config`                                         | Create config file                                                    |


##### Window
| Command                                               | Description                                                           |
| ------------------------------------------------------| --------------------------------------------------------------------- |
|type `FILE-PATH`\.ssh\ `ADD HERE HOST NAME`.pub        | show ssh key (window)                                                 |
|notepad `FILE-PATH`\.ssh\ `ADD HERE HOST NAME`.pub     | show ssh key (window)                                                 |
|code `FILE-PATH`\.ssh\ `ADD HERE HOST NAME`.pub        | show ssh key                                                          |
|`New-Item -Name config`                                | Create config file with Powershell                                    |
|`notepad -Name config`                                 | Open config file with notepad and Add Configurations                  |


```plaintext
Generating public/private rsa key pair.
</br>Enter file in which to save the key (C:\Users\admin/.ssh/id_rsa): "ADD HERE HOST NAME"
```


##### Config File Format 

```plaintext
Host github.com-`SET HOST`
  HostName github.com
  User git
  IdentityFile ~/.ssh/`ADD HERE HOST NAME`
  IdentitiesOnly yes
```


##### Set the config of Git
| Command                                       | Description                                                                               |
| :-------------------------------------------- | :---------------------------------------------------------------------------------------- |
| `git config --global user.name` `USER-NAME`   | set Global configuration of User Name and also check config without adding `USER-NAME`    |
| `git config --global user.email` `USER-EMAIL` | Set Global configuration of User Email and also check config without adding `USER-EMAIL`  |
| `git config user.name` `USER-NAME`            | Set Username config in particular folder                                                  |
| `git config user.email` `USER-EMAIL`          | Set Email config in particular folder                                                     |


##### Clone with different host
| Command                                                    | Description                                                           |
| -----------------------------------------------------------| --------------------------------------------------------------------- |
|git clone git@`SET HOST`:`USERNAME`/Git-Python-Commands.git | To use a specific SSH key when cloning a project from a different host, you need to update the SSH configuration file (~/.ssh/config) to define a custom host and associate it with the desired SSH key.   


## Init
| Command                                   | Description                                                    |
| ------------------------------------------| ---------------------------------------------------------------|
| `git init`                                | Create an empty Git repository or reinitialize an existing one |
| `git init --bare`                         | Create a bare Git repository                                   |
| `git init --template=/path/to/template`   | Use a custom directory as a template for the repository        |

## Clone
| Command                                                                  | Description                                                 |
| -------------------------------------------------------------------------| ------------------------------------------------------------|
| `git clone <repository-url>`                                             | Clone a repository into a new directory                     |
| `git clone --branch <branch-name> <repository-url>`                      | Clone a specific branch from a repository                   |
| `git clone --single-branch --branch <branch-name> <repository-url>`      | Clone only a single branch from a repository                |
| `git clone --depth 1 <repository-url>`                                   | Clone a shallow copy of a repository                         |

## Remote
| Command                                   | Description                                                    |
| ------------------------------------------| ---------------------------------------------------------------|
| `git remote add origin <repository-url>` | Add a remote repository named "origin"                    |
| `git remote -v`                           | List all remote repositories                             |
| `git remote rename <old-name> <new-name>` | Rename a remote repository                               |
| `git remote remove <name>`                | Remove a remote repository                               |
| `git remote set-url origin <new-url>`     | Change the URL of a remote repository                    |
| `git remote show origin`                  | Show information about a remote repository               |
| `git remote prune origin`                 | Remove remote tracking branches no longer on the remote  |
| `git remote update`                       | Fetch updates from all remote repositories                   |


## Branch
| Command                                              | Description                                            | 
| ---------------------------------------------------- | ------------------------------------------------------ | 
| `git branch <branch-name>`                      | Create a new branch                                    | 
| `git branch`                                    | List branches (the asterisk denotes the current branch) | 
| `git branch -r`                                     | List all remote branches                              | 
| `git branch -a`                                     | List all branches (local and remote)                   | 
| `git branch --all`                    | List all local and remote branches (alias for `git branch -a`) | 
| `git branch -v`                                     | Show latest commit on each branch                      | 
| `git branch --merged`                               | List branches merged into the current branch            | 
| `git branch --no-merged`                            | List branches not merged into the current branch        | 
| `git branch --contains <commit>`                    | List branches containing a specific commit             | 
| `git branch --no-contain <commit>`                  | List branches not containing a specific commit         | 
| `git branch --remotes`                              | List remote-tracking branches                          | 
| `git branch -D <branch-name>`                    | Delete the branch                                      | 
| `git branch -m <old-branch-name> <new-branch-name>` | Rename the Branch                                    | 

## Checkout
| Command                                     | Description                                                      | 
| --------------------------------------------| -----------------------------------------------------------------| 
| `git checkout <branch-name>`                | Switch to the specified branch                                   | 
| `git checkout -b <new-branch>`             | Create and switch to a new branch                                | 
| `git checkout -b <new-branch> <start-point>`| Create a new branch from a specific commit or branch             | 
| `git checkout -`                                    | Switch to the branch last checked out                  | 
| `git checkout -- <filename>`                | Restore a specific file from the last commit                    | 
| `git checkout -p`                           | Interactively choose individual changes to restore               | 
| `git checkout -q`                           | Quiet mode - suppress output                                     | 
| `git checkout -f`                           | Force checkout                                                   | 
| `git checkout --detach`                     | Detach HEAD from any branch, checking out a specific commit      | 
| `git checkout -B <branch> [<start-point>]`  | Create or reset a branch to a specific commit                    | 


## Switch
| Command                                  | Description                                           | 
| ---------------------------------------- | ----------------------------------------------------- | 
| `git switch <branch-name>`               | Switch to the specified branch                       | 
| `git switch -c <new-branch>`            | Create and switch to a new branch                    | 
| `git switch -d <branch-name>`            | Delete a branch                                      | 
| `git switch -r`                         | Switch to a remote branch                            | 
| `git switch -f <branch-name>`            | Force switch to a branch, discarding changes        | 
| `git switch -t <remote-branch>`         | Switch to a tracking remote branch                  | 
| `git switch -c <new-branch> <start-point>` | Create a new branch based on a specific commit    | 
| `git switch -c <new-branch> <start-point>` | Create a new branch based on a specific commit    | 


## Status
| Command                              | Description                                  | 
| -------------------------------------| -------------------------------------------- | 
|`git status`                          |Show the working tree status                  | 
|`git status -s`                       |Show short status                             | 
|`git status -b`                       |Show the branch information along with status | 
|`git status --ignored`                |Show ignored files                            | 
|`git status --porcelain`              |Show output in a machine-readable format      | 
|`git status --untracked-files=<mode>` | Control handling of untracked files          | 

## Add
| Command                                     | Description                                              | 
| --------------------------------------------| ------------------------------------------------------ | 
| `git add filename.txt`                      | Add file contents to the index                        | 
| `git add -p`                                | Interactively stage changes                           | 
| `git add .`                                 | Add all changes in the current directory              | 
| `git add -u`                                | Add modified and deleted files                       | 
| `git add -A`                                | Add all changes in the entire working tree           | 
| `git add -N filename.txt`                   | Add a new file to the index without content          | 
| `git add -i`                                | Start an interactive add session                     | 

## Commit
| Command                                   | Description                                        | 
| ----------------------------------------- | -------------------------------------------------- | 
| `git commit -m "Commit message"`         | Record changes to the repository                   | 
| `git commit -a -m "Commit message"`      | Stage and commit all modified files               | 
| `git commit --amend`                     | Amend the last commit                              | 
| `git commit --amend --no-edit`           | Amend the last commit without editing the message | 
| `git commit --signoff`                   | Add a Signed-off-by line to commit messages       | 
| `git commit --date="YYYY-MM-DD HH:MM:SS"`| Set the commit date                               | 
| `git commit --allow-empty`               | Allow an empty commit                              | 
| `git commit --reuse-message=<commit>`    | Reuse commit message from a specified commit      | 

## Notes
| Command                                         | Description                                                              | 
| ----------------------------------------------- | ------------------------------------------------------------------------ | 
| `git notes add -m "Note message" <commit-hash>` | Add a note to a commit                                                   | 
| `git notes show <commit-hash>`                  | Show the notes associated with a commit                                  | 
| `git notes edit <commit-hash>`                  | Edit the notes associated with a commit                                  | 
| `git notes remove <commit-hash>`                | Remove the notes associated with a commit                                | 
| `git notes copy <from-commit> <to-commit>`      | Copy notes from one commit to another                                    | 
| `git notes merge <commit1> <commit2>`          | Merge notes from two commits                                              | 
| `git notes append -m "Additional message"`     | Append a message to the existing notes of the current commit             | 
| `git notes show-ref`                           | Show the refs that have notes                                            | 
| `git notes prune`                              | Remove notes for commits that no longer exist                            | 
| `git notes list`                               | List the notes refs                                                       | 

## Log
| Command                          | Description                                         | 
| ---------------------------------| ----------------------------------------------------| 
| `git log`                        | Show commit logs                                    | 
| `git log --oneline`              | Show abbreviated commit logs                        | 
| `git log --graph`                | Show ASCII graph of branch and merge history        | 
| `git log --decorate`             | Show refs names of any commits in the output        | 
| `git log --author=<author>`      | Show commits by a specific author                   | 
| `git log --since=<date>`         | Show commits since a specific date                  | 
| `git log --until=<date>`         | Show commits until a specific date                  | 
| `git log --grep=<pattern>`       | Show commits with a commit message matching a pattern | 
| `git log --stat`                 | Show commit stats                                   | 
| `git log --patch`                | Show commit diffs                                   | 
| `git log <since>..<until>`       | Show commits in a range of revisions                | 
| `git log --author=<author> --grep=<pattern>` | Show commits by a specific author matching a pattern | 

## Shortlog
| Command                          | Description                                               | 
| ---------------------------------| ----------------------------------------------------------| 
| `git shortlog`                   | Summarize 'git log' output by author                      | 
| `git shortlog -s`                | Show commit count only                                    | 
| `git shortlog -n`                | Sort authors by number of commits (in descending order)   | 
| `git shortlog -e`                | Show email addresses along with author names             | 
| `git shortlog -w`                | Ignore whitespace changes                                 | 
| `git shortlog --since=<date>`    | Show commits since a specific date                       | 
| `git shortlog --after=<date>`    | Show commits after a specific date                       | 
| `git shortlog --before=<date>`   | Show commits before a specific date                      | 
| `git shortlog --no-merges`       | Exclude merge commits from the summary                   | 
| `git shortlog --abbrev-commit`   | Show abbreviated commit hashes                           | 


## Push
| Command                                              | Description                                           | 
| -----------------------------------------------------| ------------------------------------------------------| 
| `git push`                                           | Push changes to remote repository OR remembered branch  | 
| `git push origin master`                             | Push changes to the "master" branch                   | 
| `git push -u origin <local-branch>:<remote-branch>`  | Push a local branch to a specific remote branch      | 
| `git push origin --delete <remote-branch>`           | Delete a remote branch                                | 
| `git push origin --tags`                             | Push tags to the remote repository                    | 
| `git push origin :<remote-branch>`                   | Delete a remote branch (alternative)                 | 
| `git push --force origin <branch>`                   | Force push changes to a branch                       | 
| `git push origin HEAD`                               | Push the current branch                              | 
| `git push origin --all`                              | Push all branches to the remote repository           | 
| `git push origin --mirror`                           | Mirror all refs to the remote repository              | 
| `git push --set-upstream origin branch-name`         | Set branch to remote repository                       | 
| `git push -u origin branch-name`                     | Push changes to the remote repository OR remember the branch  | 
| `git push -f`                                       | Force push a branch to your remote repository        | 
| `git push origin +master`                     | Push local changes to the remote master branch              |  


## Revert
| Command                           | Description                                                    | 
| ----------------------------------| ---------------------------------------------------------------| 
| `git revert <commit>`             | Revert some existing commits                                   | 
| `git revert --no-commit <commit>` | Revert changes without committing                              | 
| `git revert --edit <commit>`      | Edit the commit message before reverting                      | 
| `git revert --abort`              | Abort the revert operation                                     | 
| `git revert HEAD`                 | Revert changes in the last commit                              | 
| `git revert --no-commit HEAD`     | Revert changes from the last commit without committing         | 
| `git revert --edit HEAD`          | Edit the commit message before reverting the last commit       | 
| `git revert --abort`              | Abort the revert operation                                     | 
| `git revert --soft HEAD^`         | Soft revert changes from the previous commit                    | 
| `git revert --no-commit --soft HEAD^` | Soft revert changes without committing                        | 
| `git revert --edit --soft HEAD^`  | Edit the commit message before soft reverting                 | 

## Reset
| Command                                  | Description                                                   | 
| ---------------------------------------- | --------------------------------------------------------------| 
| `git reset HEAD <file>`                  | Unstage file(s) from the staging area                         | 
| `git reset --soft HEAD~1`                | Move HEAD to the previous commit, keeping changes             | 
| `git reset --mixed HEAD~1`               | Move HEAD to the previous commit, unstaging changes           | 
| `git reset --hard HEAD~1`                | Discard changes and move HEAD to the previous commit          | 
| `git reset --merge ORIG_HEAD`            | Undo a failed merge                                           | 
| `git reset --keep HEAD~2`                | Move HEAD to two commits ago, keeping local changes          | 

## Restore
| Command                                       | Description                                                 | 
| --------------------------------------------- | ------------------------------------------------------------| 
| `git restore <file>`                          | Restore working tree files                                  | 
| `git restore --source=HEAD~2 --staged <file>` | Restore staged changes from a specific commit               | 
| `git restore --worktree --source=HEAD <file>` | Restore a file to the state at the last commit              | 
| `git restore --staged <file>`                 | Unstage changes for a specific file                         | 
| `git restore --source=HEAD --staged <file>`   | Unstage changes for a specific file from the last commit    | 
| `git restore --source=HEAD~2 <file>`          | Restore a file to the state at a specific commit            | 
| `git restore --source=HEAD~2 --staged .`     | Restore all files to the state at a specific commit         | 
| `git restore --source=HEAD --worktree .`     | Restore all files to the state at the last commit           | 
| `git restore --staged .`                     | Unstage all changes for all files                           | 
| `git restore --source=HEAD --staged .`       | Unstage all changes for all files from the last commit      | 


## Stash
| Command                                   | Description                                                    | 
| ------------------------------------------| ---------------------------------------------------------------| 
| `git stash save "Work in progress"`       | Stash the changes in a dirty working directory away           | 
| `git stash list`                          | List all stashed changes                                      | 
| `git stash show`                          | Show the changes in the latest stash                          | 
| `git stash show -p`                       | Show the patch representing the changes in the latest stash    | 
| `git stash apply`                         | Apply the changes from the latest stash                        | 
| `git stash apply <stash@{n}>`             | Apply the changes from a specific stash                        | 
| `git stash pop`                           | Apply and remove the changes from the latest stash             | 
| `git stash pop <stash@{n}>`               | Apply and remove the changes from a specific stash             | 
| `git stash drop`                          | Remove the latest stash                                        | 
| `git stash drop <stash@{n}>`              | Remove a specific stash                                        | 
| `git stash clear`                         | Remove all stashed changes                                     |


## show-branch
| Command                                        | Description                                                           | 
| ---------------------------------------------- | --------------------------------------------------------------------- | 
| `git show-branch`                              | Show branches and their commits                                       | 
| `git show-branch --more=10`                    | Show more commits                                                     | 
| `git show-branch --topic`                       | Group commits by topic                                                 | 
| `git show-branch --sha1-name`                  | Show full commit SHA-1 names                                           | 
| `git status`                                   | Show the working tree status                                          | 
| `git status -s`                                | Show short status                                                     | 
| `git status -v`                                | Show verbose status                                                   | 
| `git status --ignored`                         | Show ignored files                                                    | 
| `git status --untracked-files=all`             | Show untracked files                                                  | 
| `git status --ignored --untracked-files=all`   | Show all ignored and untracked files                                  |


## Fetch
| Command                                  | Description                                                     | 
| ---------------------------------------- | --------------------------------------------------------------- | 
| `git fetch`                              | Download objects and refs from another repository              | 
| `git fetch origin`                       | Fetch updates from the remote named "origin"                   | 
| `git fetch --all`                        | Fetch updates from all remote repositories                     | 
| `git fetch --prune`                      | Remove remote tracking branches no longer on the remote        | 
| `git fetch origin <branch>`              | Fetch updates for a specific branch from the remote            | 
| `git fetch origin <branch>:<local-branch>` | Fetch updates for a specific branch and rename it locally     | 
| `git fetch --tags`                       | Fetch tags from the remote repository                          | 
| `git fetch --depth=<depth>`              | Limit fetching to the specified number of commits back in history | 
| `git fetch --unshallow`                  | Convert a shallow clone to a complete repository               | 


## Merge
| Command                                   | Description                                                    | 
| ------------------------------------------| ---------------------------------------------------------------| 
| `git merge <branch>`                      | Merge a branch into the current branch                        | 
| `git merge --abort`                       | Abort the current merge operation                             | 
| `git merge --continue`                    | Continue the current merge operation                          | 
| `git merge --no-commit`                   | Perform the merge without creating a commit                  | 
| `git merge --squash <branch>`             | Squash all changes from a branch into a single commit         | 
| `git merge --strategy=<strategy> <branch>`| Specify a merge strategy                                      | 
| `git merge --strategy-option=<option>`    | Pass an option to the merge strategy                          | 
| `git merge --no-ff <branch>`              | Create a merge commit even for fast-forward merges            | 
| `git merge --ff-only <branch>`            | Allow only fast-forward merges                                | 
| `git merge --no-edit <branch>`            | Do not open an editor to edit the merge message               | 


## Prune
| Command                                   | Description                                                    | 
| ------------------------------------------| ---------------------------------------------------------------| 
| `git fetch --prune`                       | Fetch updates and prune deleted remote branches               | 
| `git remote prune origin`                 | Remove remote tracking branches no longer on the remote      | 
| `git branch --prune`                      | Remove local branches that have been deleted on the remote   | 
| `git gc --prune=<mode>`                   | Cleanup unnecessary files and optimize the local repository  | 


## Pull
| Command                                  | Description                                                    | 
| ---------------------------------------- | ---------------------------------------------------------------| 
| `git pull <remote> <branch>`            | Fetch from and integrate with another repository or a local branch | 
| `git pull --rebase <remote> <branch>`   | Fetch and rebase from another repository or a local branch   | 
| `git pull --ff-only <remote> <branch>`  | Perform only a fast-forward merge during pull                | 
| `git pull --no-commit <remote> <branch>`| Fetch and integrate without committing the merge             | 
| `git pull --no-rebase <remote> <branch>`| Fetch and integrate without rebasing                         | 
| `git pull --squash <remote> <branch>`   | Integrate changes as a single squashed commit                | 
| `git pull --recurse-submodules=<option>`| Update submodules along with the pull operation              | 


## Cherry-pick
| Command                                          | Description                                                          | 
| -------------------------------------------------| ---------------------------------------------------------------------| 
| `git cherry-pick <commit>`                       | Apply the changes introduced by a specific commit                     | 
| `git cherry-pick <start>..<end>`                 | Apply the changes from a range of commits                             | 
| `git cherry-pick --continue`                     | Continue the cherry-pick process after resolving conflicts           | 
| `git cherry-pick --abort`                        | Abort the cherry-pick process and return to the pre-cherry-pick state| 
| `git cherry-pick --quit`                         | Stop the cherry-pick process without committing or reverting changes | 
| `git cherry-pick --no-commit <commit>`           | Apply changes from a commit without committing                        | 
| `git cherry-pick --edit <commit>`                | Edit the commit message during cherry-pick                           | 
| `git cherry-pick --signoff <commit>`             | Add a Signed-off-by line to the commit message during cherry-pick   | 
| `git cherry-pick --strategy=<strategy> <commit>` | Use a specific merge strategy during cherry-pick                     | 


## Rebase
| Command                           | Description                                                              | 
| --------------------------------- | ------------------------------------------------------------------------ | 
| `git rebase <branch>`             | Reapply commits on top of another base tip                               | 
| `git rebase --abort`              | Abort a rebase in progress                                              | 
| `git rebase --continue`           | Continue a rebase after resolving conflicts or applying a patch manually | 
| `git rebase --skip`               | Skip the current commit and continue with the next one                   | 
| `git rebase --edit-todo`          | Edit the todo list during an interactive rebase                        | 
| `git rebase --onto <new-base>`   | Rebase commits onto a new base                                           | 


## Submodule
| Command                                            | Description                                                    | 
| -------------------------------------------------- | -------------------------------------------------------------- | 
| `git submodule add <repository-url> <path>`       | Add a new submodule to the repository                        | 
| `git submodule init`                              | Initialize submodules                                       | 
| `git submodule update`                            | Update submodules                                           | 
| `git submodule update --init`                     | Initialize and update submodules in one command             | 
| `git submodule update --recursive`                | Update submodules recursively                               | 
| `git submodule update --remote`                   | Update submodules to the latest commit on their remote branch | 
| `git submodule sync`                              | Synchronize submodule URLs                                 | 
| `git submodule foreach <command>`                 | Run a command in each submodule                            | 
| `git submodule status`                            | Show the status of submodules                              | 
| `git submodule deinit <submodule-path>`           | Deinitialize a submodule                                    | 
| `git submodule absorbgitdirs`                     | Move submodule directories into the superproject            | 


## mv
| Command                                        | Description                                       | 
| -----------------------------------------------| --------------------------------------------------| 
| `git mv <old-filename> <new-filename>`          | Move or rename a file, a directory, or a symlink | 
| `git mv <file1> <file2> <directory>`           | Move multiple files to a directory               | 
| `git mv --force <file1> <file2>`               | Force move, even if the target exists             | 
| `git mv --dry-run <file1> <file2>`             | Perform a dry run, see what would be done         | 
| `git mv --verbose <file1> <file2>`             | Run verbosely, showing files as they are moved    | 
| `git mv --quiet <file1> <file2>`               | Suppress output, only show errors                | 
| `git mv --no-checkout <file1> <file2>`         | Skip checkout and only move/delete                | 
| `git mv --index-only <file1> <file2>`         | Only update the index, not the working directory | 
| `git mv --dry-run --verbose <file1> <file2>`  | Perform a dry run verbosely                       | 
| `git mv --force --dry-run <file1> <file2>`    | Force move in a dry run                           | 
| `git mv --force --verbose <file1> <file2>`    | Force move and run verbosely                      | 


## rm
| Command                     | Description                                               | 
| ----------------------------| ----------------------------------------------------------| 
| `git rm <filename>`         | Remove a file from the working directory and the index    | 
| `git rm --cached <filename>`| Remove a file from the index only                         | 
| `git rm -r <directory>`     | Remove a directory and its contents recursively            | 


## range-diff
| Command                                   | Description                                                                                      | 
| ------------------------------------------| -------------------------------------------------------------------------------------------------| 
| `git range-diff <commit1>..<commit2>`     | Compare two commit ranges                                                                         | 
| `git range-diff <commit1>..<commit2> <path>` | Compare two commit ranges for a specific file or directory                                      | 
| `git range-diff --dual-color <commit1>..<commit2>` | Use dual color highlighting for comparison                                                   | 
| `git range-diff --color-moved <commit1>..<commit2>` | Highlight moved lines during comparison                                                     | 
| `git range-diff --stat <commit1>..<commit2>` | Show abbreviated statistics for changes                                                     | 
| `git range-diff --no-color <commit1>..<commit2>` | Disable color highlighting during comparison                                                | 
| `git range-diff --submodule=log <commit1>..<commit2>` | Include submodule changes in the comparison                                               | 
| `git range-diff --submodule=short <commit1>..<commit2>` | Summarize submodule changes in the comparison                                           | 
| `git range-diff --submodule=diff <commit1>..<commit2>` | Show detailed submodule diffs in the comparison                                          | 
| `git range-diff --submodule=short --dual-color <commit1>..<commit2>` | Summarize submodule changes with dual color highlighting                              | 
| `git range-diff --submodule=diff --color-moved <commit1>..<commit2>` | Show detailed submodule diffs with moved lines highlighted                                | 
| `git range-diff --submodule=none <commit1>..<commit2>` | Exclude submodule changes from the comparison                                              | 


## describe
| Command                               | Description                                                     | 
| ------------------------------------- | --------------------------------------------------------------- | 
| `git describe`                        | Describe the current commit with the nearest tag                 | 
| `git describe --tags`                 | Describe the current commit with the nearest tag, including tags that are not on the commit's history | 
| `git describe --abbrev=<n>`           | Set the number of hex digits to abbreviate object names         | 
| `git describe --contains <commit>`    | Find the tag that contains a specific commit                    | 
| `git describe --all`                  | Show all references (not just tags)                              | 


## bundle
| Command                                           | Description                                                 | 
| --------------------------------------------------| ------------------------------------------------------------| 
| `git bundle create <file> <ref>`                  | Create a binary file containing references and objects      | 
| `git bundle verify <file>`                        | Check the validity of a bundle file                        | 
| `git bundle list-heads <file>`                    | List references in a bundle file                           | 
| `git bundle unbundle <file> <path>`               | Extract objects and references from a bundle file          | 
| `git bundle create --all <file>`                  | Create a bundle with all references                        | 
| `git bundle create --branches=<pattern> <file>`   | Create a bundle with references matching a pattern         | 
| `git bundle create --tags=<pattern> <file>`       | Create a bundle with tags matching a pattern               | 
| `git bundle create --since=<date> <file>`         | Create a bundle with references after a certain date      | 
| `git bundle create --exclude=<pattern> <file>`    | Create a bundle excluding references matching a pattern    | 
| `git bundle create --stdout <ref>... > <file>`    | Write a bundle file to standard output                     | 


## git clean
| Command                | Description                                                  | 
| -----------------------| -------------------------------------------------------------| 
| `git clean -n`         | Dry run: Show which files would be removed                   | 
| `git clean -f`         | Force removal of untracked files                             | 
| `git clean -fd`        | Force removal of untracked files and directories            | 
| `git clean -n -d`      | Dry run: Show which directories would be removed             | 
| `git clean -f -d`      | Force removal of untracked directories                       | 
| `git clean -xdf`       | Force removal of untracked files and directories recursively | 
| `git clean -i`         | Interactive mode: Choose which untracked files to remove     | 
| `git clean -x`         | Remove ignored files also                                   | 
| `git clean -X`         | Remove only ignored files                                   | 
| `git clean -e <pattern>`| Exclude files matching the specified pattern from removal    | 


## grep
| Command                                   | Description                                                    | 
| ------------------------------------------| ---------------------------------------------------------------| 
| `git grep <pattern>`                      | Search for a pattern in files tracked by Git                   | 
| `git grep -n <pattern>`                   | Show line numbers for matching lines                          | 
| `git grep -c <pattern>`                   | Show only the count of matching lines                         | 
| `git grep -l <pattern>`                   | Show only the names of files with matching lines              | 
| `git grep -e <pattern>`                   | Specify a pattern using regular expressions                   | 
| `git grep -i <pattern>`                   | Perform a case-insensitive search                              | 
| `git grep -w <pattern>`                   | Match whole words only                                         | 
| `git grep -v <pattern>`                   | Invert the match, displaying non-matching lines               | 
| `git grep -f <file>`                      | Read patterns from a file                                      | 
| `git grep -L <pattern>`                   | Search for files not matching the pattern                     | 
| `git grep --recurse-submodules <pattern>` | Search in submodules                                           | 


## diff
| Command                                   | Description                                                    | 
| ------------------------------------------| --------------------------------------------------------------- | 
| `git diff`                                | Show changes between commits, commit and working tree, etc     | 
| `git diff <commit1> <commit2>`            | Show changes between two commits                              | 
| `git diff <file>`                         | Show changes for a specific file                               | 
| `git diff --staged`                       | Show changes staged for the next commit                        | 
| `git diff --cached`                       | Show changes staged for the next commit (alias for --staged)   | 
| `git diff --name-only`                    | Show only names of changed files                               | 
| `git diff --color-words`                  | Show word-level differences with color highlighting            | 
| `git diff --stat`                         | Show brief diffstat for changes                                 | 
| `git diff HEAD`                           | Show changes between the working directory and the last commit | 
| `git diff HEAD~3..HEAD`                   | Show changes for a commit range                                | 
| `git diff --color-words <commit1>..<commit2>` | Show word-level differences between two commits            | 


## maintenace
| Command                      | Description                                                              | 
| ---------------------------- | ------------------------------------------------------------------------ | 
| `git maintenance start`      | Start maintenance on the repository                                      | 
| `git maintenance stop`       | Stop maintenance on the repository                                       | 
| `git maintenance status`     | Check the status of maintenance operations                                | 
| `git maintenance pack`       | Pack loose objects in the repository into pack files                     | 
| `git maintenance run`        | Run maintenance tasks on the repository                                  | 
| `git maintenance start-again`| Restart interrupted maintenance operations                                |


## show
| Command                      | Description                                  | 
| ---------------------------- | ---------------------------------------------| 
| `git show`                   | Show various types of objects                | 
| `git show --name-only`       | Show only names of changed files             | 
| `git show --stat`            | Show statistics about changes                | 
| `git show --patch`           | Show the patch introduced by the commit      | 
| `git show HEAD~3`            | Show details of the commit three revisions back | 
| `git show <commit-hash>`     | Show details of a specific commit            | 
| `git show <commit-hash>^`   | Show details of the parent of a commit      | 
| `git show <commit-hash>^2`  | Show details of the second parent of a merge commit | 
| `git show <tag-name>`        | Show details of a specific tag               | 


## tag
| Command                                         | Description                                                    | 
| ----------------------------------------------- | ---------------------------------------------------------------| 
| `git tag`                                       | List all tags                                                  | 
| `git tag <tag-name>`                            | Create a lightweight tag                                        | 
| `git tag -a <tag-name> -m "tag message"`        | Create an annotated tag                                         | 
| `git tag -d <tag-name>`                         | Delete a tag                                                    | 
| `git tag -l <pattern>`                          | List tags matching a pattern                                    | 
| `git tag -v <tag-name>`                         | Verify the signature of a tag                                   | 
| `git show <tag-name>`                           | Show information about a tag                                    | 
| `git push origin <tag-name>`                    | Publish a tag to a remote repository                           | 
| `git push --tags`                               | Publish all tags to a remote repository                        | 
| `git checkout <tag-name>`                       | Switch to a specific tag                                        | 
| `git tag -a <tag-name> <commit-hash>`           | Create an annotated tag at a specific commit                  | 
| `git tag -d $(git tag -l)`                      | Delete all local tags                                           | 
| `git push origin --delete <tag-name>`           | Delete a tag from a remote repository                          | 
| `git push --delete origin <tag-name>`           | Delete a tag from a remote repository (alternative syntax)      | 
| `git tag --contains <commit>`                   | List tags containing a specific commit                         | 
| `git describe --tags`                           | Describe the most recent tag reachable from a commit            | 


## reflog
| Command                           | Description                                                   | 
| ----------------------------------| --------------------------------------------------------------| 
| `git reflog`                      | Show a log of the Git reference history                       | 
| `git reflog show <ref>`           | Show the reflog for a specific reference                      | 
| `git reflog expire --expire-unreachable=now --all` | Prune reflog entries older than the specified time   | 
| `git reflog delete <ref>@{<index>}` | Delete a specific entry from the reflog                | 
| `git reflog delete --expire=<time>` | Delete reflog entries older than the specified time   | 
| `git reflog expire --expire=now --rewrite --all` | Rewrite and prune all reflog entries           |


## annotate
| Command                                           | Description                                                    | 
| --------------------------------------------------| ---------------------------------------------------------------| 
| `git annotate <file>`                             | Show line annotations for a file                              | 
| `git annotate -L <start>,<end> <file>`            | Show annotations for a specific line range                    | 
| `git blame <file>`                                | Show what revision and author last modified each line         | 
| `git blame -L <start>,<end> <file>`               | Show annotations for a specific line range                    | 
| `git blame --reverse <file>`                      | Show what revision and author last modified each line (reversed) | 


## blame
| Command                                           | Description                                                    | 
| --------------------------------------------------| ---------------------------------------------------------------| 
| `git annotate <file>`                             | Show line annotations for a file                              | 
| `git annotate -L <start>,<end> <file>`            | Show annotations for a specific line range                    | 
| `git blame <file>`                                | Show what revision and author last modified each line         | 
| `git blame -L <start>,<end> <file>`               | Show annotations for a specific line range                    | 
| `git blame --reverse <file>`                      | Show what revision and author last modified each line (reversed) | 


## send-email
| Command                                        | Description                                                  | 
| ---------------------------------------------- | -------------------------------------------------------------| 
| `git send-email <options> <rev-list-options>`  | Send a series of patches via email                            | 
| `git send-email --annotate <options> <rev-list-options>` | Annotate the patches with details before sending | 
| `git send-email --compose <options> <rev-list-options>` | Compose emails interactively before sending | 
| `git send-email --smtp-server=<server> <options> <rev-list-options>` | Use a specific SMTP server to send emails | 
| `git send-email --suppress-cc=<address> <options> <rev-list-options>` | Suppress CC recipients from emails | 
| `git send-email --no-validate <options> <rev-list-options>` | Skip email validation checks | 
| `git send-email --confirm=<number> <options> <rev-list-options>` | Confirm email before sending | 
| `git send-email --dry-run <options> <rev-list-options>` | Simulate sending emails without actually sending them | 
| `git send-email --confirm=always <options> <rev-list-options>` | Always confirm before sending emails | 


## citool
| Command         | Description                                    |
|-----------------|------------------------------------------------|
| `git citool`    | Open the Git Commit Tool                       |


## gc
| Command          | Description                                                  |
| -----------------| -------------------------------------------------------------|
| `git gc`         | Cleanup unnecessary files and optimize the local repository  |
| `git gc --auto`  | Run automatic garbage collection                              |
| `git gc --prune` | Remove unreachable objects from the repository               |
| `git gc --aggressive` | Perform aggressive garbage collection                      |
| `git gc --quiet` | Run garbage collection quietly (suppress output)            |
| `git gc --auto --quiet` | Run automatic garbage collection quietly                |
| `git gc --aggressive --prune` | Perform aggressive garbage collection with pruning     |


## gtik
| Command      | Description                           |
| ------------ | ------------------------------------- |
| `gitk`       | Open the Git repository browser      |


## gui
| Command        | Description                               |
| -------------- | ----------------------------------------- |
| `git gui`      | Launch the Git GUI                        |
| `git gui blame <filename>` | View file history in Git GUI      |
| `git gui citool` | Launch the Git Commit Tool         |
| `git gui browser` | Open the Git Repository Browser   |


## worktree
| Command                                               | Description                                                              |
| ------------------------------------------------------| -------------------------------------------------------------------------|
| `git worktree add <path> <branch>`                    | Create a new working directory linked to a branch                        |
| `git worktree list`                                  | List all linked working trees                                           |
| `git worktree lock <path>`                           | Lock a working tree to prevent modifications                             |
| `git worktree unlock <path>`                         | Unlock a previously locked working tree                                  |
| `git worktree prune`                                 | Prune stale working tree metadata                                        |
| `git worktree remove <path>`                         | Remove a linked working tree                                             |
| `git worktree move <path> <new-path>`                | Move a linked working tree to a new location                            |
| `git worktree add <path> <commit-ish>`               | Create a new working directory linked to a specific commit              |
| `git worktree add <path> --detach`                   | Create a new working directory linked to HEAD, detached from any branch |
| `git worktree add <path> <branch> --lock`            | Create a new working directory linked to a branch and lock it           |
| `git worktree add <path> <branch> --force`           | Create a new working directory even if the path already exists          |
| `git worktree add <path> <branch> --recurse-submodules` | Create a new working directory with submodules initialized            |
