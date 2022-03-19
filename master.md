# Swami Shreeji

### Commands
```sh

git cofig --list --show-origin --global
git cofig --list --show-origin

# Restore vs Checkout
git restore --stage 
git switch  # works with branch only
git switch -c <newbranch>
git log --online
git checklut HEAD~2
git checkout - # Move to head if you are at detached head
git checkout Hash
# reverting a file changes at both stage and working area
git checkout head index.html
# revert only working area based on sources
git restore --staged index.html
# restore the file from some of hash / head (only restore from hash)
git restore --source HASH|HEAD~2 index.html

# STASH
git stash list
git stash apply <S> # Keep the stash ( stash is shared across branch)
git stash pop
git stash drop <S>
git stash add <S>
git stash save "message"
# show the stash
git stash show <s> -p
# stash based branch
git stash branch new_branch <s>
git stash clear

git commit -a -m "commit message"
git commit -m "message for commit"

# Revert vs Reset
# All revert all lost (entire commit deleted)
git reset HEAD~1 --hard|mixed|soft 
git reset hash --hard # ( deleted the last commit or till that hash)
git reset
git reflog show master # to get the deleted commit

# actually mixed == move to only stage area
# hard = all stage + workign
# soft = 
# mix = 

# move file from stage to work area Unstage
git restore --staged <fname>
# same unstage : stage to working area
git reset head --mixed

# or
# Oportunity to revert only changes done in the the given Hash : individual ahs changes
git revert Hash
git revert Hash

# detached head ( to create a branch from that position)
git checkout Hash
# this will create a name of the branch
git branch <branch name>
git checkout -- # this will take you to head
git switch - # this will take you to head
git show hash filename
git commit --amend # change the message of the commit last"


# Remote repo
git remote -p
git remote
# here origin is just a remote name .. easy to remember remote
git remote add <origin> url
git remote rename oldname newname
git remote remove name

# Rename master to main by github : rename branch
git branch -M main

# removing a remote branch 
git push -d <remote> <branchname>
# removing a local branch
git branch -d <branchname>


git push origin localbranch:remotebranch
git push origin brancn # where you have same branch.
git pull origin main
#upstream link between local and remote branch
git push -u origin master
git push -u origin otherbranch
# git push will start working after upstream 
# get all branch ret=moe too
git branch -r

#setting the upstream for a given branch
git branch --set-upstream-to or --track origin/main
git pull origin main


# tags
git tag
git tag -l "*beta"
git checkout <tag>
tag  == hash
git diff t1 t2
git tag V1.0.0 #create a tag for commit
git tag -a V1.0.0 #created an annotated tag
git show V1.0.0 # to get details
git push origin V1.0.0 #PUSH specific tag .. 
git push origin --tags # all tags will be moved.


# reglogs 90 days local
git reflog
git reflog show master/main
# Name qualifier
git diff main main@{1.month.ago}

```