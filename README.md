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

These comments aim to provide an overview and understanding of various Git commands, operations, and concepts commonly used in version control workflows.
