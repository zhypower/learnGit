我们在学习～
首先，先本地创建文件夹，然后git init初始化文件夹为仓库
然后，在本地创建一个文件，git add readme.txt
git clone 'https://github.com/zhypower/learnGit.git'
git commit -m "first commit"
git remote add origin https://github.com/zhypower/learnGit.git
git push -u origin master


远程库与本地库不一致造成的，在hint中也有提示把远程库同步到本地库就可以了。
git pull --rebase origin master