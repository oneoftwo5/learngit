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
git checkout -- readme.txt:把文件在工作区的修改全部撤销（变得和暂存区一样）。
git reset HEAD readme.txt:把暂存区的修改撤销掉，重新放回工作区
小结：
场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。
场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。
git rm readme.txt:删除一个文件