Git is a distributed version control system.
Git is free software distributed under the GPL.
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