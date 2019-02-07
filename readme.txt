git 分布式版本控制系统
	
	下载：https://git-scm.com/download/win 外网（慢）
	
	安装：https://www.cnblogs.com/wj-1314/p/7993819.html
	
	配置：
		系统中所有用户；
			$ git config --system user.name "w3c"
			$ git config --system user.email w3c@w3cschool.cn

		当前用户：
			$ git config --global user.name "w3c"
			$ git config --global user.email w3c@w3cschool.cn
			
		当前目录：
			$ git config --global user.name "w3c"
			$ git config --global user.email w3c@w3cschool.cn
			
	功能：提供项目编写阶段的快照。
			克隆资源作为工作目录
			在克隆的资源上添加、修改内容
			同步别人对该项目的修改，更新资源
			提交前查看修改
			提交修改
			对提交资源进行回滚
			
	工作区、缓存区、版本库：
		工作区：git init [project_name] 指定的文件路径
		缓存区：工作区的映射，目录结构随工作区中资源的变动而变动
		版本库：包含缓存区和其他分支。当执行git commit 时，版本库目录结构变成当前工作区的目录结构，默认工作目录为master的目录
	
	git创建仓库：
		1）当前目录结构:
			$ git init
		2）指定目录：
			$ git init dirname(该目录为相对路径：D:\apppath\Git-2.20.1\Git\)
		3）通过GitHub链接创建仓库
			$ git clone URL [可以指定仓库的名字]
	
	基本命令：
		向仓库中添加文件：
			$ git add *.txt
		提交修改：
			$ git commit -m "comment..."
		省去添加缓存，直接提交修改：
			$ git commit -am "comment..."
			
		git status：查看上次提交后是否又有修改
		git status -s 简化输出结果
			A ：没有修改
			AM：有修改
			
		git diff：查看执行git status 的结果的详细信息，显示具体文件的改动信息
	
	
	
	分支：
		查看已有分支：
			git branch
		创建并指定分支名：
			git branch branchname 
		切换分支:
			git checkout branchname
		创建并直接切换分支：
			git checkout -b branchname
	
	合并：
		将指定分支下的文件合并到当前分支
			git merge branchname 
		合并分支后可能有冲突，可以通过手动编辑解决冲突，然后commit掉。
	
	查看历史提交id：
		git log
		简化log：
			git log --oneline
			
	标签：版本信息
		查看标签：
			git tag
			git log --decorate
		创建标签：
			git tag -a tagname
		给指定提交打标签：
			git tag -a tagname commitID
