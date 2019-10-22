我们在学习～~
首先，先本地创建文件夹，然后git init初始化文件夹为仓库
然后，在本地创建一个文件，git add readme.txt
git clone 'https://github.com/zhypower/learnGit.git'
git commit -m "first commit"
git remote add origin https://github.com/zhypower/learnGit.git
git push -u origin master


远程库与本地库不一致造成的，在hint中也有提示把远程库同步到本地库就可以了。
git pull --rebase origin master

这个时候我按老师的方法做，
创建并切换分支

git status # 查看当前git仓库状态, 确认处于master分支中

git branch pr-test # 从master分支分出为pr-test的分支

git checkout pr-test # 切换至pr-test分支
修改内容

使用任何自己喜欢用的编辑器/IDE修改内容

add commit push
git status # 查看当前做了哪些修改
git add . # . 表示当前目录 git add . 是把当前目录的所有修改添加到暂存区里
git status # 确认下修改
git commit -m 'this is a commit' # 输入commit信息, 简要概括下本次修改
git log # 查看commit历史
git push # 提交到自己的远程仓库


然后我发现，并没有更新，这是因为pr-test分支没有合并

切换到master分支，合并分支，然后在push就没有问题了，指令如下：

 $ git checkout master  

 $ git merge pr-test(这里换成你的分支名字)

 $ git branch -d pr-test ##当前分支已经没用了，记得删除，如果你还要用就不要删除了

 $ git push -u origin master 
