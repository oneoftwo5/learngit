Git is a distributed version control system.
Git is free software distributed under the GPL.
Creating a new branch is quick & simple.
learngit:
git init
git add readme.txt
git commit -m "wrote a readme txt"
git status:查看修改状态
git diff readme.txt:查看修改细节
git log --pretty=oneline:查看版本修改日志
git reset --hard HEAD^:回退至上一版本
git reset --hard 1094a:回退至指定版本
git reflog:记录自己的指令，可以查看版本的名字
git checkout -- readme.txt:把文件在工作区的修改全部撤销（变得和暂存区一样）。
git reset HEAD readme.txt:把暂存区的修改撤销掉，重新放回工作区
小结：
场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。
场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。
git rm readme.txt:删除一个文件

连接远程仓库：
git remote add origin https://github.com/oneoftwo5/learngit.git 关联远程库
git remote add origin git@github.com:oneoftwo5/learngit.git 关联远程库2
git branch -M main 将本地仓库改名（master不好）
git push -u origin main 把本地库的所有内容推送到远程库上
git clone git@github.com:oneoftwo5/gitskills.git 从远程库克隆
之后可以简化成 git push origin main
git remote rm <name> 如果添加的时候地址写错了，或者就是想删除远程库，可以用这个命令。使用前，建议先用git remote -v查看远程库信息
git checkout -b dev :创建并切换到新分支dev.也可以用git switch -c dev
= git branch dev ; git checkout dev
git checkout dev:切换到dev分支，也可以用git switch dev
git branch:查看当前分支，前面有*号的就是现在所在分支
git merge dev:命令用于合并指定分支到当前分支
git branch -d dev: 删除dev分支