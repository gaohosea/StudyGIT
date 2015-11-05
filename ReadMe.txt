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