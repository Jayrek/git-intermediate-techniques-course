This comprehensive list covers various Git commands, workflows, and concepts for version control and collaboration.
Descriptive comments explaining various Git commands and concepts:

### Git Configuration
- `git config user.name`: Configures the global username for Git commits.
- `git config user.name "Jayrek"`: Sets the username "Jayrek" for Git commits.
- `git config user.email`: Configures the global email for Git commits.
- `git config user.email "jrektabasa@gmail.com"`: Sets the email "jrektabasa@gmail.com" for Git commits.

### Repository Initialization and Configuration
- `git init`: Initializes a new Git repository in the current directory.
- `git add <filename>`: Stages a specific file for the next commit.
- `git add .`: Stages all modified and new files for the next commit.
- `git commit`: Commits the staged changes with an editor to add a commit message.
- `git commit -m "commit message"`: Commits staged changes with a concise commit message.
- `git status`: Displays the status of the working directory and staged changes.
- `git push`: Pushes committed changes to a remote repository.

### Undoing Changes
- `git restore --staged <filename>`: Unstages a file from the staging area.
- `git restore .`: Discards unstaged changes in the working directory.
- `git restore --cached <filename>`: Unstages changes but keeps them in the working directory.
- `git log --oneline`: Displays a concise log of commits, showing commit IDs and messages.
- `git log --grep='fix'`: Filters the commit log to show only commits with "fix" in the message.
- `git log -p`: Shows the commit log with the changes introduced in each commit.

### Reverting Changes
- `git revert`: Reverts the changes made in a commit, creating a new commit to undo specific changes.
- `git revert <commitID>`: Reverts changes introduced by a specific commit.

### Other Commands and Concepts
- `git mv`: Moves or renames a file, stage the change, and commit it.
- `.gitkeep`: A convention (not a Git command) used to keep an empty directory tracked in Git.
- `git diff`: Shows the differences between changes in the working directory and the staging area.
- `git diff --staged`: Displays the differences between the staged changes and the last commit.
- `git diff --cached`: Shows the differences between the staged changes and the last commit without unstaging changes.
- `git checkout`: Switches branches or restores working tree files.

### Branch Operations
- `git switch <branchName>`: Switches to an existing branch.
- `git switch -c <branchName>`: Creates a new branch and switches to it.
- `.gitignore`: A file that specifies intentionally untracked files to be ignored by Git.

### Git Remote
- `git remote -v`: Shows the remote repositories along with their URLs.
- `git fetch`: Fetches changes from the remote repository but does not merge them into the local branch.
- `git remote set-url origin <repo url>`: Changes the URL of the remote named "origin."

### Force Push
- `git push -f`: Forces push commits to the remote repository, overwriting history. Use with caution as it can cause data loss.
- `git push --force`: Performs a force push to the remote repository.

### Reset and Branch Operations
- `git reset --hard origin/main`: Resets the current branch to match the main branch in the remote repository.
- `git branch --merged`: Lists branches that have been merged into the current branch.
- `git branch --no-merged`: Lists branches that have not been merged into the current branch.

### Branch Cleanup and Deletion
- `git branch -d <branchName>`: Deletes a local branch.
- `git push -d origin <branchname>`: Deletes a remote branch.
- `git remote prune origin`: Deletes stale remote tracking branches.

### Tags and Tag Operations
- Tag Creation:
  - `git tag <tagName> <commitHash>`: Creates a lightweight tag.
  - `git tag -am "version v1.0" <tagName> <commitHash>`: Creates an annotated tag with a message.
- Tag Deletion:
  - `git tag -d <tagName>`: Deletes a tag.
- Tag Listing:
  - `git tag`
  - `git tag --list`
  - `git tag -l`
  - `git tag -l “v2*”`
  - `git tag -n`: List tags with first line of each annotation (-n implies -l)
  - `git tag -n5`: list tags with five lines of each annotation 
  
- Tag Pushing and Fetching:
  - `git push origin <tagName>`: Pushes a specific tag to a remote repository.
  - `git push origin --tags`: Pushes all tags to a remote repository.
  - `git fetch --tags`: Fetches only tags from a remote repository.

### Rebase and Interactive Rebase
- Rebase Operations:
  - `git rebase main`: Rebases the current branch onto the main branch.
  - `git rebase --onto <newBase> <upstream> <branch>`: Reapplies commits from `<branch>` onto `<newBase>` starting from `<upstream>`.
  - `git rebase --continue`, `git rebase --skip`, `git rebase --abort`: Resumes, skips, or aborts a rebase in progress.
- Pull Rebase:
  - `git pull -r`, `git pull --rebase`: Performs a pull while rebasing instead of merging.

### Logs, Blame, Bisect
- `git log`, `git log -p`: Shows commit history and commit diffs.
- `git blame filename.txt`: Annotates a file with commit details, showing who last modified each line.
- `git bisect`: Helps in finding a specific commit that introduced a bug or issue by performing a binary search.

### Cherry-pick and Patch
- `git cherry-pick <sha>`: Applies the changes introduced by the specified commit onto the current branch.
- `git diff <sha1>..<sha2> > output.diff`: Creates a patch file with changes between two commits.
- `git apply output.diff`: Applies a patch file to the working directory.

### Stashing, Interactive Add/Reset/Restore
- `git stash -p`: Stashes specific changes interactively.
- `git add -i`, `git add --interactive`: Adds changes interactively.
- `git reset -p`, `git restore -p`: Resets or restores changes interactively.
- `git commit -p`: Commits interactively.

These comments aim to provide an overview and understanding of various Git commands, operations, and concepts commonly used in version control workflows.
