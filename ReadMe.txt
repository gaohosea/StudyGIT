$ git config --global user.name "Your Name" 		//--global 参数表示这台机器所有仓库都使用这个配置
$ git config --global user.email "email@example.com"
$ mkdir StudyGit //创建StudyGit目录
$ cd StudyGit	//修改当前路径为StudyGit
$ pwd			//显示当前目录
$ git init		//把这个目录变成GIT可以管理的仓库
$ git add filename //把文件添加到仓库<从工作区存入暂存区（stage）>
$ git commit -m "description"	//把文件提交到仓库<从暂存区存入第一分支master>
$ git status //查看当前状态
$ git diff	//查看具体修改内容difference
$ git log	//查看历史记录<不同版本>
$ git log --pretty=online  //单行输出历史记录
$ git reset --hard HEAD^	//回退到上一个版本
$ git reset --hard HEAD^^	//回退到上上一个版本
$ git reset --hard HEAD~100	//回退到上100个版本
$ git reset --hard 456125	//回退到commit id 为456125 的版本
$ git cat filename	//查看filename的内容
$ git reflog	//查看commit id
$ git checkout -- filename  //丢弃工作区的修改
$ git reset HEAD filename  //把暂存区的修改撤销掉，重新放回到工作区
$ rm filename	//删除工作区文件
$ git rm filename // 执行git commit 可以从版本库中删除 
$ ssh-keygen -t rsa -C "youremail@example.com"	创建SSH Key 用于连接远程仓库
$ git remote add origin git@github.com:yourname/StudyGIT.git //本地关联远程仓库
$ git push -u origin master		//把本地库的所以内容推送到远程库上，第一次推送master分支 加-u
$ git branch //查看分支
$ git branch <name> //创建分支
$ git checkout <name> //切换分支
$ git checkout -b <name> //创建+切换分支
$ git merge <name> //合并某分支到当前分支
$ git branch -d <name> //删除分支
$ git log --gragh //查看分支合并图
$ git merge --no--ff -m "merge with no-ff" dev //禁用Fast forward 的合并分支,本次合并会创建一个commit，所以加上-m参数，描述commit
$ git log --gragh --pretty=online --abbrev-commit //查看分支历史
$ git stash  //储藏当前工作现场
$ git stash list //查看储藏工作现场
$ git stash apply //恢复工作现场
$ git stash drop //删除储藏工作现场
$ git stash pop //恢复的同时把stash内容也删了
$ git stash apply stash@{0} //恢复指定的stash
$ git remote -v //查看远程库信息
$ git push origin dev //推送dev分支到远程
$ git checkout -b dev origin/dev  //创建远程origin的dev分支到本地
$ git branch --set-uostream dev origin/dev  //指定本地dev分支与远程orign/dev分支的链接
$ git pull //把最新的提交从origin/dev中抓取下来
$ git tag v1.0 //打一个新标签
$ git tag //查看所有标签
$ git tag v0.9 62246937 //为对应的commit id打上标签
$ git show v0.9  //查看标签信息
$ git tag -s v0.2 -m "signed version 0.2 released" fec145a  //用私钥签名一个标签 需安装gpg
$ git tag -d v0.1  //删除标签
$ git push origin v1.0  //推送标签到远程
$ git push origin --tags //一次性推送全部尚未推送到远程的本地标签
$ git tag -d v0.9
$ git push origin :refs/tags/v0.9 //远程删除标签
