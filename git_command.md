# ⭐ **Git Essentials (Daily Use)** ### **Configure Git**
bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
### **Clone a repo**
bash
git clone <repo-url>
### **Check repo status**
bash
git status
### **Add files**
bash
git add <file>
git add .          # add everything
### **Commit changes**
bash
git commit -m "your message"
### **Push to remote**
bash
git push
git push origin <branch>
### **Pull latest changes**
bash
git pull
git pull origin <branch>
--- # 🌿 **Branches** ### **List branches**
bash
git branch
git branch -a       # include remote branches
### **Create a branch**
bash
git branch <branch-name>
### **Switch branch**
bash
git checkout <branch>
### **Create & switch**
bash
git checkout -b <branch-name>
### **Delete branch**
bash
git branch -d <branch-name>
git branch -D <branch-name>   # force delete
### **Delete remote branch**
bash
git push origin --delete <branch-name>
--- # 🔄 **Merging / Rebasing** ### **Merge a branch into current**
bash
git merge <branch-name>
### **Rebase current branch on another**
bash
git rebase <branch-name>
### **Abort a rebase**
bash
git rebase --abort
--- # 🧽 **Stash (Temporary save)** ### **Stash changes**
bash
git stash
git stash save "message"
### **List stashed items**
bash
git stash list
### **Apply last stash**
bash
git stash apply
### **Apply and delete**
bash
git stash pop
### **Drop a stash**
bash
git stash drop stash@{0}
--- # 🔍 **Logs & History** ### **View commit history**
bash
git log
git log --oneline
git log --graph --oneline --decorate --all
### **Show what changed**
bash
git diff
git diff <file>
git diff <commit1> <commit2>
### **Show a commit**
bash
git show <commit-id>
--- # ⏪ **Undo / Fix Mistakes** ### **Undo last commit (keep changes)**
bash
git reset --soft HEAD~1
### **Undo last commit (discard changes)**
bash
git reset --hard HEAD~1
### **Discard changes in a file**
bash
git checkout -- <file>
### **Reset local branch to remote**
bash
git reset --hard origin/<branch>
### **Revert a commit**
bash
git revert <commit-id>
--- # ☁️ **Remote Repositories** ### **View remotes**
bash
git remote -v
### **Add a remote**
bash
git remote add origin <url>
### **Change remote URL**
bash
git remote set-url origin <new-url>
--- # 🏷️ **Tags** ### **Create a tag**
bash
git tag <tag-name>
### **Create annotated tag**
bash
git tag -a <tag-name> -m "message"
### **List tags**
bash
git tag
### **Push tags**
bash
git push --tags
--- # 🧹 **Cleanup Commands** ### **Remove untracked files**
bash
git clean -f
### **Remove untracked files + dirs**
bash
git clean -fd
--- # 🚀 **Advanced Commands** ### **Squash commits (interactive)**
bash
git rebase -i HEAD~<number>
### **Cherry-pick a commit**
bash
git cherry-pick <commit-id>
### **Fetch without merging**
bash
git fetch
### **Prune deleted remote branches**
bash
git fetch --prune
--- # 🧨 **Danger Zone Commands** ### **Force push**
bash
git push --force
git push -f
### **Delete all local changes**
bash
git reset --hard