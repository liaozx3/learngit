My first git.

git init
git add file
git commit -m "..."
git status
git diff
git log/reflog
git reset --hard commit_id      e.g. HEAD^^ (HEAD~2)
git reset HEAD file
git checkout -- file
git rm file
git remote add origin git@github.com:Liaozx3/name.git
git push -u origin master
git push origin master
git clone git@github.com:liaozx3/name.git
git checkout -b "newbranch"
git branch "newbranch"
git checkout "branch"
git merge "branch"
git branch -D/d "branch"
git log --graph
git stash
git stash list
git stash apply	stash@{..}	  	git stash drop
git stash pop

查看远程库信息，使用git remote -v；
本地新建的分支如果不推送到远程，对其他人就是不可见的；
从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；
在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；
建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；
从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。
删除远程分支：git push origin :branch-name   (冒号)

命令git tag <name> (commid_id) 用于新建一个标签，默认为HEAD，也可以指定一个commit_id；
git tag -a <tagname> -m "blablabla..."可以指定标签信息；
git tag -s <tagname> -m "blablabla..."可以用PGP签名标签；
命令git tag可以查看所有标签
命令git push origin <tagname>可以推送一个本地标签；
命令git push origin --tags可以推送全部未推送过的本地标签；
命令git tag -d <tagname>可以删除一个本地标签；
命令git push origin :refs/tags/<tagname>可以删除一个远程标签。