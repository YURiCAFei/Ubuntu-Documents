# 简介

如何推送本地文件到自己远程的github仓库

# 新建本地代码仓库

```shell
mkdir repo
cd repo
git init
```

# git add

```shell
git add file.txt      # 添加file.txt文件
git add repo/         # 添加整个目录
git add .             # 添加当前目录下的所有文件和目录
```

# git commit

```shell
git commit -m "Update README file"
```

# 创建、切换分支（可选）

```shell
# 创建分支 git branch命令
git branch feature

# 切换分支 git checkout
get checkout feature

# 删除分支
# 不能删除当前分支
get checkout master
geit branch -d feature
```

# 提交代码

```shell
git remote add <remote-name> <remote-url>
git push <remote-name> <branch-name>
```

remote-name可以自由命名，一般命名为origin

