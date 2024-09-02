# 简介

配置git

# 安装git

```shell
sudo apt install git
```

# 设置git和github

```shell
# 设置你自己的名字和邮箱
git config --global user.name "YURiCAFei"
git config --global user.email 786053522@qq.com

# 生成 ssh 的密钥，按回车三次
ssh-keygen -t rsa -b 4096 -C "786053522@qq.com"

# 将下面显示的东西添加到你的 github -> setting -> SSH keys 中
cat ~/.ssh/id_rsa.pub

# 测试是否可以连接到你的 github 账户
ssh -T git@github.com

# 删除/添加 github 仓库地址
git remote rm origin
git remote add origin [address]

# 解决fatal: Authentication failed for ‘https://github.com/*/*.git/‘
# https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens 按官网文档先生成token
git remote set-url origin https://<token>@github.com/<username>/<reponame>.git
```

