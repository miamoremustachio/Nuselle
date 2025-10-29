# 🛠️ Setting up

👤 Set user name
- `git config --global user.name "Your Name"`

✉️ Set user email
- `git config --global user.email "you@example.com"`

📝 Set default code editor
- `git config --global core.editor "code --wait"` 

| _Option_   | _Level_      | _Config location_  |
| ---------- | ------------ | ------------------ |
| `--system` | system level | **/etc/gitconfig** |
| `--global` | user level   | **~/.gitconfig**   |
| none       | repo level   | **./.git/config**  |

# 🐣 Basics

`git status`
 📁 Check the state of the working directory

`git add <file path>`
📇 Add files to the index

![[Screenshot 2024-08-13 195911.png]]

`git commit -m "<message>"` 
📩 Create a commit

> _add — put in the frame, commit — take the shot 📸_

`git commit --amend`
✏️ modify the most recent commit
_(combine staged changes with the previous commit)_

`git rm --cached <file>` 
🗑️ Remove files from the index without deleting them from the local file system

`git push origin <local branch name>`
💨 Push all the commits to the remote repo
 
`git revert <commit>`
⏪ Invert the specified commit changes and appends a new commit


`git clean -n`
🧹 “Dry run” a working tree clean (remove all untracked files)

# 🌿 Branching

`git branch` 
🪴 Show all the local branches (when called w/o arguments)

- `... <branch>`
🌱 Create a new branch

- `... -m <branch>`
🏷️ rename branch

- `... -r`
☁️ Show all the remote branches

- `... -a`
♾️ Show ALL the branches

- `... --list “<pattern>”`
🔎 search branches

`git checkout <branch>` 
🔁 Switch to another branch

- `... -- <file>`
⬆️ Take a file out of previous commit in the current branch

- `... <commit_hash>`
⏮️ Switch the current working directory to the specific commit state _(useful for inspecting old versions of your project)_

- `... -b <branch>`
🔂 Switch to the newly created branch

`git branch -d <branch>`
🗑️ Delete local branch

`git push origin --delete <branch>`
❌ Delete remote branch

`git merge <branch>`
🔀 Сombine multiple sequences of commits into the current branch

`git fetch --prune`
♻️ fetch all remote branches and delete remote refs that are no longer in use

`git switch`
🔁 Switch to another branch

- `... -c`
🔂 Switch to the newly created branch


`git restore <file>`
♻️ Restore file from the index

- `... -- source <branch> <file>`
✳️ Take a file out of another branch

# 📝 Logging

 `git log --oneline`
🗒️ Show all the commits

`git show somebranch:path/to/your/file`
Log file content to the console

# 📮 Stash

`git stash`
📥 Take uncommitted changes (both staged and unstaged) and save them for later use

- `... pop`
🍿 Reapply previously stashed changes

- `... apply`
🔄 Reapply previously stashed changes
_and_  keep them in your stash

- `... drop`
🗑️ Remove a single stash

- `... clear`
🔥 Remove all stashes

- `... save "<message>"`
💾 Save with description

- `... list`
📃 View all stashes

- `... -u`
Include untracked files



[^1]: Sources:
	[https://git-scm.com/](https://git-scm.com/)
	[https://devpractice.ru/category/git/git-for-beginners/](https://devpractice.ru/category/git/git-for-beginners/)
