- [基础命令](#基础命令)
  - [建立仓库提示命令](#建立仓库提示命令)
  - [清除缓存重新提交数据 (用于更新.gitnore):](#清除缓存重新提交数据-用于更新gitnore)
  - [修改仓库地址名称后重新绑定仓库](#修改仓库地址名称后重新绑定仓库)
  - [生成公钥与github连接](#生成公钥与github连接)
  - [清除本地修改，拉取仓库最新内容](#清除本地修改拉取仓库最新内容)

## 基础命令

### 建立仓库提示命令

```
echo "# Cyber-Security-Notes" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:kyl1n0/Cyber-Security-Notes.git
git push -u origin main
```

### 清除缓存重新提交数据 (用于更新.gitnore):

```
git rm --cached -r .
git add .
# 当前时间的 commit
git commit -m "$(date)"
```

### 修改仓库地址名称后重新绑定仓库

```
git remote rm origin
git remote add origin git@github.com:moekylin/Do1ng.git
```

### 生成公钥与github连接

```
ssh-keygen
cat ~/.ssh/id_rsa.pub
git config --global user.name "moekylin"
git config --global user.email "moekylin@qq.com"
git config --list
```

### 清除本地修改，拉取仓库最新内容

当本地仓库修改了内容执行 `git pull` 时，会出现如下内容

```
error: Your local changes to the following files would be overwritten by merge:
        README.md
Please commit your changes or stash them before you merge.
```

可以通过两种方式拉取远程仓库内容

方式1：stash 会把所有未提交的修改（包括暂存的和非暂存的）都保存起来，用于后续恢复当前工作目录。
比如下面的中间状态，通过git stash命令推送一个新的储藏，当前的工作目录就干净了。

方式2：--hard 参数撤销工作区中所有未提交的修改内容，将暂存区与工作区都回到上一次版本，并删除之前的所有信息提交：

```
# 方式 1
git stash
git pull
git stash pop
# 方式 2
git reset --hard
git pull
```