# git-intermediate-techniques-course

GIT ESSENTIAL

Git config user.name
Git config user.name “Jayrek”

Git config user.email
Git config user.email “jrektabasa@gmail.com”

Git init

Git add <filename>
Git add .

Git commit
Git commit -m “commit message”

Git status

Git push

Git restore —staged <filename>
Git restore .
Git restore —cached <filename>

Git log —online
Git log —grep=‘fix’
Git log -p


Git revert
Git revert <commitID>

Git mv

.gitkeep

Git revert

Git diff
Git diff —staged
Git diff —cached

Git checkout 

Git switch <branchName>
Git switch -c <branchName>

.gitignore


——

Intermediate techniques

Git remote -v
Git fetch
Git remote set-url origin <repo url>


Force push to a remote
Git push -f
Git push —force

Git —reset hard origin/main

Merged branches
Git branch —merged
Git branch —no-merged
Git branch -r —merged

Git branch —merged HEAD
Git branch —merged <branchName>
Git branch —merged HEAD <commit>

Git switch <branchName>

Prune stale branches
Git branch -d <branchName> // Delete local branch	

Git push -d origin <branchname> // Delete remote branch

Git remote prune origin // Delete state remote tracking 	branches
Git remote prune origin —dry-run

// shortcut: prune, then fetch
Git fetch —prune
Git fetch -p

Tagging
Create tag
Git tag <tagName> <commitHash> // add lightweight tag

// add annotated tag (most common)
Git tag -am “version v1.0” <tagName> <commitHash>

Delete tag
Git tag -d <tagName>
Git tag —delete <tagName>

List tags alphabetically
Git tag
Git tag —list
Git tag -l

Git tag -l “v2*” // list tag beginning with “v2”

// List tags with first line of each annotation 
// (-n implies -l)
Git tag -n

// list tags with five lines of each annotation 
Git tag -n5

// work with tags (list SHAs)	
Git show v1.1 
Git diff v1.0..v1.1

Git switch v1.0 // tags are not branches

Git switch -c branch_v1 v1.0

// push a tag to a remote repository
Git push origin <tagName>

// push all tags to a remote repository
Git push origin —tags

// fetch commits and tags
Git fetch

// fetch only tags (with necessary commits)
Git fetch —tags 	

// delete remote tags like remote branches
Git push -d origin <tagName>

Interactive mode
Git add -I
Git add —interactive

Patch mode
Git add —patch
Git add -p

Git stash -p
Git reset -p
Git restore -p
Git commit -p


Share select changes
Cherry picking commits
Git cherry-pick <sha>
Git cherry-pick <sha>..<sha>

Create diff patches
Git diff <sha1>..<sha2> > output.diff // will create an output file

Apply diff patches
Git apply output.diff


Rebasing 

// rebase current branch to tip of main
Git rebase main 

// rebase new_feature to tip of main
Git rebase main new_feature


Git rebase —onto <newBase> <upstream> <branch>
Git rebase —onto ecommerce main new_feature

Git rebase —continue
Git rebase —skip
Git rebase —abort

// return commit where topic branch diverges
Git merge-base main new_feature

Pull Rebase
Git pull -r
Git pull —rebase
Git pull —rebase=preserve
Git pull —rebase=interactive

Logs

// list commits that change filename.txt
Git log filename.txt

// list commits as patches (diffs)
Git log -p
Git log —patch

Blame
// annotate file with commit details
Git blame filename.txt

// ignore whitespace changes
Git blame -w filename.txt

// add a global alias for “praise”
Git config —global alias.praise blame

Bisect
Git bisect start
Git bisect good <treeish>
Git bisect bad <treeish>
Git bisect reset
